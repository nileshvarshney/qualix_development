You are a senior backend architect, data platform engineer, and product-minded frontend engineer.

This prompt is only for Module 4:
Alerts and Notifications + Alert UI

Use the existing platform plus Profiling, Rules, and Scoring.

IMPORTANT UI/UX POLICY:
- Audit existing notification panels, status widgets, alert banners, activity feeds, tables, and detail pages first.
- Reuse current alert-like or incident-like screens if they exist.
- Prefer extending an existing activity/operations/monitoring screen rather than creating a separate alert world.
- Move existing alert-related items to the correct navigation if needed.

## Objective

Implement alerting and expose it through reused operations/monitoring UI with minimal net-new UI.

## Functional scope

Backend:
1. Alert definitions and lifecycle
2. Triggering from rule failures, score drops, freshness breaches
3. Notification targets
4. Alert history
5. Alert APIs

UI:
1. Reuse existing activity/feed/list/detail patterns
2. Add or adapt Alerts page or Alerts section
3. Add alert summary to dashboard if suitable widget exists
4. Reuse badges/status colors/patterns already in app

## Required workflow

Step 1: Audit
- Find any existing notifications, events, activity logs, operations pages, banners, issue lists, or monitoring widgets
- Identify which can host active alerts and alert history

Step 2: Plan
- Show minimal changes to surface alerts in the right app location

Step 3: Implement additive changes only

## Desired visible UI after implementation

Prefer this structure if compatible with existing app:
- Existing Operations or Monitoring area gains Alerts view
- Existing dashboard gains alert summary widget
- Existing asset detail gains Alerts section/tab if already tabbed
- Existing detail pages reused for alert drilldown where possible

## Deliverables

Return output in this order:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Minimal Safe Change Plan
4. Backend/Data Model Changes
5. API Changes
6. UI Changes and Navigation Placement
7. Files to Modify
8. Files to Create
9. Files Explicitly Not Touched
10. Code
11. Regression Checklist
12. Final Visible UI Changes

## Definition of done

A user should be able to:
- see active alerts in a reused operations/monitoring context
- open alert details without duplicative page patterns
- manage alert states from the existing app shell

Start with:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Minimal Safe Change Plan
