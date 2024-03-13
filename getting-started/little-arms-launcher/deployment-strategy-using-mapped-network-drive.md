# ⭐ Deployment Strategy using Mapped Network Drive

This article instructs users on the basics of changing application installation locations using the Little Arms Launcher, as well as using a mapped network drive as a deployment strategy.

## 📘Basic Instructions for Changing Application Installation Location <a href="#ud83d-udcd8-basic-instructions-for-changing-application-installation-location" id="ud83d-udcd8-basic-instructions-for-changing-application-installation-location"></a>

By default, the Little Arms Launcher and Zephyr are installed in the following locations:

`C:\Program Files\Little Arms Launcher`

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Default Location for Little Arms Launcher</p></figcaption></figure>

`C:\Little Arms Studios\Apps\Zephyr`

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Default Location for Zephyr App</p></figcaption></figure>

In order to change the installation location of Zephyr, please follow the following steps:

1. Inside the Little Arms Launcher, change the target application installation location by:
   1. Selecting “Settings”
   2. Selecting "Change"
   3. Choosing the new desired drive location

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>The Settings tab within the Little Arms Launcher</p></figcaption></figure>

2. Any files in the old location will be copied over to the new location

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>This message appears within the Little Arms Launcher</p></figcaption></figure>

3. As an example, we have chosen to change the target location to the computer's "D" drive and to place the contents into a folder named "TestLocation".

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Example of moving the installation location to a different folder on a different drive</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Example of folder structure in new installation location after the move</p></figcaption></figure>

{% hint style="warning" %}
Please note that the new location still maintains the "Little Arms Studios/Apps/Zephyr" folder structures within the new location.
{% endhint %}

4. Pressing the "Launch" button in the Little Arms Launcher will run the chosen app from the location set in the Settings tab

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>The green Launch button for launching Zephyr within the Little Arms Launcher</p></figcaption></figure>

## 📘Changing Installation Location to a Mapped Network Drive <a href="#ud83d-udcd8-changing-installation-location-to-a-mapped-network-drive" id="ud83d-udcd8-changing-installation-location-to-a-mapped-network-drive"></a>

We can leverage the Zephyr application’s known folder structure to deploy the app via shared network location. If this solution works best for your situation, please follow these steps:

### Disable the Auto Update Feature <a href="#disable-the-auto-update-feature" id="disable-the-auto-update-feature"></a>

The first step is disabling the auto update feature for the shared application. To do this:

1. Select the grey circle with the **...** symbol top open up the menu
2. Select "App Settings"

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Verify “Automatically apply available updates.” is toggled off

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Configure Application Location <a href="#configure-application-location" id="configure-application-location"></a>

The next step is to configure the Application location. To do this:

1. In Windows, select Start and then "This PC"
2. Select "Computer" and then "Add a network location"
3. Choose the desired folder from the network map

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>In this example, the Application files are on a computer named "GUNGNIRTEMP" in a shared location called "RemoteZephyr"</p></figcaption></figure>

4.  If your map was accepted and successful, you will see your mapped location in the "This PC"

    window as a new folder under "Network locations"

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Example of a successful mapping</p></figcaption></figure>

### Choose Mapped Location Within Little Arms Launcher <a href="#choose-mapped-location-within-little-arms-launcher" id="choose-mapped-location-within-little-arms-launcher"></a>

Finally, you need to set the mapped location as the installation location within the Little Arms Launcher so the Launcher knows where to find the Zephyr application files. To do this:

1. In the Little Arms Launcher, select “Settings”
2. Select "Change" to choose a different drive location

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Select "This PC" and you will see a drive list as well as our new network location.
4. Select the new network location

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
This dialog will appear while the Little Arms Launcher is making the necessary changes.
{% endhint %}

5. When the operation completes, you will see the Little Arms Launcher is now using the Zephyr application folders located on the remote server at the "RemoteZephyr" folder location.

<figure><img src="../../.gitbook/assets/image (15) (1) (1) (1).png" alt=""><figcaption><p>Example of mapped network folder set as the installation location within the Little Arms Launcher</p></figcaption></figure>

6. Pressing the "Launch" button in the Little Arms Launcher will run Zephyr from the remote location

<figure><img src="../../.gitbook/assets/image (16) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Loading times may vary depending on network speed, computer specs, and network traffic.
{% endhint %}
