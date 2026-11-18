---
title: "Lifecycle 11: Operation, Maintenance, and Technical Closure"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./10-handover-and-support-transition.md"
  - "./12-retirement-and-client-exit.md"
  - "../04-engineering-standards/observability-and-operational-readiness.md"
  - "../04-engineering-standards/backup-recovery-and-incident-engineering.md"
---

# Lifecycle 11: Operation, Maintenance, and Technical Closure

## 1. Purpose
Defines the proposed practices for operating, monitoring, maintaining, and supporting applications that remain under agency retainer or internal operational management, up until formal project technical closure.

## 2. Proposed Scope
- Operational telemetry: application performance monitoring (APM), error tracking, log management, and alert routing.
- Maintenance runbooks: scheduled maintenance tasks, cache clearing, data pruning, and certificate renewals.
- Operational incident triage, severity classification, troubleshooting, and escalation.
- Periodic backup restoration drills to verify recovery objectives (RTO and RPO).
- Ongoing vulnerability intake, software supply-chain monitoring, and critical dependency patching.
- Execution of minor maintenance releases and SLA adherence tracking.
- Formal technical closure when ongoing operational retainers expire or conclude.

## 3. Applicability
Applies to client applications under active maintenance contracts and internal agency systems.

## 4. Related Documents
- [`./10-handover-and-support-transition.md`](./10-handover-and-support-transition.md): Transition into maintenance.
- [`./12-retirement-and-client-exit.md`](./12-retirement-and-client-exit.md): Downstream system retirement.
- [`../04-engineering-standards/observability-and-operational-readiness.md`](../04-engineering-standards/observability-and-operational-readiness.md): Monitoring standards.
- [`../04-engineering-standards/backup-recovery-and-incident-engineering.md`](../04-engineering-standards/backup-recovery-and-incident-engineering.md): Disaster recovery.

## 5. Questions to Research or Decide
- What response time SLAs (e.g., 1-hour critical vs. next-business-day standard) will the agency offer during maintenance?
- How is after-hours on-call coverage staffed and compensated in a small agency?
- How often must dependency security updates (e.g., monthly vs. quarterly) be deployed for maintenance clients?

## 6. Candidate Evidence and Artifacts
- Monthly Operational Health & Uptime Report.
- Quarterly Backup Restoration Drill Log.
- Incident Post-Mortem & Remediation Records.

## 7. Next Action
Draft standard SLA tiers and Maintenance Operations Runbook template.
