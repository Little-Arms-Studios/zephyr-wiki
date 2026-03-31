# Zephyr SIM Performance Issues

Zephyr Versions 1.10.5 and 1.10.7 have some known performance issues and may require some users to rollback to a previously performant version until we can solve the issues in a later update.\
&#x20;\
Some computers that are at or below or minimum requirements ([https://wiki.zephyr-sim.com/system-requirements](https://wiki.zephyr-sim.com/system-requirements)) that cannot achieve >30FPS (frames per second) will experience a "drone wobble". This may result in the drone shaking and moving on its own without any input in the controller.\
&#x20;\
There's two steps to solve the issue for the time being:

1. Try to reduce graphics settings to achieve a higher FPS
2. Rollback to a previously performant version

&#x20;\
**Reduce Graphics Settings**\
Try navigating to Main Menu -> Settings and adjusting your Graphics Settings to the following:

1. Resolution -> Lower to an acceptable resolution
2. Weather System -> Off
3. Grass System -> Off
4. Graphic Quality -> Fastest

&#x20;\
**Rollback to previous performant version**\
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



The next update will aim to alleviate this issue; however, running the simulator at less than 30FPS is never recommended.
