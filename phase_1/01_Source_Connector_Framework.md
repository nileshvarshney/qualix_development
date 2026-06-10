We are building an enterprise Data Quality and Governance platform. Phase 1 Module 1: Source Connector Framework.

We have already completed most of the work, you just need to ensure we are not missing anyting mentioned below 

Your task is to design and implement a pluggable connector framework that will later support metadata discovery, profiling, rule execution, and governance extensions.

<scope>
Focus only on:
- source connection model
- connector abstraction
- connector adapters
- connection lifecycle
- metadata discovery interface
- connector health and scan readiness

Do not implement:
- lineage
- policy engine
- access governance
- glossary
- compliance reporting
- full profiling engine
- rule engine
</scope>

<objective>
Design a connector framework that supports at least:
- PostgreSQL
- MySQL
- Snowflake
- BigQuery
- S3/file datasets (metadata-level support only)

The framework must provide a common interface for:
- test_connection
- list_databases or equivalent
- list_schemas
- list_tables
- list_columns
- get_table_metadata
- sample_rows
- run_metadata_scan
</objective>

<requirements>
Implement:
1. Source connection entity and configuration model
2. Secure credential abstraction
3. Connector interface / base class
4. Source-specific adapters
5. Metadata normalization into a shared internal format
6. Error handling and retry classification
7. Source health status
8. Scan-readiness tracking
9. Environment tagging such as dev/stage/prod
10. Last successful scan tracking
</requirements>

<design_constraints>
- Keep connector-specific logic separate from orchestration and metadata services
- Design for easy addition of new source types
- Use clear typing and validation
- Prefer production-grade patterns over demo code
- Add extension points for future profile and rule scan support
- If a full implementation is too large, build a production-quality scaffold with at least one fully implemented connector and clean placeholders for the others
</design_constraints>

<deliverables>
Return output in this order:
1. Architecture summary
2. Connector abstraction design
3. Source data model
4. Error model
5. Adapter structure
6. API endpoints for source management
7. Folder structure
8. Implementation plan
9. Code
10. Next integration notes for Asset Registry
</deliverables>

<definition_of_done>
A developer should be able to:
- register a source
- store source config
- test source connectivity
- invoke metadata discovery through a common interface
- see normalized metadata output
- inspect connector health state
</definition_of_done>
