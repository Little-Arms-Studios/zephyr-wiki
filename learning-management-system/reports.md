---
icon: file-lines
---

# Reports

Flight reports are saved after each module is completed. Each user can access their own reports; however, some users, like admins and instructors, can access the reports of users at their organization.

To view reports:

1. Sign in to your Zephyr account at [zephyr-sim.com](https://zephyr-sim.com/)
2. Click "REPORTS" on the lefthand menu

{% hint style="info" %}
You can only view the Reports of one user at a time. If you need to view an aggregated report of multiple user reports, please see the [Request Report](reports.md#request-report) section
{% endhint %}

## Using the Reports Page

<figure><img src="../.gitbook/assets/image (361).png" alt="Reports Page"><figcaption></figcaption></figure>

### Selecting a User

Ultimately, the "User" field is what will load reports in the table at the bottom of the page. You can filter the user selection by course by selecting a course from the "Filter Users by Course" dropdown.

When you're ready to select a single user, click the "Select a user" field and either click on the user in the list in the flyout menu or search for their name/email in the search field in the flyout menu and click the resulting user.

<figure><img src="../.gitbook/assets/image (362).png" alt="Select a User on Reports Page" width="428"><figcaption></figcaption></figure>

Once a user is selected, a default range of reports will be loaded into the reports table below.

<figure><img src="../.gitbook/assets/image (363).png" alt="Reports Page with User Selected"><figcaption></figcaption></figure>

### Report Filters

You can filter reports using the following fields:

1. Scene
2. Module
3. Additional Filters:
   1. Show Reports for the Current Institution Only \[Note: only visible if you selected yourself]
   2. Show Reports with Score of "0"
   3. Show Uncompleted Reports
   4. Show Highest Score for Each Module (this will only return one report for each module)
4. Start Date and End Date (defaults to one month)

### Viewing Report

For each report in the table, you can click the "View" button to view the details of the report.

Depending on the module, the report details may include more or less information. For example, the NIST Test modules will include a breakdown of each objective in a table at the top of the View Report modal.

#### NIST Test Report Example

<figure><img src="../.gitbook/assets/image (366).png" alt="NIST Test Report Example and Details"><figcaption></figcaption></figure>

#### View Report Details

The top of the report will include the following meta information: **User, Scene, Module, Date/Time of Report, and Score.**

**Main Report Details** include:

* **User**
* **Organization Name (if applicable)**
* **Drone Name**
* **Date**
* **Scene/Module**
* **Score/Possible Score**
* **Score Percent (if applicable)**
* **Grade (if applicable)**
* **Reset and Crash Count**
* **Start, End, and Total Time**
* **Average, Max Altitutde**
* **Average, Top Speed**
* **Violations (altitude and line of sight)**

**Objective Details**

Each module consists of objectives that contribute to the user's total score. Here you can click on each objective to view details on how it was completed or failed.

## Request Report

As an Admin or Instructor, you can click the "Request Report" button on the REPORTS page to generate a CSV that will be emailed to you.

The Report Request modal looks like this

<figure><img src="../.gitbook/assets/image (367).png" alt="Report Request Part 1" width="451"><figcaption></figcaption></figure>

1. Enter the email that you want the Report Request sent to (by default this will be your account email)
2. Click the "Pencil" icon under the Users section to summon the "Select Users" modal

<figure><img src="../.gitbook/assets/image (368).png" alt="Select Users modal"><figcaption></figcaption></figure>

3. Optional: Filter the "Options" column by selecting a "Course" on the lefthand side
4. Click on the users in the "Options" column that you'd like to include in the report and they will move to the "Selection" column
   1. Alternatively, you can click "Add All" if you want all of the current users in the "Options" column to be included
5. Click "Apply"
6.  You will be brought back to the main "Report Request" modal where the "Users" number should be updated to reflect your selection (i.e. if you selected 3 users, you should see 3 / X in the Users section)

    <figure><img src="../.gitbook/assets/image (370).png" alt="Users Selected" width="390"><figcaption></figcaption></figure>

    1. You can verify your selected users by clicking the "Eye" icon to show/hide the list of selected users
7. Select a Date Range for the reports you'd like to be included in the Report
8. **Filtration Options**
   1. Module Completion: you can specify if you want only completed, only incomplete, or all completion types to be included in the report
      1. A module is "incomplete" if it's ended early by the user or if a crash results in the module to be ended automatically.
   2. Highest Score Only: if this is toggled "On" it will only include one report for each module for each user. This report will be the user's highest score for the given module
   3. Modules: select which modules should be included in the report
      1. Similar to the Users selection from step 2, click the "Pencil" icon to summon the Module picker window.
      2. Click on the modules you'd like to include in the report and they will move to the "Selection" column
      3. Click "Accept" when you're happy with your selection
      4. You will be brough back to the main "Report Request" modal where the "Modules" number should be updated to reflect your selection (i.e. if you selected 20 modules, you should see 20 / X in the Modules section)
      5. You can verify your selected modules by clicking the "Eye" icon to show/hide the list of modules
9.  **Included Information**



    <figure><img src="../.gitbook/assets/Screenshot 2026-05-15 at 10.43.21 AM.png" alt="Included Information" width="453"><figcaption></figcaption></figure>

    1. This section pertains to the columns that will be included in the report. Toggle on each section that you would like to be included in the final report (conveniently, you can select All/None at the top of this section)
10. **Report Data Agreement**
    1. Finally, you must acknowledge that once the report data leaves the Zephyr system, Zephyr and Little Arms Studios are no longer responsible for the security of that data
    2. Toggle this "On" if you agree
11. Click "Send"

A notice will appear letting you know that your request is processing and you should expect an email once it finishes.

{% hint style="info" %}
Depending on your selection, the processing time may vary. If you haven't received an email with the report after 10 minutes, please email support@littlearms.com
{% endhint %}

