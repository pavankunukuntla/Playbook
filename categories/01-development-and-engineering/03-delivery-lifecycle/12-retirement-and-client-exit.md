---
title: "Lifecycle 12: Retirement and Client Exit"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./11-operation-maintenance-and-technical-closure.md"
  - "../04-engineering-standards/data-databases-and-test-data.md"
  - "../../12-legal-security-and-risk-management/README.md"
---

# Lifecycle 12: Retirement and Client Exit

## 1. Purpose
Defines the proposed procedure for safely decommissioning software systems, conducting secure data export and sanitization, shutting down cloud infrastructure, terminating integrations, and recording formal technical exit upon client relationship termination.

## 2. Proposed Scope
- Formal decommissioning authorization and ownership sign-off.
- Notification sequence to affected end-users and upstream/downstream integration partners.
- Secure data export: full database dump, asset archives, and encrypted delivery to client.
- Data retention, regulatory archival, and secure sanitization / deletion verification.
- Comprehensive cloud infrastructure teardown (terminating compute, deleting databases, releasing static IPs, purging caches).
- Revocation of all access credentials, API keys, service accounts, and IAM roles.
- Archival of project Git repositories and documentation to long-term agency cold storage.
- Formulation of the Final Decommissioning Audit Record.

## 3. Applicability
Applies when a client system is permanently retired, superseded by a new application, or when the client terminates the agency relationship and exits agency infrastructure.

## 4. Related Documents
- [`./11-operation-maintenance-and-technical-closure.md`](./11-operation-maintenance-and-technical-closure.md): Preceding operational stage.
- [`../04-engineering-standards/data-databases-and-test-data.md`](../04-engineering-standards/data-databases-and-test-data.md): Data retention standards.
- [`../../12-legal-security-and-risk-management/README.md`](../../12-legal-security-and-risk-management/README.md): Legal compliance on data deletion.

## 5. Questions to Research or Decide
- What is the mandatory waiting period between putting a system into "read-only / maintenance mode" and executing final infrastructure destruction?
- How long must the agency retain cold backups of client data for legal protection post-termination?
- How do we technically verify that no orphaned cloud resources continue incurring billing charges post-teardown?

## 6. Candidate Evidence and Artifacts
- System Decommissioning Plan & Authorization Form.
- Encrypted Data Export Delivery Receipt.
- Infrastructure Destruction & Access Revocation Audit Log.
- Final Technical Exit Certificate.

## 7. Next Action
Develop a comprehensive System Decommissioning & Cloud Teardown Checklist.
