You are a senior backend architect, data platform engineer, and product-minded frontend engineer.

We are building Phase 2 of an enterprise Data Quality platform.

This prompt is only for Module 1:
Profiling Engine + Profiling UI

Use the existing Phase 1 platform as the foundation:
- Source Connector Framework
- Asset Registry
- Metadata Store
- Scan Orchestration
- Results Storage
- Basic User and Role Model
- Existing UI shell, existing pages, existing routing, existing design system

IMPORTANT:
- This must be an additive change.
- Do not damage or refactor existing working pages.
- Reuse existing layout, routing, navigation, styling, tables, page shells, and API patterns.
- Add only what is needed for profiling capability and its related UI.
- If a backend primitive already exists, extend it rather than replacing it.

## Objective

Implement asset-level and column-level data profiling so users can run a profile scan on a dataset and inspect profiling results in the UI.

## Functional scope

Backend:
1. Profiling job type integrated with existing scan orchestration
2. Profile execution for supported assets
3. Persist profile results in results storage
4. Support baseline profile dimensions such as:
   - row count
   - column count
   - null ratio
   - distinct count
   - uniqueness ratio
   - min / max for numeric/date fields
   - top values
   - pattern frequency
   - freshness indicators if available
   - schema summary
5. Asset-level and column-level profile history
6. Status tracking for profile runs
7. APIs for profile summary and profile detail retrieval

UI:
1. Add a "Profiling" action on supported asset detail pages
2. Add a profile run trigger flow
3. Add profile run status and latest profile summary
4. Add an asset profile detail page or tab
5. Add column profile cards/table
6. Add historical profile run selector
7. Add empty, loading, and error states
8. Add role-aware UI behavior based on existing permissions

## UI screens to add

Use existing app shell. Add only the following screens or tabs:
- Asset Detail > Profiling tab
- Profile Run modal or action panel
- Profile Run History section
- Column Profile Detail drawer or page
- Optional: Profile Summary card on asset overview

UI requirements:
- Do not redesign the existing app
- Add pages/tabs in the current navigation and page patterns
- Show key profile metrics in readable tables/cards
- Include “last profiled at”, “run status”, and “asset health snapshot”
- Make results understandable to data stewards and engineers
- If no profile exists, render a clear empty state with CTA to run first profile

## Deliverables

Return output in this order:
1. Audit of existing Phase 1 integration points relevant to profiling
2. Profiling architecture summary
3. Data model changes
4. APIs
5. UI screens and navigation changes
6. Files to create
7. Files to modify
8. Files explicitly not touched
9. Implementation plan
10. Code
11. Regression checklist
12. Final screens that should appear

## Definition of done

A user should be able to:
- open an asset
- trigger a profiling run
- see profiling job status
- view latest profile summary
- inspect per-column profiling results
- compare profile runs historically

Start with:
1. Audit of existing profiling-related extension points
2. Profiling architecture summary
3. Data model changes
Do not start broad refactoring.
