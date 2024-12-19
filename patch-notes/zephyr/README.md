---
icon: drone
---

# Zephyr

## v1.8.5

### December 19, 2024

_This update includes new modules in existing scenarios, new flyable drones, and an improvement to the controller mapping interface. And bug fixes, of course._

**New Features ✨**

* New Modules
  * Added new modules to the Tower Inspection scenario:
    * Free Fly
    * Free Fly - Monopole
    * Free Fly - Lattice
    * Free Fly - Guyed
* New Flyable Drones
  * Skydio X10
    * The Skydio X10 is billed as having the best array of sensors in its size-class, including a top of the line thermal camera. Fast and agile with a max flight time of 40 minutes, the X10 is an excellent drone for most situations.
  * DJI Avata 2
    * The DJI Avata 2 is a lighter, faster improvement on the first generation Avata. With a solid camera and excellent mobility, the Avata 2 is an excellent choice for cinematic and tracking shots.
* Input Curves
  * Customizable input curves are here! This is the full release of the preview feature from the previous patch.
  * An Input Curve profile changes how sensitive different analog inputs, such as flight and camera controls, are at various stages of input.
* New Controller Support
  * Added official profiles for the DJI FPV Remote Controller 3 on Windows and Mac
  * Added official profiles for a new revision of the FS-i6s

**Improvements** 🙌

* Scenario Updates
  * Flight Path Practice
    * Updated instruction text for clarity in some modules
* Controller Mapping
  * Added a UI popup to the Controller Mapping interface that indicates if a controller is not in its neutral state, allowing users to better remap inputs for controllers
  * Added "Flight Mode Switch" as a mappable field
  * Calibration and mapping data are now controller specific settings
* Drone Improvements
  * New flashlight functionality added to many existing drones
  * Loki max tilt angle adjusted to bring it more in-line with real world counterpart

**Bug Fixes 🐛**

* Fixed an issue causing a module timeout error on drone cash in certain circumstances
* Fixed a typo in the Spektrum Interlink DX controller profile
* Fixed an issue impacting the appropriate display of camera capture messaging
* Fixed an issue with the gimbal UI
* Fixed a graphical on The Island scenario impacting gutters on some buildings

Known Issues ❗

* Due to engine changes, users may experience a warning message the first time they log in to Zephyr after the update. This warning message is caused by changes to the grass system and will go away after the user changes their grass setting to a supported option.
* There is a graphical issue impacting the water on The Island scenario
