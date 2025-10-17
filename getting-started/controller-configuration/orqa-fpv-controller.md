# Orqa FPV Controller

## Default Button Mapping

* Left stick: controls ascent, descent and yaw
* Right stick: controls pitch and roll
* Right shoulder rocker \[B]: controls pitch of camera
* Left should rocker \[C]: controls zoom of the camera
* Left shoulder button \[D]: changes camera perspectives from the person to the drone and vise verse
* Right should button \[A]: captures pictures (where relevant)

<figure><img src="../../.gitbook/assets/image (329).png" alt=""><figcaption></figcaption></figure>

## Adjust Gimbal Tension

If you need to adjust the gimbal tensions of your Orqa.FPV controller, please refer to the instructions PDF below provided by Orqa. If this does not resolve your issue then you will need to reach out to Orqa directly.

{% file src="../../.gitbook/assets/FPV.Ctrl_Instructions_-_Gimbal_tensions__1_.pdf" %}

## Troubleshooting

We always recommend connecting controllers to your computer via USB (not Bluetooth) for the most reliable connection. Ensure both ends are fully seated into the computer and controller and make sure the controller is turned on (the on switch is at the base of the controller between the handles. Switching the controller on should result in a "beep" noise and green lights showing on the face of the controller).

A quick way to troubleshoot issues impacting an Orqa controller is to open Zephyr and navigate to Main Menu -> Controller and read the text next to "Currently Using:" in the top bar:

1. If the text says "Currently Using:None", the simulator is not registering the controller at all. This is likely caused by either a connection issue (i.e. bad USB cable connection) or the controller is not powered on.
2. If the text says "Currently Using:Unknown Device", this is a strong indicator the firmware on the controller has not been updated to `1.0.6 - Beta` (displays as `Firmware Version: 1.0.6` in the app once updated).
3. If the text says "Currently Using:Orqa FPV.Ctrl", the simulator is successfully recognizing the controller. If input issues are still occurring, there may be another peripheral connected to the system causing an issue, or there may be an issue with the controller's input mapping/calibration.
