# IT Departments

Please see the [Security FAQs](../../../privacy-and-security/security/security-faq.md) page for details about authentication, user data, and network requirements.

## Network Requirements

Please see our FAQ about network requirements: [#what-web-ip-addresses-ports-need-to-be-whitelisted-to-access-the-site-and-sim](../../../privacy-and-security/security/security-faq.md#what-web-ip-addresses-ports-need-to-be-whitelisted-to-access-the-site-and-sim "mention")

## Little Arms Launcher and Zephyr Simulator Relationship

We use the Little Arms Launcher (Launcher) application to manage user sessions, downloads, and installations of the Zephyr Drone Simulator (SIM) application.

### Launcher Installation and Setup

When you install the Launcher, you will be prompted to select a drive on which to install applications. You can update this by:

1. Sign into the Launcher
2. Click "Settings"
3. "General" > "Management"
4. Click "Change" under the "Choose the location your installed apps are managed from"
5. Select a new location
6. The Launcher will then update its target location and move necessary files

### Zephyr Installation

{% hint style="danger" %}
It's important that whoever is installing Zephyr for a computer that will be used by other students has the same license as the students
{% endhint %}

When a user signs in to the Launcher, it detects what downloadable content (DLC) the user has access to. DLC can contain anything from [Scenarios ](../../scenarios/)to [Drones](../../drones/). When you click "Install" or "Update", only the user's applicable DLC will be downloaded and installed.

{% hint style="warning" %}
If a student has DLC that the person doing the installation and computer setup did not have, then they will be prompted to "Update" when they sign in to the Launcher. Depending on the computer and students' permissions, this may prompt them to update _every time_ they sign in to the Launcher&#x20;
{% endhint %}

## A Note on AppData

On Windows computers, the Launcher and SIM use the user's AppData folder to handle key files such as DLC and credentials.

{% hint style="danger" %}
If AppData is wiped between user sessions, then DLC may not persist between user sessions. This will result in the user being prompted to "Install" or "Update" Zephyr every time they sign in.
{% endhint %}

{% hint style="danger" %}
If the Launcher does not have permission to read/write to AppData, then the credentials file may not be created by the Launcher or picked up by the SIM. This will result in an "Invalid Credentials" error when they attempt to launch the SIM.
{% endhint %}

## Distributing Little Arms Launcher and Zephyr

Ultimately each organization’s situation and distribution platforms are different, but the same principle can be applied to your situation.

The key points about these applications and their interactions are as follows:

* Zephyr MUST be launched through the Little Arms Launcher
* The Little Arms Launcher is used to manage Zephyr updates
* The Little Arms Launcher is responsible for managing login credentials and downloading required Zephyr content

### Distribution Examples

[Microsoft's Configuration Manager](microsofts-configuration-manager.md)

[Deployment Strategy using Mapped Network Drive](deployment-strategy-using-mapped-network-drive.md)

### Changing the Launcher's User Data Folder Location

The Launcher's configuration and other key files reside in AppData by default. Some organizations have had issues with this folder and its contents persisting between users sessions on the same computer. If you need to change this location, you can do so by following these directions:

1. Create an environment variable called `LITTLE_ARMS_LAUNCHER_USER_DATA` and its value to be the path to the desired location (for example `C:\Little Arms Launcher`)
   1. **Note: it's important that the chosen location will not run into any permissions issues with reading/writing**
2. Close the system's default browser before continuing (the browser needs to pick up the new environment variable in order for deep linking to work after signing in)
3. Test installing/updating Zephyr on the computer and then signing in to the computer with another account
   1. **Note: as a reminder, when installing Zephyr on a computer that is used by other users: whoever is installing Zephyr for a computer that will be used by other students has the same license as the students**

## FAQ Troubleshooting

<details>

<summary>Launcher Sign In Deep Linking Not Allowed</summary>

The sign in process for the Launcher opens a browser window then uses a deep link to communicate back to the Launcher application to finish the sign in process.

Some organizations have had permissions issues with this process, so we provide a method for users to enable a native sign in window within the Launcher application itself.

{% hint style="info" %}
Note: Single Sign On is not supported with this method. Only Email/Password is supported
{% endhint %}

To Enforce the Native Sign In Window:

1. Click Start and type Little Arms Launcher.
2. Right-click Little Arms Launcher in the results and choose Open file location.
   1. A File Explorer window will open showing a shortcut to the app.
3. Right-click the Little Arms Launcher shortcut and choose Properties.
4. On the Shortcut tab, find the Target box.
5. Click at the end of the line, after the closing quote "...Launcher.exe".
6. Press Space, then add: `--enforce-native-login-window`
7. Click Apply, then OK

Your Little Arms Launcher Properties window should look like this

<figure><img src="../../../.gitbook/assets/image (351).png" alt="Little Arms Launcher Properties window" width="375"><figcaption></figcaption></figure>

The next time you open the Launcher and click Sign In, the native sign in window should pop up.

<figure><img src="../../../.gitbook/assets/image (350).png" alt="Launcher Native Sign In Window"><figcaption></figcaption></figure>

</details>

<details>

<summary>Zephyr Installation/Update Does Not Persist Between User Sessions. Users Are Always Prompted to "Install" or "Update"</summary>

Please see the section [#changing-the-launchers-user-data-folder-location](./#changing-the-launchers-user-data-folder-location "mention") for details

</details>
