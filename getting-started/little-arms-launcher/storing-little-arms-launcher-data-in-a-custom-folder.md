# Storing Little Arms Launcher data in a custom folder

Little Arms Launcher can store its data in a location you choose by setting the environment variable **`LITTLE_ARMS_LAUNCHER_USER_DATA`**.

You set a **parent folder** only (for example, Documents). The Launcher then creates or uses a subfolder with the usual name inside it—for example:

<table><thead><tr><th width="145.4140625">Platform</th><th width="229.61328125">Parent folder you set</th><th>Where data is stored</th></tr></thead><tbody><tr><td>macOS</td><td><code>~/Documents</code></td><td><code>~/Documents/Little Arms Launcher</code></td></tr><tr><td>Windows</td><td><code>C:\Users\You\Documents</code></td><td><code>C:\Users\You\Documents\Little Arms Launcher</code></td></tr></tbody></table>

The examples below use **Documents** as the parent folder. You can use Desktop, a network drive, or another path your account can read and write.

***

### Quick start

#### Before you begin (all platforms)

1. **Quit Little Arms Launcher** if it is open.
2. **Choose your parent folder** and note the full path. You configure the parent only—not the `Little Arms Launcher` subfolder.

***

#### macOS

Apps opened from the Dock or Applications folder do not read variables from `.zshrc`. Use a **Launch Agent** so the variable is set when you log in.

3. **Open Terminal** (Applications → Utilities → Terminal) and run:

```bash
mkdir -p ~/Library/LaunchAgents
```

4. **Create the Launch Agent file.** Open **TextEdit**, choose **Format → Make Plain Text**, then copy and paste:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <key>Label</key>
  <string>com.littlearms.launcher-user-data</string>
  <key>ProgramArguments</key>
  <array>
    <string>/bin/sh</string>
    <string>-c</string>
    <string>launchctl setenv LITTLE_ARMS_LAUNCHER_USER_DATA "$HOME/Documents"</string>
  </array>
  <key>RunAtLoad</key>
  <true/>
</dict>
</plist>
```

To use a different parent folder, change `"$HOME/Documents"` (for Desktop, use `"$HOME/Desktop"`; for a fixed path, use `"/Volumes/YourShare/YourFolder"`).

5. **Save the file** in TextEdit: **File → Save**, press **Cmd+Shift+G**, go to `~/Library/LaunchAgents`, and save as `com.littlearms.launcher-user-data.plist`.
6. **Load the Launch Agent** in Terminal (use the same parent path as in step 4):

```bash
launchctl load ~/Library/LaunchAgents/com.littlearms.launcher-user-data.plist
launchctl setenv LITTLE_ARMS_LAUNCHER_USER_DATA "$HOME/Documents"
```

7. **Log out and back in** (or restart your Mac).
8. **Open Little Arms Launcher** from Applications. Data should be in your parent folder, for example `~/Documents/Little Arms Launcher`.
9. **Optional:** In Terminal, run `launchctl getenv LITTLE_ARMS_LAUNCHER_USER_DATA` — you should see your parent path.

***

#### Windows

Windows applies user and system environment variables to desktop apps, shortcuts, and the Start menu—no extra setup beyond setting the variable.

3.  **Open Environment Variables:**

    * Press **Win + R**, type `sysdm.cpl`, press **Enter**.
    * Open the **Advanced** tab → **Environment Variables…**

    On Windows 11 you can also search **Settings** for “environment variables” and choose **Edit environment variables for your account**.
4. **Add a user variable** (under _User variables for …_, not System variables, unless your IT team instructs otherwise):
   * Click **New…**
   * **Variable name:** `LITTLE_ARMS_LAUNCHER_USER_DATA`
   * **Variable value:** your parent folder path, for example `C:\Users\YourName\Documents`
   * Click **OK** on each dialog to save.
5. **Sign out and back in** (or restart Windows) so every app session picks up the new variable.
6. **Open Little Arms Launcher** from the Start menu or desktop shortcut—not from an old Command Prompt window opened before step 4.
7.  **Confirm data location** — Files should appear under your parent folder, for example:

    `C:\Users\YourName\Documents\Little Arms Launcher`
8. **Optional:** Open a **new** Command Prompt and run:

```cmd
echo %LITTLE_ARMS_LAUNCHER_USER_DATA%
```

You should see your parent folder path.

***

### Full guide

#### What this does

`LITTLE_ARMS_LAUNCHER_USER_DATA` tells the Launcher which **parent directory** to use. The app creates or uses a subfolder named like the default location (for example `Little Arms Launcher`, or `Little Arms Launcher Beta` for Beta builds). You do not need to create that subfolder yourself.

#### macOS (detailed)

**Create the Launch Agent**

1. Open **Terminal** and run `mkdir -p ~/Library/LaunchAgents`.
2. Create `com.littlearms.launcher-user-data.plist` with the XML from the macOS quick start section.
3. Save it to `~/Library/LaunchAgents/`.

**Path examples for the plist:**

| Parent folder | Value in `launchctl setenv`       |
| ------------- | --------------------------------- |
| Documents     | `"$HOME/Documents"`               |
| Desktop       | `"$HOME/Desktop"`                 |
| Fixed path    | `"/Volumes/YourShare/YourFolder"` |

**Load and verify**

```bash
launchctl load ~/Library/LaunchAgents/com.littlearms.launcher-user-data.plist
launchctl setenv LITTLE_ARMS_LAUNCHER_USER_DATA "$HOME/Documents"
```

Log out and back in, then open the Launcher from Applications. Confirm data under your parent folder (for example `~/Documents/Little Arms Launcher`).

**Change or remove (macOS)**

**Change folder:** Quit the Launcher, edit the plist, then:

```bash
launchctl unload ~/Library/LaunchAgents/com.littlearms.launcher-user-data.plist
launchctl load ~/Library/LaunchAgents/com.littlearms.launcher-user-data.plist
launchctl setenv LITTLE_ARMS_LAUNCHER_USER_DATA "/your/new/parent/path"
```

Log out and back in. Existing data stays in the old folder until you move it.

**Remove:** Quit the Launcher, then:

```bash
launchctl unload ~/Library/LaunchAgents/com.littlearms.launcher-user-data.plist
rm ~/Library/LaunchAgents/com.littlearms.launcher-user-data.plist
launchctl unsetenv LITTLE_ARMS_LAUNCHER_USER_DATA
```

Log out and back in. The default location is `~/Library/Application Support/Little Arms Launcher` (or the Beta/Alpha name for those builds).

***

#### Windows (detailed)

**Set the variable (graphical)**

1. **Win + R** → `sysdm.cpl` → **Enter**.
2. **Advanced** → **Environment Variables…**
3. Under _User variables_, **New…**
   * Name: `LITTLE_ARMS_LAUNCHER_USER_DATA`
   * Value: parent path, e.g. `C:\Users\YourName\Documents`
4. **OK** through all dialogs.
5. Sign out and back in (or restart).

**Set the variable (Command Prompt, current user)**

Run in **Command Prompt** (replace the path with yours):

```cmd
setx LITTLE_ARMS_LAUNCHER_USER_DATA "C:\Users\YourName\Documents"
```

Close any open Launcher windows, sign out and back in, then start the Launcher again. `setx` does not affect already-running programs.

**Verify**

Open a new Command Prompt:

```cmd
echo %LITTLE_ARMS_LAUNCHER_USER_DATA%
```

Open the Launcher from the Start menu and check for data under `Documents\Little Arms Launcher` (or your chosen parent).

**Change or remove (Windows)**

**Change folder:** Quit the Launcher, update the user variable in **Environment Variables** (or run `setx` with the new path), sign out and back in.

**Remove:** Quit the Launcher, delete the `LITTLE_ARMS_LAUNCHER_USER_DATA` user variable, sign out and back in. Default data location:

`C:\Users\YourName\AppData\Roaming\Little Arms Launcher`

(Beta/Alpha builds use the matching folder name.)

***

### Troubleshooting

| Problem                                | macOS                                                                                                 | Windows                                                                                                                                           |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Launcher still uses the default folder | Log out/in after setup. Run `launchctl getenv LITTLE_ARMS_LAUNCHER_USER_DATA` before opening the app. | Sign out/in after setup. Open Launcher from Start menu, not an old terminal. Run `echo %LITTLE_ARMS_LAUNCHER_USER_DATA%` in a **new** cmd window. |
| Works in Terminal only                 | `.zshrc` is not enough; use the Launch Agent steps above.                                             | N/A — set the variable in Windows Environment Variables, not only in a single cmd session.                                                        |
| Permission errors                      | Ensure the parent folder exists and is writable (check network drives).                               | Same — verify read/write access to the parent path.                                                                                               |
| Beta or Alpha build                    | Set only the parent path; subfolder name matches the build.                                           | Same.                                                                                                                                             |

***

### For IT / lab administrators

<table><thead><tr><th width="154.90234375">Platform</th><th>Recommended deployment</th></tr></thead><tbody><tr><td><strong>Windows</strong></td><td>Set <code>LITTLE_ARMS_LAUNCHER_USER_DATA</code> as a <strong>User</strong> or <strong>System</strong> environment variable via Group Policy, Intune, or SCCM. Applies to GUI apps without extra steps.</td></tr><tr><td><strong>macOS</strong></td><td>Deploy the Launch Agent plist to each user’s <code>~/Library/LaunchAgents/</code> via Jamf, Intune, Kandji, or a login script that runs <code>launchctl setenv</code>.</td></tr></tbody></table>

In both cases, set the **parent** directory path only. The Launcher creates the `Little Arms Launcher` (or Beta/Alpha) subfolder automatically.
