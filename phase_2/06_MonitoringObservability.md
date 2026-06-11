You are a senior backend architect, data platform engineer, and product-minded frontend engineer.

This prompt is only for Module 6:
Trend Monitoring and Observability UI

Use the existing platform plus prior Phase 2 modules.

IMPORTANT UI/UX POLICY:
- Audit existing dashboard tabs, trend charts, historical views, monitoring pages, filters, and source/asset detail pages first.
- Reuse chart containers, filter bars, dashboard widgets, and overview tabs already in the app.
- Prefer adding trend views to existing dashboard and detail experiences rather than introducing a separate monitoring app.
- Move current trend-like widgets to better navigation if needed instead of duplicating them.

## Objective

Implement time-based monitoring and observability views using reused dashboard and detail UI.

## Functional scope

Backend:
1. Trend aggregation APIs
2. Historical time-series for profile/rule/score/alert data
3. Basic anomaly placeholders
4. Drilldown mapping from charts to runs/rules/alerts

UI:
1. Reuse current charting and filter systems
2. Add trend views to existing dashboard/detail locations
3. Reuse existing monitoring or analytics pages if present
4. Support asset/source/rule trend drilldowns

## Required workflow

Step 1: Audit
- Find existing charts, dashboard tabs, monitoring pages, source detail pages, asset detail pages, and filters
- Identify the best reused surfaces for trends

Step 2: Plan
- Show smallest safe set of UI and navigation changes

Step 3: Implement additive changes only

## Desired visible UI after implementation

Prefer this structure if compatible with existing app:
- Existing Dashboard gets Trends / Monitoring section or tab
- Asset Detail gets Trends tab if already tabbed
- Source Detail gets Health Trends panel if a source page already exists
- Existing alert or rules views get compact trend widgets where helpful

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
- see historical quality trends in reused dashboard/detail screens
- filter trends consistently with the rest of the app
- drill from reused charts to supporting data

Start with:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Minimal Safe Change Plan
