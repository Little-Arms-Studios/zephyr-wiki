---
icon: globe-pointer
---

# Zephyr Dashboard

## v2026.1.3

### May 27, 2026

### Highlights

This release improves admin workflows on dashboards and in user management: shared utility buttons (including wiki links), a simulator time column on the Users table, and a more reliable Select Users and Report Request experience.

***

### New features

#### Dashboard utility buttons

* Introduced a shared Utility card pattern via `DashboardUtilityButtons` and `useUtilityButtons`, supporting both in-app actions and external wiki links (with an external-link icon).
* Institution Admin and Instructor dashboards now include an Organization Onboarding Documentation link to the wiki.
* Instructor utility section updated to match Institution Admin styling (labeled card, outline pill buttons, wrapped layout).

#### Users table

* Added Sim Time (hh:mm:ss) column showing each user’s simulator time, formatted as hours:minutes:seconds.

***

### Improvements

#### Select Users modal

* Search users by first name, last name, or email while picking recipients.
* Selection is preserved when changing organization/course filters or updating the search query.

#### Report Request modal

* Modal opens at large size for easier use.
* Start and End dates use the shared date/time picker with sensible bounds (up to 5 years back; end date cannot be in the future).
* Default range: start date is one month ago at midnight; end date defaults to today.
