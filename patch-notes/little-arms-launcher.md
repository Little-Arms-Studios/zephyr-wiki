# 🦖 Little Arms Launcher

## 0.8.62 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### January 10, 2024 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

_This update includes an update to user credential handling_

**Improvements 🙌**

* Modified the way user credentials are passed from the Launcher to apps that support auto login.



## 0.8.52

### July 11, 2023 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>



**Bug Fixes 🪲**

* Fixed issue where request for federated sign in from renderer would error due to the session data object being un-sendable through IPC.
* Added a fix for usage of (bundled) wmic utility that would previously result in its evocation failing when the absolute path to the wmic executable on the user's machine contained spaces.
* Now ensure that `ensureRequiredDirectories` is executed before the initialization window is shown (during initialization of the launcher) to ensure any warning dialog windows are not obscured behind the initialization window (which is set to always display on top of all other windows).
* Consolidated handling of listing processes into a list-process utility.
