# Site License System Updates

June XX, 2025

## What's changing?

The Site License system was a major improvement and heavily requested over our legacy licensing/seat system; however, it was created as a minimally viable product with the intention to expand and improve its functionality as time went on and feedback was given.

Changes overview:

1. \[All Instructors and Institution Admins] [**Course Start and End Dates Require a Time**](site-license-system-updates.md#course-start-and-end-dates-require-a-time)
2. \[Site License Organizations Only] [**Students licenses are tracked and managed separately from Instructor and Institution Admin licenses**](site-license-system-updates.md#student-vs-instructor-vs-institution-admin-licenses)
3. \[Site License Organizations Only] [**Instructors Can Assign Licenses**](site-license-system-updates.md#instructors-can-assign-license)
4. \[Site License Organizations Only] [**Site License Automatic Assignment (In Beta. Official Release Date TBD)**](site-license-system-updates.md#site-license-automatic-assignment)

## **Why the change?**

It's been heavily requested that we introduce automatic licensing assignment to students and it's been something we've been working on for a while. Quite frankly, it's long overdue. We appreciate all of our partners and users' patience and understanding while working within the current system and we hope this change reduces a lot of the confusion and legwork involved with simply getting your students access to the simulator.

Separating student vs instructor vs institution admin license pools is a necessary step towards our ultimate goal of this release: automatic license assignment.

## What do I have to do?

At the moment, nothing! Just familiarize yourself with the new Site License Manual Assignment updates here: [Broken link](broken-reference "mention").

## When is this update happening?

The initial update that divides license pools by roles at an organization will release on **June XX, 2025.**

Site License Automatic Assignment will officially release once we finalize our Beta test. Release date TBD, listen out for another announcement when that's officially ready.

## How can I beta test?

Contact your Account Manager or sales@littlearms.com and tell them you are interested in testing the Site License Automatic Assignment system.

***

### **Course Start and End Dates Require a Time**

Since we are scheduling automations on course dates, it's paramount that we get as exact as possible so that there's no confusion around when things are happening. For instance, if we are removing licenses from students at automatic site licensing organizations when their course ends, we know exactly when students can expect to lose access to the simulator.&#x20;

This also allows users to be explicit when creating a course and factoring in any time zone differences between the instructors and students of a course.

<figure><img src="../../../.gitbook/assets/image.png" alt="" width="375"><figcaption><p>Create Course Window</p></figcaption></figure>

### **Student vs Instructor vs Institution Admin Licenses**

Currently, all site licenses are pooled and distributed together at an organization regardless of role. This was an initial flaw in our design since Student licenses are functionally different than Instructor/Institution Admin licenses at a site license organization.

This updated will separate those pools so that they can be managed independently as they should have been from the start. This separation not only clarifies billing concerns, but allowed us to create the automatic assignment feature outlined below.

<figure><img src="../../../.gitbook/assets/image (1).png" alt="" width="375"><figcaption><p>Site License Usage</p></figcaption></figure>

### **Instructors Can Assign Licenses**

Initially we were cautious about giving instructors the ability to assign and remove licenses from users; however, through testing and feedback it's clear that it would make instructors' lives much easier if they had the ability to assign licenses instead of reaching out to their institution admins. This is a small change that removes a very long step in the student licensing process.

### **Site License Automatic Assignment**

{% hint style="warning" %}
Official Release Date TBD. Private Beta Only
{% endhint %}

The biggest headache with the current system is the assigning and removing of licenses to users. For a new student, the process goes:

1. Instructor creates a course
2. Instructor invites student to a course
3. Student registers and accepts invite to a course
4. Instructor notifies Institution Admin that Student registered and accepted their invite and are ready for a license
5. Institution Admin assigns license to Student

That was entirely too many steps to simply assign a license to a student.

It has been heavily requested that a student simply gets a license assigned to their account when they accept the invite. It's been a very complicated journey to get here, but this feature will allow organizations to do just that.

Details about this change can be found here: [Broken link](broken-reference "mention")

