# Simulator Performance Issues

March 13, 2026

## Overview

There's a current issue that we are trying to solve in the next release (we solved it a little bit from 1.10.5 to 1.10.7, but it's still present on some lower end machines).\
&#x20;\
In other words, some machines that are at or below or minimum requirements ([https://wiki.zephyr-sim.com/system-requirements](https://wiki.zephyr-sim.com/system-requirements)) that cannot achieve >30FPS (frames per second) will experience a **drone wobble** (the drone will shake or wobble on its own without any input from the user and possibly crash itself).

## Fixes

There's two steps to solve the issue for the time being:

1. Try closing other applications that are utilizing RAM and CPU resources
2. Try to **reduce graphics settings** to achieve a higher FPS
3. **Rollback to a previously performant version**

### (Option 1) Try closing other applications

If you have other applications that utilize a good amount of your RAM and CPU this can impact the performance of the simulator.

Examples of RAM and CPU-demanding applications are:

* Browsers with many tabs open (this can utilize a considerable amount of RAM especially if many of them are "active" tabs). Try closing the browser or any tabs that are not necessary
* Photo and video editing applications
* Video games

You can view what applications are using what resources by:

* Windows:
  * Press Ctrl + Shift + Esc to bring up the Task Manager
  * Click on the "Processes" tab
  * You can sort the column by CPU or Memory usage to find the applications that are utilizing the most resources
* Mac:
  * Press Command + Space and type in "Activity Monitor" and press Enter
  * This will open a window that shows active applications and their resource usage
  * You can view the CPU and Memory tabs respectively to identify other applications that are using resources

### (Option 2) Reduce Graphics Settings

Try navigating to Main Menu -> Settings and adjusting your Graphics Settings to the following:

1. Resolution -> Lower to an acceptable resolution
2. Weather System -> Off
3. Grass System -> Off
4. Graphic Quality -> Fastest

Try these settings to see if your computer can run the simulator at a higher FPS.

### (Option 3) Rollback to previous performant version

If nothing above solves your issue, you may want to roll back to a previously performant version of Zephyr (details below) To rollback to a previous version of Zephyr:

1. Open the Little Arms Launcher and login
2. On the Zephyr page, click the three dots icon
3. Click "App Settings"
4. Toggle "Enable selective version management" to "ON" (the toggle should be positioned to the right)
5. Click "Back" to go back to the Zephyr page
6. Click the downward arrow on the green button
7. Hover over "Revert to"
8. Click on "Version 1.8.171"
9. Let the Launcher revert
10. Click "Launch Current Version" below the green button when it become available

We sincerely apologize for the inconvenience and are actively working on solutions to make the simulator more performant for the majority of users.

If you have any questions or issues you can always reach out to support@littlearms.com and we will assist you to the best of our ability.

Sincerely,

The Zephyr Team
