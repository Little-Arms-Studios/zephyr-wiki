# 🦖 Little Arms Launcher

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
