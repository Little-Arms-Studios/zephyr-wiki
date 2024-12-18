# 🪪 Hardware License

Hardware Licenses were introduced for special circumstances where organizations needed to purchase Zephyr pre-loaded on a device. This system allows us to provide these devices and restrict access accordingly.

## Register a Hardware License

{% hint style="info" %}
Institution Admin & Instructor only
{% endhint %}

To register a hardware license, an institution admin will need to:

1. Download and install the Little Arms Launcher on the device.
2. Once installed, login to the Launcher and click "Settings"
3. Click the "Register" button under the "Hardware License" section
4. Select the organization you would like to create the hardware license for
5. Enter a unique name for the hardware license label (something that would help you identify the device that the license is installed on)
6. Click "Register"

Once complete, you should see the hardware license label and an "unregister" button where the "register" button was

## Unregister a Hardware License

{% hint style="info" %}
Institution Admin & Instructors only
{% endhint %}

To unregister a hardware license, you can either do so from the device it's installed on or the Zephyr-Sim.com website.

### From the Device:

1. Open the Little Arms Launcher and login
2. Go to "Settings" and click "Unregister" under the "Hardware License" section

### From the Website:

1. Go to [zephyr-sim.com](https://zephyr-sim.com) and login to your account
2. Select the role associated with your hardware license organization
3. Go to "Manage" > "Hardware Licenses"
4. Find the hardware license from the table and click the "Cog" icon
5. Select "Unregister"

## Creating a Hardware License Organization <a href="#link-your-drone-logbook-account-to-zephyr" id="link-your-drone-logbook-account-to-zephyr"></a>

{% hint style="warning" %}
For LAS Admins, how to create an organization that is hardware restricted
{% endhint %}

1. Login to your Administrator account on Zephyr-Sim.com
2. Go to Manage > Organizations and click "Create"
3. Setup the Organization as normal, but ensure the following values are selected:
   1. Billing Type: Site License
   2. Allow Hardware License: ON
   3. Hardware License Count: _Number based on agreement_
   4. Hardware License Expiration: _Expiration date of hardware licenses based on agreement_
4. On the pop up that follows for selecting the organization product, **make sure that Site License Count is set to Zero** (we'll explain why later), but still make sure that you either select or create the appropriate product that provides them with the necessary scenarios

Why set Site License count to Zero?

Scenario access for Hardware License organizations is granted by the Product > Organization association, NOT the License associated with the user account. For instance, if a user has the following account setup:

{% hint style="info" %}
Roles: \[Any role at the hardware license organization]

Licenses: None
{% endhint %}

If they were to login to a device that **has a hardware license for their organization**, the organization's associated product will be provided and the user will get access to the organization's content.

If they were to login to a device the **does not have a hardware license**, they will encounter an error in the simulator saying "No Licenses Found."

## Change an Existing Organization to Hardware License

{% hint style="warning" %}
For LAS Admins, how to change an existing organization to a hardware license organization
{% endhint %}

1. Login to your Administrator account on zephyr-sim.com
2. Go to Manage > Organizations and find the organization in the table
3. Go to Edit
4. Change the following values:
   1. Billing Type: Site License
   2. Allow Hardware License: ON
   3. Hardware License Count: _Number based on agreement_
   4. Hardware License Expiration: _Expiration date of hardware licenses based on agreement_
5. Complete those edits
6. Go to "Assign Licenses"
7. Unassign all licenses from all users at the organization
8. Go to "Add/Remove Licenses"
9. Set their license count to zero

The organization should be set!

## FAQs

1.

