---
description: >-
  This guide provides step-by-step instructions for a FileWave administrator to
  bundle Little Arms Launcher and its secondary assets into a single, pre-cached
  deployment for school lab environments.
---

# FileWave Deployment on a Mac Environment

### Phase 1: Prepare the Source Machine

The administrator needs a clean technician Mac (or a test lab machine) to capture the entire installation layout.

1. **Install the Launcher:** Download and install **Little Arms Launcher** into the `/Applications` directory on the technician Mac.
2.  **Set the Apps Library to a shared system path:** On first launch, the launcher prompts for a preferred drive/location. **Do not accept the default** for lab deployments — the default is the current user's home folder (`~/Library/Application Support`), which is not shared across student accounts.

    * When prompted, choose a location that resolves to a **system-wide writable path**, such as `/Library/Application Support` _(recommended)_ or `/Users/Shared`.
    * Alternatively, after setup, go to **Settings → General → Management** and set **Apps Library Location** to `/Library/Application Support`.

    > The technician account must have permission to write to the chosen location. You may need to temporarily grant admin access or pre-create the target directory with appropriate ownership (`root:wheel` or `admin`) and permissions.
3. **Download Secondary Content:** Open the launcher, sign in if prompted, and trigger the installation of **Zephyr** and **all required DLC, scenario packs, and support files** used in your courses. Let every download finish completely. Launch Zephyr once and confirm it opens successfully.
4. **Verify the Paths:** Confirm where the files were saved.
   * The launcher should be located at `/Applications/Little Arms Launcher.app`.
   *   The secondary apps and support files must be under the shared Apps Library, **not** inside the launcher `.app` bundle:

       ```
       {AppsLibraryRoot}/Little Arms Studios/Apps/Zephyr/Zephyr.app
       {AppsLibraryRoot}/Little Arms Studios/Apps/Zephyr/DLC/
       ```

       Where `{AppsLibraryRoot}` is the path you selected in step 2 (e.g. `/Library/Application Support`).
   * Record this path — it must match the `rootDir` value stored in launcher settings (see step 5).
5.  **Prepare shared launcher settings (recommended for lab devices):** Copy the launcher's settings directory from the technician account to a shared system path:

    **Source (default):**

    ```
    ~/Library/Application Support/Little Arms Launcher/
    ```

    **Destination (example) Notice the missing \~ in the new path:**

    ```
    /Library/Application Support/Little Arms Launcher/
    ```

    The `app-data-store.json` file inside should have `"setupComplete": true` and `"rootDir"` pointing to your shared Apps Library root (e.g. `"/Library/Application Support"`).

    > **Authentication note:** Session tokens in `user-authentication-data` are encrypted with a key stored in the **macOS Keychain** on the target machine. Pre-cached auth data will **not** transfer to other machines or users. Plan for students to sign in individually.

***

### Phase 2: Build the Fileset in FileWave Central

The administrator will use FileWave Central to capture these files exactly as they sit on the disk.

1. **Open FileWave Central:** Navigate to the **Filesets** section in the left-hand menu.
2. **Create a New Fileset:** Click **New Desktop Fileset** in the top toolbar and select **File/Folder**.
3. **Import the Launcher:** Browse to and select **Little Arms Launcher** from the `/Applications` folder. Click **Open** to import it into the Fileset structure.
4.  **Import the Support Content:** Inside the Fileset window, mimic the system path by navigating to or creating the `Library/Application Support/` folder structure. Right-click, select **Import Files/Folders**, and pull in the `Little Arms Studios` payload folder containing the secondary software:

    ```
    Little Arms Studios/Apps/Zephyr/Zephyr.app
    Little Arms Studios/Apps/Zephyr/DLC/
    ```
5. **Import shared launcher settings (if prepared in Phase 1, Step 5):** In the same `Library/Application Support/` tree, import the shared `Little Arms Launcher` folder (containing `app-data-store.json` and related files).
6.  **Verify the Structure:** Double-check the virtual file system tree inside the Fileset. For a system-wide deployment it must match this layout:

    ```
    root/Applications/Little Arms Launcher.app
    root/Library/Application Support/Little Arms Studios/Apps/Zephyr/Zephyr.app
    root/Library/Application Support/Little Arms Studios/Apps/Zephyr/DLC/…
    root/Library/Application Support/Little Arms Launcher/…   (if using shared settings)
    ```

    Adjust the prefix if you used a different Apps Library root (e.g. `/Users/Shared`).

***

### Phase 3: Set Permissions and Self-Healing Rules

Because this is a school lab, files must be protected from accidental deletion or modification by students.

1. **Set Root Ownership:** Select the top-level folders inside the Fileset, right-click, and select **Properties**. Ensure the Owner is set to `root` and the Group is set to `wheel` (or `admin`).
2. **Configure Executable Permissions:** Ensure the launcher binary and any secondary executables (including contents of `Zephyr.app`) have permissions set to `755` (Read/Write/Execute for Owner, Read/Execute for others).
3. **Enable Self-Healing:** In the file properties, ensure the verification setting is set to **Self-Healing (Reinstall if modified or deleted)**. If a student deletes a support file, DLC pack, or secondary app, FileWave will automatically replace it on the next check-in.

***

### Phase 4: Create and Link the PPPC Security Profile

To stop macOS from prompting students for an admin password when the launcher runs background tasks, a Privacy profile must be attached.

1. **Open Profile Editor:** Go to **Assistants > Profile Editor** in FileWave Central.
2. **Create New Profile:** Click **New**, name it uniquely (e.g. _Little Arms Launcher TCC Permissions_), and scroll down to the **Privacy Preferences Policy Control (PPPC)** payload.
3.  **Add Full Disk Access:** Click the **+** button to add an entry.

    * Enter the launcher's **Bundle Identifier:** `com.littlearms.LittleArmsLauncher`
    * Enter its **Code Requirement** signature (obtain from the signed app using FileWave's code requirement helper or `codesign -dr -` on the installed `.app`).
    * Set the **SystemPolicyAllFiles (Full Disk Access)** option to **Allow**.

    Consider also allowing **Keychain Access** (required for secure storage of authentication encryption keys) and **Accessibility** if prompted by macOS.
4. **Save the Profile:** Click **Save**. This creates a configuration profile alongside your fileset.

***

### Phase 5: Associate and Test the Model

1.  **Configure shared launcher settings for all users (recommended for lab devices):** Deploy an environment variable so every student account reads launcher configuration from the shared system path prepared in Phase 1:

    | Variable                         | Example value                                       |
    | -------------------------------- | --------------------------------------------------- |
    | `LITTLE_ARMS_LAUNCHER_USER_DATA` | `/Library/Application Support/Little Arms Launcher` |

    This can also be passed as a launch argument (takes precedence over the environment variable):

    ```
    --user-data-dir="/Library/Application Support/Little Arms Launcher"
    ```

    Apply via FileWave environment variable payload, custom launch script, or wrapper deployed to `/usr/local/bin/`.
2. **Combine Filesets:** Create a **Fileset Group** containing the payload Fileset, the shared launcher settings Fileset (if applicable), and the PPPC Profile so they travel together.
3. **Target a Test Group:** Drag and drop the Fileset Group onto a small test group of lab computers.
4. **Update the Model:** Click the **Update Model** button in the top toolbar to publish the changes.
5.  **Verify Deployment:** Once FileWave completes the local network transfer, log into a test machine as a **standard student user** (non-admin) and verify:

    | Check                     | Expected result                                                    |
    | ------------------------- | ------------------------------------------------------------------ |
    | Launcher opens            | `/Applications/Little Arms Launcher.app` launches without errors   |
    | No first-run setup prompt | If settings were pre-seeded with `setupComplete: true`             |
    | Student sign-in           | Student can authenticate with their Zephyr account                 |
    | Zephyr appears installed  | Zephyr shows as installed without downloading                      |
    | DLC/content available     | Required scenario packs are present; no re-download needed         |
    | Zephyr launches           | Application opens and loads content from the pre-cached DLC folder |

    The secondary software should load without needing to download anything from the internet. Expand to the rest of the computers after successful testing.
