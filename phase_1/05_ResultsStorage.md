# Phase 1 · Module 5: Results Storage

## Context
You are enhancing an existing, working enterprise Data Quality and Governance platform.
The connector framework, asset registry, metadata store, and scan orchestration are already implemented.
Some Results Storage work may already exist.
**Read all existing code before writing anything. Do not overwrite existing files unless there is no other option.**

---

## Scope
**Build only:**
- Scan result persistence
- Run summaries
- Asset-level scan summaries
- Historical metrics storage
- Evidence and diagnostics model
- Future compatibility with profiling and rule results

**Do not build:**
- Full profiling engine
- Rule engine
- Lineage
- Compliance reporting

---

## Objective
Design and implement a results storage layer for metadata scans and future quality scan outputs supporting:
- Latest result lookup
- Historical trend lookup
- Scan run comparison
- Linkage to source, asset, connector, and job run

---

## Requirements

**Store:**
- scan_run_summary
- asset_scan_summary
- profiling_result_placeholder
- rule_result_placeholder
- failed_sample_records_placeholder
- metrics_history
- Diagnostics and evidence

**Future-compatible fields must anticipate:**
- Null ratio
- Distinct count
- Min / max
- Top values or pattern frequency
- Freshness
- Volume changes
- Schema drift indicators

---

## Design Constraints
- Separate summary metrics from heavy evidence payloads where appropriate
- Add retention strategy for large or sensitive evidence
- Make trend queries efficient
- Keep linkage to job runs and assets explicit

---

## Deliverables
Produce in this order:
1. Results domain summary
2. Storage model
3. Entity relationships
4. Database schema
5. Historical and comparison query design
6. APIs
7. Folder structure
8. Implementation plan
9. Code
10. Next integration notes for Basic User and Role Model

---

## Definition of Done
A developer must be able to:
- Persist scan run summaries
- Retrieve latest results
- Retrieve trend history
- Compare two runs
- Inspect result evidence links
