---
icon: rocket-launch
---

# Little Arms Launcher

## v0.12.6 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### August 13, 2025

_This update enhances the download and installation experience in preparation for the next simulator update in which scenarios will be split into DLC. Also includes some nice bug fixes and improvements that will hopefully mitigate common issues users experience._

**New Features** <i class="fa-sparkles">:sparkles:</i>

* New “Preparing” step added to app installation process, so you’ll know when the app is getting ready before the download begins.
* Improved drive selection feedback user experience when running the Little Arms Launcher for the first time.

**Bug Fixes** <i class="fa-bug">:bug:</i>

* Fixed an issue that could result in an app installation/update failure if certain folders utilized by the Little Arms Launcher didn't exist where usually expected.
* Fixed a case where setting the Little Arms Launcher's dedicated folder could fail unnecessarily if the source and destination happened to be the same.
* Resolved an issue that could cause certain URLs to be mishandled during downloads.

Performance and Security <i class="fa-lock">:lock:</i>

* Improved stability across installation, update, and drive-listing (on Windows) processes.
* Enhanced error handling for app installation catalogs, file cleanup, and app data management.
* Optimized logging for better diagnostics, including CPU details and launcher process tracking.

## v0.12.0 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### February 7, 2025

_This update introduces support for offline mode, remember me, command line arguments, native window login fallback option, and application version management._

**New Features ✨**

* Added the ability to register your device to run in offline mode if permitted.
* Added a "remember me" option (and a way to disable it)
* Added support for command line arguments for launching the launcher
* Added an option to enable "application version management" to the end user

**Improvements 🙌**

* Logging updates to better track and understand common launcher problems users have encountered

## v0.11.0 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### December 18, 2024 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

_This update introduces support for hardware licenses._

**New Features ✨**

* Added the ability to register your device and acquire a hardware license through a supported institution. Using the Little Arms Launcher with a valid hardware license grants access to its associated content, in addition to any content you currently have access to when running Zephyr.



## v0.10.3 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### December 3, 2024 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

_This update introduces social provider support and improvements to the launcher._

**New Features ✨**

* Initial support for SSO

**Improvements 🙌**

* Updated auth0 development domain

**Bug Fixes 🪲**

* Login issue that would result in erroneous error if a previous login attempt had been canceled



## v0.9.2 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### October 16, 2024 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

_This update is primarily a fix for list-drives functionality on macOS_

**Improvements 🙌**

* SCSS related dependency updates

**Bug Fixes 🪲**

* list-drives functionality on macOS where process could hand when using diskutil



## v0.9.0 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### August 20, 2024 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

_This update includes some bug fixes and improvements to the Launcher_

**Improvements 🙌**

* General project cleanup
* Updated node version to 18.18.0
* Updates listProcess errors to be more comprehensive
* Error log fetching and zip submission for reporting payload
* Addressables system updates
* Fallback functionality to app update process

**New Features ✨**

* New Dev Mode feature

**Bug Fixes 🪲**

* Partitions list from diskutil in list-drives
* App install issue related to DLC folder existence
* Logic issue with app update map creation
* URL generation for API requests
* Improper channel value being sent in API requests



## v0.8.62 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### January 10, 2024 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

_This update includes an update to user credential handling_

**Improvements 🙌**

* Modified the way user credentials are passed from the Launcher to apps that support auto login.



## v0.8.52

### July 11, 2023 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

_This update includes improvements and bug fixes_

**Improvements 🙌**

* Consolidated handling of listing processes into a list-process utility.

**Bug Fixes 🪲**

* Fixed issue where request for federated sign in from renderer would error due to the session data object being un-sendable through IPC.
* Added a fix for usage of (bundled) wmic utility that would previously result in its evocation failing when the absolute path to the wmic executable on the user's machine contained spaces.
* Now ensure that `ensureRequiredDirectories` is executed before the initialization window is shown (during initialization of the launcher) to ensure any warning dialog windows are not obscured behind the initialization window (which is set to always display on top of all other windows).



## v0.8.48

### July 6, 2023

_This update includes improvements and bug fixes_

**Improvements 🙌**

* Finished Vue3 migration
* Implemented new method of fetching app executable ProductVersion on Windows using powershell.
* Updated behavior of the \`list-drives\` service to include support for new method for macOS, as well as improved fallback handling.
* Streamlined aspects of information/error logging.
* Added preliminary recognition for when the user's machine suspends such as when it goes to sleep
* Changed compilation of Typescript from `babel-loader` to `ts-loader`
* Added `diskutil` method for listing drives.
* Added hard drive detection utility to development settings view
* Minor type-related updates and various other corrections to `src` content
* Streamlined aspects of project tooling
* Updated NodeJS to `v18.14.2`
* Made improvements to renderer error handling
* Various other minor improvements

**Bug Fixes 🪲**

* Minor bug fix for listing drives via powershell
* Prevent `Content-Type` header from automaticaly being set in requests if already explicitly declared in requerst parameters.
