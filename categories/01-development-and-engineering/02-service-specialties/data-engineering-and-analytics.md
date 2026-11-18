---
title: "Specialty: Data Engineering and Analytics"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../03-delivery-lifecycle/README.md"
  - "../04-engineering-standards/data-databases-and-test-data.md"
  - "../04-engineering-standards/observability-and-operational-readiness.md"
---

# Specialty: Data Engineering and Analytics

```yaml
specialty: data-engineering-and-analytics
activation_status: unconfirmed
prescribed_stack: none # Intentionally unconfirmed
```

## 1. Purpose
Explores the candidate technical requirements, pipeline quality gates, and schema management practices for delivering data extraction, transformation, warehousing, and analytics infrastructure.

## 2. Proposed Scope
- Batch and streaming ETL/ELT pipeline architectures.
- Cloud data warehousing (e.g., BigQuery, Snowflake, ClickHouse, PostgreSQL) and data lakehouse patterns.
- Data modeling, dimensional modeling, and schema migration strategies.
- Data quality verification, automated testing (e.g., dbt tests, Great Expectations), and freshness checks.
- Data privacy compliance: data anonymization, pseudonymization, PII masking, and retention enforcement.
- Business intelligence (BI) data mart provisioning and dashboard integration.
- Pipeline orchestration, dependency graphs, and backfill execution.

## 3. Applicability
Relevant when scoping, designing, building, or maintaining data pipelines, transformation jobs, or analytical databases. (Activation status: **unconfirmed**).

## 4. Related Documents
- Shared Lifecycle: [`../03-delivery-lifecycle/README.md`](../03-delivery-lifecycle/README.md).
- Engineering Standards:
  - [`../04-engineering-standards/data-databases-and-test-data.md`](../04-engineering-standards/data-databases-and-test-data.md): Database engineering standards.
  - [`../04-engineering-standards/security-and-privacy-engineering.md`](../04-engineering-standards/security-and-privacy-engineering.md): Data masking and regulatory privacy.
  - [`../04-engineering-standards/observability-and-operational-readiness.md`](../04-engineering-standards/observability-and-operational-readiness.md): Pipeline monitoring and SLA alerts.

## 5. Specialty-Specific Research Questions
- What lightweight modern data stack (e.g., DuckDB, dbt-core, Airbyte, Dagster) fits startup client budgets without high recurring cloud costs?
- How should historical data backfills be managed safely without overloading production source databases?
- What automated testing patterns best validate data pipeline schema drift when upstream APIs modify data contracts unexpectedly?

## 6. Known Unknowns
- Target client data volume and ingestion velocity profiles (megabytes vs. terabytes daily).
- Client in-house analytics engineering capability to maintain dbt models or pipeline DAGs post-handover.
- Cloud data warehouse query cost predictability and budget controls.

## 7. Candidate Evidence and Artifacts
- Data Pipeline Quality & Schema Validation Test Suite.
- Data Anonymization & PII Masking Reference Architecture.
- Data Warehouse Cost Allocation & Query Guardrail Playbook.

## 8. Next Action
Investigate lightweight, cost-effective data transformation and orchestration tools suitable for small-to-medium business clients.
