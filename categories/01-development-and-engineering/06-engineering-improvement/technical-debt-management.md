---
title: "Improvement: Technical Debt Management"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./improvement-backlog.md"
  - "../01-engineering-governance/exceptions-and-escalation.md"
---

# Improvement: Technical Debt Management

## 1. Purpose
Establishes a proposed framework for identifying, cataloging, risk-ranking, and systematically retiring technical debt to prevent codebase entropy, velocity degradation, and operational fragility.

## 2. Proposed Scope
- Technical debt classification (Martin Fowler's Technical Debt Quadrant: Prudent/Deliberate vs. Reckless/Inadvertent).
- Standardized debt logging: capturing debt items directly in issue trackers with a `tech-debt` label, linking the temporary shortcut to the required long-term refactor.
- Estimating the "interest rate" of debt: identifying items that actively slow down everyday feature development versus low-impact legacy quirks.
- Debt repayment capacity models: proposing a standard allocation (e.g., 10%–20% of sprint capacity or scheduled hardening periods) dedicated to debt remediation.
- Pre-handover debt audits: ensuring client deliverables do not leave behind hidden architectural debt that undermines client trust.

## 3. Applicability
Applies to all active client codebases and agency-managed internal platforms.

## 4. Related Documents
- [`./improvement-backlog.md`](./improvement-backlog.md): Central backlog of internal improvements.
- [`../01-engineering-governance/exceptions-and-escalation.md`](../01-engineering-governance/exceptions-and-escalation.md): Logging debt resulting from approved exceptions.
- [`../03-delivery-lifecycle/03-existing-system-assessment.md`](../03-delivery-lifecycle/03-existing-system-assessment.md): Assessing inherited debt.

## 5. Questions to Research or Decide
- How do we commercially justify technical debt repayment sprints to clients on fixed-budget contracts?
- What criteria mandate an immediate architectural refactor rather than deferring to technical debt?
- How is technical debt tracked in client repositories vs. internal agency systems?

## 6. Candidate Evidence and Artifacts
- Technical Debt Register & Prioritization Matrix.
- Sprint Capacity Allocation Telemetry (% debt vs. feature work).
- Technical Debt Retirement Burn-down Chart.

## 7. Next Action
Draft standard `tech-debt` issue template for project tracking repositories.
