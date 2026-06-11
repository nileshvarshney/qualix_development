You are a senior backend architect, data platform engineer, and product-minded frontend engineer.

This prompt is only for Module 2:
Rule Engine + Rule Builder UI

Use the existing platform plus Profiling from Module 1.

IMPORTANT UI/UX POLICY:
- Audit existing forms, list pages, table pages, detail pages, rule-like screens, validation screens, and scheduling screens first.
- Reuse and extend existing create/edit/detail/list patterns.
- Prefer adapting existing forms and result tables rather than introducing a new rule-builder framework.
- If similar screens exist in the wrong section, move or rewire them instead of duplicating them.
- Keep changes minimal and safe.

## Objective

Implement data quality rules and expose them through reused and extended UI.

## Functional scope

Backend:
1. Rule definitions and templates
2. Rule versioning
3. Rule scope by asset/table/column
4. Rule severity and thresholds
5. Rule execution
6. Rule results and history
7. Rule APIs

Initial rule types:
- not_null
- unique
- accepted_values
- regex_pattern
- numeric_range
- date_range
- freshness
- row_count_threshold
- duplicate_threshold
- custom SQL placeholder

UI:
1. Reuse existing list/detail/form screens where possible
2. Add or adapt a Rules tab on asset detail
3. Add or adapt a Rules management page
4. Reuse existing run history/detail pages for rule runs where possible
5. Add assignment flow using existing modal/drawer/form pattern

## Required workflow

Step 1: Audit
- Find existing list views, form pages, schedule forms, detail pages, and any rule/validation-like UI
- Identify what can be reused or moved

Step 2: Plan
- Show smallest safe set of modifications
- Avoid duplicate create/edit pages if suitable forms already exist

Step 3: Implement additive changes only

## Desired visible UI after implementation

Prefer this structure if compatible with existing app:
- Asset Detail > Rules tab
- Existing admin/configuration area extended with Rules page
- Existing form framework reused for Create/Edit Rule
- Existing run history pages reused for rule run history and results

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
- create or edit a rule using reused form patterns
- assign rules to assets/columns from existing asset context
- run rules and view results in reused operations/run screens
- inspect rules from the right navigation without duplicate pages

Start with:
1. Audit Findings
2. Existing Screens/Components to Reuse
3. Minimal Safe Change Plan
