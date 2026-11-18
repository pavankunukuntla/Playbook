---
title: "Pattern: Ongoing Maintenance"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../03-delivery-lifecycle/11-operation-maintenance-and-technical-closure.md"
  - "../04-engineering-standards/observability-and-operational-readiness.md"
  - "../../10-finance-and-money-management/README.md"
---

# Pattern: Ongoing Maintenance

## 1. Purpose
Defines proposed engineering workflows, operational rhythms, SLA tracking, and scope boundaries for delivering ongoing technical maintenance, support retainers, and preventative system care.

## 2. Proposed Scope
- Categorization of maintenance activities:
  - *Preventative:* Monthly dependency patching, runtime upgrades, security CVE patching.
  - *Corrective:* Bug fixes, defect triage, operational troubleshooting.
  - *Adaptive:* Minor adjustments to accommodate external third-party API changes.
  - *Perfective:* Small performance enhancements and database index tuning.
- Strict scope boundary management: preventing feature development from consuming allocated maintenance retainer hours.
- SLA adherence: tracking response time and resolution time metrics against contractually agreed tiers.
- Monthly operational reporting: detailing uptime, resolved defects, applied patches, and cloud resource consumption.
- Retainer capacity allocation and rollover boundaries (collaborating with Finance and Project Delivery).

## 3. Applicability
Applies to all client systems maintained under ongoing post-launch service-level agreements (SLAs) or monthly technical retainers.

## 4. Related Documents
- [`../03-delivery-lifecycle/11-operation-maintenance-and-technical-closure.md`](../03-delivery-lifecycle/11-operation-maintenance-and-technical-closure.md): Operational stage.
- [`../04-engineering-standards/observability-and-operational-readiness.md`](../04-engineering-standards/observability-and-operational-readiness.md): Monitoring.
- [`../../10-finance-and-money-management/README.md`](../../10-finance-and-money-management/README.md): Retainer billing and hours reconciliation.

## 5. Questions to Research or Decide
- What is our minimum monthly maintenance retainer fee and hours allocation?
- How do we handle maintenance requests that exceed the monthly allotted hours (e.g., auto-bill overage vs. require SOW addendum)?
- What is our standard SLA for Sev 1 critical production defects outside standard business hours?

## 6. Candidate Evidence and Artifacts
- Monthly Maintenance & Security Patching Report.
- SLA Response Time & Incident Resolution Telemetry.
- Maintenance Retainer Capacity & Hours Burn-down Log.

## 7. Next Action
Collaborate with Sales and Project Delivery to formulate standard Maintenance Retainer SLA tiers.
