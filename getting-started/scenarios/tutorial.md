---
description: >-
  Learn everything you need to get started with Zephyr. Whether you are brand
  new to the simulator or an experienced operator looking for a refresher, this
  scenario is the best place to get started.
cover: ../../.gitbook/assets/image (52).png
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 🏀 Tutorial

## Introduction

The Tutorial scenario consists of four modules that walk users through the basics of using Zephyr, from controlling a drone to completing module objectives. The four modules are:

1. Drone Power and Basic Control
2. Guide Drone, Flight Modes, and Control Modes
3. Camera Controls
4. Objectives

<figure><img src="../../.gitbook/assets/image (21) (1) (1).png" alt=""><figcaption><p>Screenshot of the Module Selection Screen for the Tutorial Scenario</p></figcaption></figure>

## Drone Roster

For ease of use and simplicity, each module in the Tutorial scenario uses the DJI Phantom 4.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1).png" alt=""><figcaption><p>Screenshot of the Drone Selection for the Tutorial Scenario</p></figcaption></figure>

## Module Breakdowns

### Drone Power and Basic Controls

To power on the drone, move the sticks on your controller or press the corresponding keyboard keys into the positions shown on the screen and hold that position for two seconds.

<figure><img src="../../.gitbook/assets/image (14) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To increase the drone's altitude, press up on the `Left Stick` or `W` on the keyboard to throttle up.  Increase altitude until your drone reaches the purple box.

<figure><img src="../../.gitbook/assets/image (15) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To decrease the drone's altitude, press down on the `Left Stick` or `S` on the keyboard to throttle down. Decrease altitude until your drone reaches the purple box.

<figure><img src="../../.gitbook/assets/image (16) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Rotation around the vertical axis of a drone is called "yaw". To change the yaw of the drone, hold the `Left Stick` right or left, or hold `A` or `D` on the keyboard.

Complete three full rotations to complete this objective.

<figure><img src="../../.gitbook/assets/image (17) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Rotation around the horizontal left-to-right axis is known as "pitch". To change the pitch of the drone, hold the `Right Stick` up or down, or hold the `Up` or `Down` arrow keys on the keyboard.

To complete this objective, pitch the drone forward so it moves to the purple box, and then pitch the drone backwards so it moves to the second purple box.

<figure><img src="../../.gitbook/assets/image (18) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
In most flight modes, the drone will move relative to the direction it is facing, _not_ the way the user is facing.  If the operator changes the pitch, the drone will move forward or backward relative to itself, as seen in the bottom right corner (Drone Camera).
{% endhint %}

Use a combination of yaw and pitch to pilot your drone into the purple boxes.

<figure><img src="../../.gitbook/assets/image (19) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Rotation around the horizontal forward-to-backward axis is known as roll. To change the roll of the drone, hold the `Right Stick` left or right, or hold the `Right` or `Left` arrow keys on the keyboard.

Complete the objective by using roll to move your drone into both of the purple boxes.

<figure><img src="../../.gitbook/assets/image (20) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (21) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Complete this objective by using a combination of yaw and roll to pilot your drone into the purple boxes.

<figure><img src="../../.gitbook/assets/image (22) (1) (1).png" alt=""><figcaption></figcaption></figure>

Congratulations! You know understand the basics of piloting a drone in Zephyr. Please spend some time trying out the full range of controls.

### Guide Drone, Flight Modes, and Control Modes

#### Guide Drone

"Guide Drone" is a large overlay that shows the orientation of the drone even when far away or obscured by an object, allowing users better control of the drone. "Guide Drone" can be toggled on or off with `Left Shift` on the keyboard.

<figure><img src="../../.gitbook/assets/image (23) (1) (1).png" alt=""><figcaption></figcaption></figure>

Use the Guide Drone to help you pilot the drone to the two purple boxes.

#### GPS Mode

{% hint style="info" %}
To switch Flight Modes, press `F1` on the keyboard
{% endhint %}

In GPS Mode, the drone will automatically adjust itself to maintain its position in space when the operator stops giving input.

<figure><img src="../../.gitbook/assets/image (24) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Attitude Mode (ATTI)

{% hint style="info" %}
To switch Flight Modes, press `F1` on the keyboard
{% endhint %}

In ATTI mode, the drone has no positional stabilization, so it tends to drift after the operator stops giving input.

<figure><img src="../../.gitbook/assets/image (25) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
To switch Control Modes, press `F2` on the keyboard
{% endhint %}

{% hint style="warning" %}
Not all Control Modes are available on all drones in Zephyr
{% endhint %}

#### CourseLock Mode

While a drone is in CourseLock Mode, its forward direction when it entered CourseLock will remain its forward direction while CourseLock is active. This means the same input will always move the drone in the same direction, regardless of its current yaw.

#### HomeLock Mode

When a drone enters HomeLock Mode, the geographical point the drone was located at becomes its "home point". This means horizonal input causes the drone to circle its home point.

### Camera Controls

{% hint style="warning" %}
Not all drones in Zephyr have the ability to move their cameras up and down
{% endhint %}

To switch cameras, press the corresponding button on your controller (often the left button on the rear of the controller) or `Spacebar` on the keyboard.

<figure><img src="../../.gitbook/assets/image (26) (1) (1).png" alt=""><figcaption></figcaption></figure>

To pitch the drone camera up and down, use the corresponding inputs on your controller (often should dials) or press the `Home` and `End` keys on the keyboard.

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

### Objectives

#### Path Objective

With a Path objective, the drone must enter the objective cubes in the correct order - a "path".

Follow the path objective cubes in sequence from left to right.  A circular indicator will appear in the correct blue cube and begin to fill as the drone approaches it.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Zone Objective

With a Zone objective, you must pilot the drone into the objective cube and remain within the cube until the objective completes.  For this specific objective, the drone needs to remain in the objective cube for five seconds.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Zone objectives may also appear as brackets or rings.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Target Objective

With a Target objective, you must pilot the drone into a Zone objective cube and then "capture" and object using the drone's camera.

Begin by piloting the drone into the Zone objective.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Once inside the Zone objective, a reticle will appear on the drone's camera. Aim the drones camera at the soccer ball in the middle of the gym.

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Once the drone camera is correctly aimed the soccer ball, the target objective will begin to fill. Keep the target centered in the reticle until the objective completes.

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Landing Objective

With a Landing objective, you must land the drone in a designated area.  For this specific objective, the drone needs to remain in the objective cube for five seconds.

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Pilot the drone over the objective, and then lower the drone to the ground.

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Continue to hold down on altitude (`Left Stick` down or `W` on the keyboard by default) to power down the drone.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Not all Landing objectives require the drone to be powered off in order to be completed.
{% endhint %}
