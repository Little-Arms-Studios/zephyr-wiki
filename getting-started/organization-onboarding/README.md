---
icon: school
---

# Organization Onboarding

Thank you for entrusting us with your drone training needs! This guide will serve to help you through the Learning Management System (LMS), the Little Arms Launcher, the Zephyr Simulator, and how they all work to orchestrate the most effective and powerful drone training platform.

## QuickStart

Below is our video series about the LMS and Little Arms Launcher

* [How To: Installing and Running the Launcher Patcher and Zephyr Drone Simulator](https://youtu.be/hbDNAxIS5HE)
* [How To: Zephyr Drone Simulator's Learning Management System (LMS)](https://youtu.be/THFozU5N-hc)
* [How To: Student LMS Walkthrough](https://youtu.be/f6n1kDLw9Wg)

{% hint style="info" %}
For IT Departments: [it-departments](it-departments/ "mention")
{% endhint %}

## Overview

Enterprise accounts are managed through Organizations. Organizations have the following types of users: Admins, Instructors and Students.

* Admins: handle billing and inviting instructors (plus everything instructors can do)
* Instructors: managing courses, assignments, inviting students, and reporting
* Students: belong to a course and can view their assignments, progress, and flight reports&#x20;

All of the above is managed through the LMS at [zephyr-sim.com](https://zephyr-sim.com/).&#x20;

Once users have accounts created, they can access the simulator by downloading and installing the Little Arms Launcher. Then installing Zephyr through the Launcher. Details can be found here: [installation](../little-arms-launcher/installation/ "mention")

{% hint style="warning" %}
If your IT department needs to install and distribute the simulator to computers, please refer to this documentation: [it-departments](it-departments/ "mention")
{% endhint %}

## Getting Started

### Managing Licenses

As the Admin, once you've created your account and accepted your Admin invite to the new organization, the next step is to ensure you have the correct, expected number of licenses. Do this by looking at the "SITE LICENSE USAGE" card on your dashboard.

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-14 at 1.20.35 PM.png" alt="Site License Usage Card"><figcaption></figcaption></figure>

Based on your [Site License ](../../learning-management-system/site-license/)billing type ([manual](../../learning-management-system/site-license/manual-assignment.md) vs [automatic](../../learning-management-system/site-license/automatic-assignment.md)), your card may or may not have the "Assign" button shown in the picture above. If you have the "manual" license type, you will see the button. If you have the "automatic" license type, you will not see the button. Please review the documentation based on your license type to understand how assigning licenses to Students works.

### Managing Users

#### Inviting Admins/Instructors

As the Admin, you may have other Instructors that need to be invited to the organization. To get to the Invite Users modal, you have two options:

**Option 1**

1. From your dashboard on zephyr-sim.com, click "Invite Admin/Instructor" on the "USERS" card

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-14 at 1.30.24 PM.png" alt="Users Dashboard Card" width="288"><figcaption></figcaption></figure>

**Option 2**

Alternatively, you can invite users through the MANAGE / USERS table:

1. From your dashboard on zephyr-sim.com, click "MANAGE" on the lefthand side of the screen
2. Expand the "USERS" table
3. Click the three dot icon next to the search field
4. Select "Invite Admin/Instructors(s)"

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-14 at 1.28.22 PM.png" alt="Invite Users Dropdown on Users Table"><figcaption></figcaption></figure>

Once you've summoned the Invite Users modal, select "Instructor" or "Admin". Once selected, you will see how many licenses you have available to assign to the chosen user role.

{% hint style="info" %}
If you need more Admin or Instructor licenses, please contact your account manager or support@littlearms.com&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-14 at 1.32.02 PM.png" alt="Invite Users Modal" width="453"><figcaption></figcaption></figure>

Enter the email(s) of the people you need to invite (pressing "Enter" or clicking "Add" after each one)

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-14 at 1.35.45 PM.png" alt="Enter Emails to Invite"><figcaption></figcaption></figure>

Click "Invite" when you are finished. Email invitations will be sent to those users. They will need to (a) register their Zephyr account and (b) accept the invite on their dashboard that should appear in a blue banner when they sign in.

#### Inviting Students

Students need to be invited to a Course. If you have not yet created a Course, please see the "[Managing Courses](./#managing-courses)" section below.

Just like inviting Admins and Instructors, you have two options to summon the Invite Student(s) modal

**Option 1**

1. From your dashboard on zephyr-sim.com, click "Invite Student" on the "USERS" card

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-14 at 1.30.24 PM.png" alt="Users Dashboard Card" width="288"><figcaption></figcaption></figure>

**Option 2**

Alternatively, you can invite users through the MANAGE / USERS table:

1. From your dashboard on zephyr-sim.com, click "MANAGE" on the lefthand side of the screen
2. Expand the "USERS" table
3. Click the three dot icon next to the search field
4. Select "Invite Student(s)"

<figure><img src="../../.gitbook/assets/image (359).png" alt="Invite Students Option on Users Table"><figcaption></figcaption></figure>

Depending on your Site License type (manual vs automatic), your Invite Student(s) modal will look different.

#### Manual Site License - Invite Student(s) Modal

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-14 at 1.43.35 PM.png" alt="Invite Students Modal for Manual Site License Organization"><figcaption></figcaption></figure>

Manual Site License organizations' modal will look like the image above. We'll highlight each field and its functionality below.

**Course:** you must select a course to invite the student(s) to. Note: only **active** and **future** courses will be available to select. If an option is disabled it's because the course has already ended

**Emails**: enter the email(s) of the student(s) you would like to invite to the course. Press "Enter" or click "Add" after each email. Alternatively, if you have a list of emails separated by commas, semicolons, or spaces you can copy and paste them into this field then press "Enter".

**Send Invites:** You have two options: **Send Immediately** or **Choose a Date.** Note: if the course has already started, your only option is to send the invites immediately. Otherwise, if you'd like to schedule the invites to be sent out at a later date, you can select "Choose a Date" and a date/time picker will appear below.

<figure><img src="../../.gitbook/assets/image (360).png" alt="Date Time Picker for Invite Students Modal"><figcaption></figcaption></figure>

Once you've clicked "Invite", students will receive an email notification of their invite based on your "Send Invites" option selected.

#### Automatic Site License - Invite Student(s) Modal

Please see [#automatice-site-license-invite-student-s-modal](./#automatice-site-license-invite-student-s-modal "mention") for a comprehensive walkthrough.

### Managing Courses

Please see [courses.md](../../learning-management-system/courses.md "mention") for details.

### Managing Assignments

Please see [assignments.md](../../learning-management-system/assignments.md "mention") for details.

### Flight Reports

Please see [reports.md](../../learning-management-system/reports.md "mention") for details.

## Conclusion

If you have any questions, issues, or feedback, please reach out to your account manager or start a support case by visiting [https://support.zephyr-sim.com/](https://support.zephyr-sim.com/).
