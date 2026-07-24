---
icon: drone
---

# Zephyr

## v1.11.10

### July 22, 2026

This release contains several major bug fixes as well as multiple under-the-hood improvements.

#### **New Features**

* New Controller Support
  * Added support for the Futaba T6K and WSC-1 USB adapter

#### **Improvements**

* Updated performance specs of and removed camera zoom from the Brinc Lemur 2 to bring it more in line with its real-world counterpart
* Enabled banking for the flight physics for the Brinc Lemur 2
* Optimized 3D models in several scenes to improve sim performance
* Updated objective text in modules in the Beach scenario for clarity
* Updated the code for rotation and target objectives for better measurement and control
* Tweaked thermal imaging visuals to bring down the intensity of image "ghosting"
* Thermal imaging pass on additional objects throughout the sim
* Adjusted placement and density of foliage in the SAR Mountain scenario
* Removed camera zoom from Bring Lemur 2
* Updated objective number text to better fit in the objective list
* Removed deprecated mobile controller functionality from the sim

#### **Bug Fixes**

* Fixed an issue where the simulator would be set to an unsupported resolution by default
* Fixed an issue where audio settings set in the Main Menu were not respected in most scenarios
* Fixed an issue causing certain drones to explode on spawn in some scenarios
* Fixed an issue with some drones wobbling on spawn in the Warehouse scenario
* Fixed an issue impacting some capture targets in the Beach scenario
* Fixed a text display issue in the Thermal View Select dropdown menu
* Fixed an issue where certain capture targets in SAR Fundamentals were not highlighting
* Fixed an issue where certain capture targets in SAR Fundamentals were not capturing
* Fixed an issue where some objective UI elements would not clear after completion in SAR Fundamentals

#### **Known Issues**

* If your previously saved resolution is not compatible with Zephyr after this fix, your Zephyr may launch in Windowed mode. You can change it to your desired mode and supported resolution by navigating in Zephyr to Main Menu > Settings.
* Graphical issue impacting certain textures in the Yard scenario
* Audio chatter does not respect the master audio slider in certain scenarios
