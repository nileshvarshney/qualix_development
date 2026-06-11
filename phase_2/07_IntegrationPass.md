You are a senior backend architect, data platform engineer, and product-minded frontend engineer.

This prompt is for the Phase 2 Integration Pass.

Assume Phase 2 modules already exist:
1. Profiling
2. Rules
3. Scoring
4. Alerts
5. Failed Records
6. Trends

IMPORTANT UI/UX POLICY:
- This is an integration and reuse pass, not a rewrite.
- Audit all existing screens first.
- Prefer consolidating overlapping screens and moving them into the correct navigation instead of creating new duplicates.
- Reuse existing asset detail, dashboard, operations, and administration structures.
- Preserve current working routes, layouts, and flows.
- Make the app feel coherent without destructive refactoring.

## Objective

Integrate all Phase 2 features into the existing app so they appear in the right places and reuse the current UI wherever possible.

## Required workflow

Step 1: Audit all current UI surfaces
- dashboard pages
- source pages
- asset pages
- operations pages
- run history pages
- detail pages
- alert/monitoring/activity pages
- admin pages
- any duplicated or overlapping Phase 2 screens

Step 2: Identify consolidation opportunities
- which screens should be merged
- which widgets should be moved
- which tabs should be added to existing detail pages
- which duplicate pages should be avoided

Step 3: Propose final information architecture
Prefer this if compatible with the current app:
- Dashboard
  - Overview
  - Data Quality
  - Trends / Monitoring
  - Alerts Summary
- Sources
- Assets
  - Overview
  - Profiling
  - Rules
  - Quality Score
  - Alerts
  - Failures / Evidence
  - Trends
- Operations
  - Scan Jobs
  - Run History
- Administration
  - Users
  - Teams
  - Roles

Step 4: Implement only the smallest safe set of integration changes

## Deliverables

Return output in this order:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Overlapping/Duplicate UI Identified
4. Unified Information Architecture
5. Minimal Safe Change Plan
6. API/Backend Integration Adjustments
7. Files to Modify
8. Files to Create
9. Files Explicitly Not Touched
10. Code Changes
11. Regression Checklist
12. Final Visible UI Structure
13. End-to-End User Flows Now Supported

## Definition of done

The app should feel like one coherent data quality product built on top of existing UI, not a collection of newly added disconnected pages.

A user should be able to:
- navigate to profiling, rules, scoring, alerts, evidence, and trends from logical existing surfaces
- drill between related experiences
- keep using prior screens without regressions
- avoid duplicate pages for the same concept

Start with:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Overlapping/Duplicate UI Identified
Do not begin with rewriting routes or layouts.
