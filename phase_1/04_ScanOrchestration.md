# Phase 1 · Module 4: Scan Orchestration

## Context
You are enhancing an existing, working enterprise Data Quality and Governance platform.
The connector framework, asset registry, and metadata store are already implemented.
Some Scan Orchestration work may already exist.
**Read all existing code before writing anything. Do not overwrite existing files unless there is no other option.**

---

## Scope
**Build only:**
- Job definitions
- Job execution model
- Scheduling
- Retries
- Worker execution
- Scan run tracking
- Orchestration APIs

**Do not build:**
- Full profiling logic
- Rule engine logic
- Policy engine
- Lineage

---

## Objective
Design and implement a scan orchestration system that manages metadata discovery and future scan jobs in a clean, extensible way.

**Required job types:**
- connection_test
- metadata_discovery
- asset_refresh
- profile_scan_placeholder
- rule_scan_placeholder
- source_health_check

---

## Requirements
Implement:
1. Job definition model
2. Job run model
3. Manual trigger support
4. Scheduled execution support
5. Queue-based or worker-based execution model
6. Job statuses: queued, running, succeeded, partial_success, failed, timed_out, cancelled
7. Retry handling
8. Idempotent reruns
9. Logs per run
10. Metrics per run: started_at, ended_at, duration, assets_scanned, errors_count, warnings_count
11. Safe separation of orchestration from connector logic

---

## Design Constraints
- Orchestration service must call connector and metadata services — not embed their logic
- Support future parallel scans
- Add per-source concurrency control
- Design for future event-driven triggers
- Distinguish saved job configuration from individual job executions

---

## Deliverables
Produce in this order:
1. Orchestration architecture summary
2. Job model
3. Execution flow
4. Scheduling strategy
5. Retry and idempotency strategy
6. Database schema
7. APIs
8. Folder structure
9. Implementation plan
10. Code
11. Next integration notes for Results Storage

---

## Definition of Done
A developer must be able to:
- Define a scan job
- Run it manually
- Schedule it
- View execution history
- Inspect logs and status
- Rerun jobs safely
