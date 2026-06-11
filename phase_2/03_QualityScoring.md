You are a senior backend architect, data platform engineer, and product-minded frontend engineer.

This prompt is only for Module 3:
Quality Scoring + Scorecard UI

Use the existing platform plus Profiling and Rules.

IMPORTANT UI/UX POLICY:
- Audit existing dashboard pages, summary cards, KPI tiles, charts, overview panels, badges, and asset summary sections first.
- Reuse current dashboard shells and asset overview layouts.
- Prefer adding scorecards into existing dashboard/asset overview experiences instead of inventing a parallel dashboard.
- Move existing related widgets into the right location if necessary rather than duplicating them.

## Objective

Implement quality scoring and surface it through reused dashboards, reused asset summaries, and minimal new UI.

## Functional scope

Backend:
1. Quality score model by dimension
2. Asset score calculation
3. Score history
4. Rollups where possible
5. Score APIs

Dimensions:
- completeness
- validity
- uniqueness
- timeliness
- consistency placeholder
- integrity placeholder

UI:
1. Add score summary to existing dashboard if one exists
2. Add quality badge/scorecard to existing asset overview/detail
3. Reuse existing chart patterns for score trends
4. Reuse existing top-risk list/table widgets if available

## Required workflow

Step 1: Audit
- Find existing dashboards, cards, charts, widgets, score-like components, and asset summary panels
- Identify the best places to insert score UI

Step 2: Plan
- Show what existing components will be reused
- Show what minimal changes are needed to expose scores in the right navigation locations

Step 3: Implement additive changes only

## Desired visible UI after implementation

Prefer this structure if compatible with existing app:
- Existing Dashboard gets Data Quality Overview widgets
- Asset Overview or Asset Detail gets Quality Score card/badge
- Existing chart page or dashboard tab reused for score trends

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
- see a score on an existing dashboard or asset summary page
- inspect score breakdown on a reused detail experience
- see score trends without introducing a competing dashboard

Start with:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Minimal Safe Change Plan
