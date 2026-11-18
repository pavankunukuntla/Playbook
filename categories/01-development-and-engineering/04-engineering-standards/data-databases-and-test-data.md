---
title: "Standard: Data, Databases, and Test Data"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./security-and-privacy-engineering.md"
  - "../03-delivery-lifecycle/09-release-readiness-and-deployment.md"
  - "../../12-legal-security-and-risk-management/README.md"
---

# Standard: Data, Databases, and Test Data

## 1. Purpose
Establishes proposed standards for database schema modeling, automated migration management, zero-downtime schema evolution, query optimization, and secure test-data generation with complete privacy preservation.

## 2. Proposed Scope
- Data modeling standards: foreign keys, cascading constraints, audit timestamps (`created_at`, `updated_at`), and soft-delete patterns.
- Version-controlled schema migrations: forward-only migrations, backwards compatibility, and reversible down-migration scripts.
- Multi-step zero-downtime migration patterns (expand/contract pattern for column renames and schema deprecations).
- Indexing strategies, query plan analysis (`EXPLAIN ANALYZE`), and connection pooling configurations.
- Test data management: synthetic data generation (e.g., Faker), database seeding scripts, and an absolute prohibition against importing unmasked production PII into development or staging environments.
- Data archival, retention scheduling, and automated data purging scripts.

## 3. Applicability
Applies to all persistent data storage, relational and NoSQL databases, and analytical data stores.

## 4. Related Documents
- [`./security-and-privacy-engineering.md`](./security-and-privacy-engineering.md): Data masking and encryption.
- [`../03-delivery-lifecycle/09-release-readiness-and-deployment.md`](../03-delivery-lifecycle/09-release-readiness-and-deployment.md): Migration rehearsal.
- [`../../12-legal-security-and-risk-management/README.md`](../../12-legal-security-and-risk-management/README.md): Data privacy and retention policy.

## 5. Questions to Research or Decide
- What ORM / migration tool (e.g., Prisma, Drizzle, Alembic, Flyway) provides the best balance of safety and developer velocity?
- How should database migrations be gated in CI to prevent accidental lockouts during heavy table alters?
- What anonymization tool (e.g., RepliByte, custom scripts) should be standard for scrubbing client data dumps?

## 6. Candidate Evidence and Artifacts
- Database Migration CI Verification Script (testing up and down migrations).
- Synthetic Seed Data Generator and Fixtures.
- Query Performance Benchmarking Log.

## 7. Next Action
Draft standard migration review checklist covering lock safety and backwards compatibility.
