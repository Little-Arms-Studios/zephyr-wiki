# 🪽 Zephyr

## v1.8.171

### April 15, 2024

_This update includes a new flyable drone, new UI features, and a multitude of bug fixes._

**New Features ✨**

* Gimbal Crosshair
  * Added a Gimbal Crosshair as a togglabe UI element.  It is disabled by default and can be enabled from the Settings Menu
* New Flyable Drones
  * Skydio X2D
    * The rugged and portable X2D was designed with reconnaissance in mind.  This impressive camera ensamble and 35 minutes of flight time make the X2D a desireable option for inspection and patrol tasks.
* Thermal Vision (Preview)
  * Thermal  Vision drone camera view is now available as a feature preview.  Toggling thermal vision is mapped to `CTRL + T` by default

**Improvements** 🙌

* Scenario Updates
  * Updated the drone rostsrs of modules sim-wide

**Bug Fixes 🪲**

* Fixed an issue impacting controller mapping where attempting to remap certain commands would freeze the simulator
* Fixed an issue impacting Xbox One controller usage on Mac systems
* Fixed lighting in the Bridge Inspection scenario
* Fixed issue where controller UI could disappear
* Fixed an issue with the description for the Autel Evo II
* Fixed a lighting issue in all scenarios causing discrepancies between weather and non-weather
* Fixed missing collision on ceiling windows in Warehouse

## v1.8.155

### January 19, 2024 <a href="#id-1.8.55-january-19-2024" id="id-1.8.55-january-19-2024"></a>

_This hotfix addresses a bug that appeared after the 1.8.54 update._

**Bug Fixes 🪲**

* Fixed an issue preventing some users from logging in to Zephyr.



## v1.8.154

### January 18, 2024 <a href="#id-1.8.54-january-18-2024" id="id-1.8.54-january-18-2024"></a>

_This update includes a rework to the Tutorial scenario, a new flyable drone, and multiple squashed bugs._

**New Features ✨**

* Updated Scenarios
  * Tutorial
    * We split the Tutorial scenario into four smaller modules instead of one enormous module. This greatly improved performance and will allow users to access desired sections of the tutorial quicker.
    * We updated the environmental art of the tutorial, switching from an empty void to a furnished gymnasium. Even if you completed the original tutorial before, it is worth checking out the new flyable area.
    * We updated the scenario and module selection art to reflect the environmental art changes.
* New Flyable Drones
  * DJI Matrice 30
    * The Matrice 30 from DJI is respected and trusted commercial drone model. Portable, rugged, and powerful, the Matrice 30 (M30) has nearly as many use cases as it does users.
* New Authorization System
  * Integrated Zephyr’s authorization system with new authorization system featured on the Zephyr website.

**Bug Fixes 🪲**

* Fixed an issue preventing modules in the Kids with Drones scenario from launching.
* Fixed an issue with the implementation of the DJI Matrice.
* Fixed an issue where Signal Feed Loss modules in the Tower Inspection scenario were not functioning properly.



## v1.8.138

### October 04, 2023 <a href="#id-1.8.138-october-04-2023" id="id-1.8.138-october-04-2023"></a>

_This update includes several bug fixes._

**Bug Fixes 🪲**

* Fixed an issue where the gimbal was unresponsive on the Skydio 2.
* Fixed several configuration issues with the Skydio 2 and Autel Evo 2 that caused the drones to perform below real world performance.
* Fixed several issues with the Tower Inspection scenario.
* Fixed an issue where grass would clip through landing pads in certain modules.

