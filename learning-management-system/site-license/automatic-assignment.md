---
description: Details about the site license auto assignment licensing method on Zephyr
---

# Automatic Assignment

This style of license assignment under a site license organization leaves it entirely up to the system to assign student licenses based on course start and end dates.

## Allocating & Revoking Licenses

Licenses are assigned to a student's account **when they accept their invite**.

Licenses are removed from a student's account **when the course ends.**

<details>

<summary><em>"What if I want to assign a license to a student outside of a course date?"</em></summary>

Under the automatic licensing method, license assignment is solely done by course dates.&#x20;

If you want to assign a license to students outside of normal course dates, then you would still need to create a course and set the start and end dates to the desired duration.

</details>

## Inviting Students

Because licensing is done automatically when a student accepts an invite, invites can only on the start date of a course.

You can still create invites any time before the course start date, they just won't be sent until their scheduled send date. So, in the example below, after we click "Invite," we can expect the course invites to be sent on 6/30/2025 at 2am (Local Time).

<figure><img src="../../.gitbook/assets/image (12).png" alt="" width="456"><figcaption><p>Invite Students to Auto Licensing Course</p></figcaption></figure>

### Welcome Email

Since we know there can be technical issues when registering and installing the simulator, we automatically send a welcome email to students 1 week before their course begins.

This email walks them through registering their account and instructs them to download and install the simulator and ensure it runs before their course begins.

Email Subject: \[Zephyr] Welcome Email and Preparations

Email Body:

<figure><img src="../../.gitbook/assets/image (13).png" alt="" width="563"><figcaption><p>Student Welcome Email</p></figcaption></figure>

## Managing Invites

You can always go to your Invites table under Manage > Invites on your Zephyr dashboard to view their status. Here you can see useful information like Status, Invite Expiration, Role/Course, and if a License Removal Date is set

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Invites Tables Automatic Licensing Organization</p></figcaption></figure>

## License Usage View & License Calculations

The most complicated portion of this system is license calculation. Our system will do everything possible to calculate license availability and prevent any license overuse. At any point in time, you can view your license usage by logging into your institution admin or instructor account and clicking the "View License Usage" button on the "Site License Usage" card.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>License Usage Overview</p></figcaption></figure>

You will be presented with a large calendar view.

#### Projected vs Historical Data

<figure><img src="../../.gitbook/assets/image (2).png" alt="" width="374"><figcaption><p>License Usage Legend</p></figcaption></figure>

We divide license usage data between projected and historical usage. Historical usage is a record of license usage from any previous day. This will show a breakdown of license usage on the specific day.

Projected usage is an anticipated estimate of license usage on the specific day given (a) any existing invitations and (b) any active licenses during that day.

In essence, anything in the future will be projected and anything in the past will be historical.

#### Navigation

<figure><img src="../../.gitbook/assets/image (3).png" alt="" width="230"><figcaption><p>License Usage Navigation</p></figcaption></figure>

Navigate through months/years by clicking the chevron arrow icons in the top right portion of the calendar view.

Click on a day to bring out the details sidebar on the right and view specific license usage on that day.

#### Sidebar (Daily Details)

<div align="center"><figure><img src="../../.gitbook/assets/image (4).png" alt="" width="375"><figcaption><p>License Usage Daily View</p></figcaption></figure></div>

With a day selected, if there are any courses, invites, and license usage projected on the day, it will populate the sidebar with total license usage at the top and a breakdown of student license usage per course on the given day.

Each student entry will either have an "email" icon or a green "checkmark" icon. An email icon indicates that an invite is sent or will be sent, but it has not been accepted. A green checkmark indicates that the student is currently registered and has a license assigned.

#### Available Actions

If you need to clean up any obsolete invitations or remove licenses, you can do so by clicking the red quick action buttons next to the student's entry. Completing one of these actions will free up a license to be used.

Note: clicking "Remove" here on a student entry removes them from the course _and_ removes the license from their account.

## Example

Say we have the following courses:

1. `Course A` that starts `6/1` and ends `6/20`
2. `Course B` that starts `6/16` and ends `6/28`

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Course Examples</p></figcaption></figure>

And our organization's `max student licenses` is `20`

Since these courses overlap, we can only have `20` students combined between the two courses. With our `max student licenses` at `20` , we cannot have more than 20 licensed students at any given time.

So, if we have invited `15` students to `Course A`, we can only invite `5` students to `Course B`.&#x20;

{% hint style="warning" %}
If you need more student licenses so that you can invite the students you need to a course, please contact your account manager or sales@littlearms.com
{% endhint %}

To continue the example, if today is May 15 and I'm preparing my courses, I can invite all 15 students to Course A and 5 students to course B. The invitations are created and viewable on the website dashboard in the invites table; however, they will not be sent to the students until the `course start date`. Students will also receive a welcome email 1 week before their course start date that will instruct them to register their account and install the simulator to ensure it works as expected before their course begins.

So, on May 25, students from Course A will receive their welcome emails. On June 1, they will receive their invitation emails. On June 9, students in Course B will receive their welcome emails. On June 16, they will receive their invitation emails.

{% hint style="warning" %}
Invitations created less than one week before the course start date will immediately result in a welcome email being sent. Invitation emails will still only be sent on the course start date

Invitations created after the course start date but before the course end date will immediately result in the invitation email being sent.
{% endhint %}

From June 1 - June 15, assuming all students register, the organization's student license usage will show as `15`. Then on June 16, assuming all student register that day, the organization's student license usage will show as `20`. Then on June 20th, Course A's students will have their licenses automatically removed. Depending on the time of day that the course ends, the organization's license usage might show `20` or `5`. Thereafter, the organization's license usage will show as `5` until Course B ends.

{% hint style="warning" %}
The time of day matters since our historical usage calculator runs once per day. Details can be found here: [#historical-license-usage](./#historical-license-usage "mention"). So, if a course ends before the calculator runs, license usage for that day will not include the licenses associated with that course.
{% endhint %}

## FAQs

<details>

<summary>"<em>I selected a course, but I don't have enough available licenses to invite the student I need"</em></summary>

You either need to request your student license limit to be increased, remove students from your organization, or verify that courses are not unintentionally overlapping and using more licenses than intended.

</details>

<details>

<summary>"<em>My available licenses is different now than it was an hour ago"</em></summary>

Available license projections can change based on a few factors: pending invitations get deleted, users get removed from an organization, courses end and licenses are automatically removed, etc.

</details>

<details>

<summary><em>"When do my student's licenses get removed?"</em></summary>

Every hour, our reconciliation function runs to two do things: (1) remove licenses from students where the license remove date has passed and (2) auto reject any outstanding invitations that have not been accepted for courses that have ended

</details>
