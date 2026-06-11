# Phase 1 · Module 6: Basic User and Role Model

## Context
You are enhancing an existing, working enterprise Data Quality and Governance platform.
All previous Phase 1 modules are already implemented: connector framework, asset registry, metadata store, scan orchestration, and results storage.
Some User and Role work may already exist.
**Read all existing code before writing anything. Do not overwrite existing files unless there is no other option.**

---

## Scope
**Build only:**
- Users
- Teams
- Role assignments
- RBAC permissions
- Ownership assignments
- Audit fields
- Notification target metadata

**Do not build:**
- Fine-grained ABAC
- Policy-based authorization
- Approval workflows
- Governance policy engine

---

## Objective
Design and implement a simple but production-ready RBAC model for Phase 1 operations.

**Initial roles:**
- admin
- data_steward
- data_engineer
- analyst
- viewer

---

## Requirements
Implement:
1. User model
2. Team model
3. Role model
4. User-role and team-role assignments
5. Asset ownership assignments
6. Permission mapping for: manage_sources, run_scans, view_results, manage_assets, manage_users, edit_metadata
7. Notification target metadata
8. Audit fields on major entities: created_by, updated_by, approved_by_placeholder, created_at, updated_at

---

## Design Constraints
- Keep authorization simple with RBAC first
- Support later extension to stewardship workflows and policy controls
- Make ownership visible on assets and scan responsibilities
- Avoid overengineering

---

## Deliverables
Produce in this order:
1. Identity and access summary
2. RBAC model
3. Entity relationships
4. Database schema
5. Permission evaluation strategy
6. APIs
7. Folder structure
8. Implementation plan
9. Code
10. Next integration notes for final Phase 1 wiring

---

## Definition of Done
A developer must be able to:
- Create users and teams
- Assign roles
- Assign ownership of assets
- Check permissions for common Phase 1 actions
- Store audit metadata on core records
