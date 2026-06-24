---
icon: globe-pointer
---

# Zephyr Dashboard

## v2026.2.2

### June 24, 2026

### Highlights

* Student license visibility — Site license usage now splits student licenses into assigned vs. pending invites across the dashboard, license overview modal, and site license card, with a color-coded progress bar and legend (Site License: Auto organizations only).
* Purchase wizard improvements — Enterprise email visitors and organization purchasers get clearer flows, including organization details on the review step, improved pricing logic, and form path included on the submission.
* Industry pages streamlined — “Talk to sales” and “Request a demo” CTAs across industry pages now route directly to the purchase wizard via “Get started.”
* License usage calendar overhaul — More reliable date handling, smarter data fetching, and clearer day-vs.-organization usage display in the calendar widget.

***

### New Features

#### License management

* Added `site-license-breakdown` service to compute assigned student licenses vs. pending invite slots for auto-licensed organizations.
* CardSiteLicenses shows a stacked progress bar (assigned + pending invites) with legend and tooltip explaining how pending invites are inferred (Site License: Auto organizations only).
* License Usage Overview modal displays pending invite counts for current license holders and loads list content on demand when switching views.
* Institution Admin and Instructor dashboards pass student license breakdown data to the site license card.

#### Purchase wizard

* Enterprise/special-email visitors who choose contact sales now complete the organization step before review, with organization summary and pricing on the review screen.
* Organization pilot count is required for purchase pricing; invalid values surface a clear error instead of defaulting to 1.
* Review step messaging tailored for special-email sales lead submissions.

#### Marketing & navigation

* Added Omada as a proud partner; reordered partner logos (SCIDUC, Omada, USI).
* Industry pages (Agriculture, Construction, Drone Training Schools, Energy & Utilities, Logistics, Public Safety, Real Estate & Media) link to the purchase wizard.
* Legacy `/pricing` route redirects to `/enterprise` while preserving query params and hash.

#### Shop

* Scene-linked shop visits show an informational alert when a scenario may not be available for individual purchase, with support contact guidance.
* Referrer-based auto-add-to-cart behavior preserved with clearer handling.

***

### Fixes

* License Usage Calendar — Fixed light-mode overlay on day cells in `DayUsagePanel` (background color and layering).
* Authentication — Failed session creation during login now triggers logout instead of leaving the user in a broken auth state.

***

### Improvements

#### License Usage Calendar Widget

* New `getDateOnlyKey` and `getHistoricalApiDateKey` helpers to standardize date formatting and avoid timezone issues.
* Refactored data fetching with generation tracking and cached date ranges to reduce redundant API calls.
* Added `usageScope` (`day` vs. `organization-current`) so the sidebar shows the correct context for usage counts.
* LicenseUsageOverview loads calendar vs. list content conditionally for better performance.
* Calendar module updated for consistent date handling across components.

#### Shop

* Removed scene-based “highlighted products” section; all products shown in the standard list with improved scene/referrer link handling.

#### Form components

* FormDatepicker — Stronger prop typing with `PropType`, improved null defaults, and safer computed property handling.
