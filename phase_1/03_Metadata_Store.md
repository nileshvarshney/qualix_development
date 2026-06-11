  # Claude Code Prompt — Phase 1 · Module 3: Metadata Store

## Context
You are enhancing an existing, working enterprise Data Quality and Governance platform.
The connector framework and asset registry are already implemented.
Some Metadata Store work may already exist.
**Read all existing code before writing anything. Do not overwrite existing files unless there is no other option.**

---

## Scope
**Build only:**
- Normalized metadata persistence
- Metadata versioning / snapshots
- Current-state and historical metadata queries
- Schema evolution tracking
- Quality-related placeholder fields

**Do not build:**
- Business glossary
- Governance policy engine
- Lineage graph
- Rule engine
- Catalog UI

---

## Objective
Design and implement a metadata store that persists normalized technical and operational metadata for discovered assets, supporting:
- Current metadata view
- Historical snapshots
- Schema evolution comparisons
- Future governance and quality extensions

---

## Requirements
Store the following for each asset:

**Schema & Table metadata**
- Source metadata, schema metadata, table metadata
- Column metadata: data type, nullable flag, precision, scale, default values
- Partition information if available
- Row count snapshot
- Last modified metadata if available
- Tags and labels
- Ownership links

**Operational metadata**
- last_scanned_at, scan_status, scan_duration, scan_version

**Quality placeholders**
- latest_profile_score, latest_quality_status
- critical_data_element, attached_rule_count_placeholder

---

## Design Constraints
- Prefer relational design unless another choice is clearly justified
- Support both latest-state and historical comparison queries
- Make schema changes trackable over time
- Design so future lineage and governance modules can attach without a major rewrite

---

## Deliverables
Produce in this order:
1. Metadata domain summary
2. Snapshot/versioning strategy
3. Entity design
4. Database schema
5. Historical query strategy
6. APIs
7. Folder structure
8. Implementation plan
9. Code
10. Next integration notes for Scan Orchestration

---

## Definition of Done
A developer must be able to:
- Persist normalized metadata from a connector
- Retrieve latest metadata for any asset
- View historical metadata snapshots
- Detect schema changes across scan runs
