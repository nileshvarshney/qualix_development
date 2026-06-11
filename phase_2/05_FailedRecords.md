You are a senior backend architect, data platform engineer, and product-minded frontend engineer.

This prompt is only for Module 5:
Failed Records and Investigation UI

Use the existing platform plus prior Phase 2 modules.

IMPORTANT UI/UX POLICY:
- Audit existing detail pages, evidence tables, record viewers, drawers, side panels, and result drilldowns first.
- Reuse current table/detail/drawer patterns.
- Prefer adding failed-record evidence to existing rule detail, run detail, or asset detail screens.
- Avoid creating duplicate “investigation” pages if an existing detail experience can support them.

## Objective

Implement failed-record investigation and surface it inside reused run/rule/asset detail workflows.

## Functional scope

Backend:
1. Failed-record evidence model
2. Masking/redaction support
3. APIs for evidence retrieval
4. Links from runs, rules, and alerts to evidence

UI:
1. Reuse existing detail pages and drawers
2. Add failed-record tab/section to existing run or rule detail pages
3. Reuse existing tables for evidence views
4. Preserve role-based visibility and masking behavior

## Required workflow

Step 1: Audit
- Find current detail screens, result tables, drilldown flows, and permission-aware data views
- Identify where evidence belongs with the least UI churn

Step 2: Plan
- Show minimal additive approach

Step 3: Implement additive changes only

## Desired visible UI after implementation

Prefer this structure if compatible with existing app:
- Rule Detail > Failed Records tab
- Run Detail > Evidence tab
- Existing alert or asset detail drilldown links into evidence
- Existing drawer/table pattern reused for record inspection

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
- inspect failed records from reused detail screens
- understand failure context with minimal new UI
- see permission-aware masking in existing patterns

Start with:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Minimal Safe Change Plan
