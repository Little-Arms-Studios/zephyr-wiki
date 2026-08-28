---
icon: rocket-launch
---

# Little Arms Launcher

## v0.12.11 <a href="#id-0.8.62-january-10-2024" id="id-0.8.62-january-10-2024"></a>

### August 28, 2026

### Bug Fixes

* **Windows device ID generation** — Fixed an issue where the Launcher could fail to read the machine identifier on Windows. The Launcher now reads `MachineGuid` directly from the registry via `registry-js`, with a fallback for mixed-architecture processes.

### Improvements

* **macOS disk image mounting** — App installs from `.dmg` files on macOS 13 and later now use `diskutil image attach` instead of the deprecated `hdiutil mount` command, improving compatibility with newer macOS versions. macOS 12 and earlier continue to use `hdiutil`.
* **Startup memory reporting** — The Launcher startup log now reports **available memory** rather than free memory, using platform-specific metrics that better match what you see in Activity Monitor on Mac.
