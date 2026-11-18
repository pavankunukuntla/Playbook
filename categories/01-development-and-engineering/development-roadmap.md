---
title: "Development and Engineering Roadmap"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./coverage-matrix.md"
  - "./open-questions.md"
---

# Development and Engineering Roadmap

This roadmap tracks the progressive research, discussion, drafting, and validation status of all architectural areas within the Development and Engineering category.

> [!NOTE]
> Dates and personal assignees are deliberately omitted to prevent fabricating arbitrary commitments. Topics are prioritized based on their foundational role in establishing safe technical operations and client delivery.

---

## 1. Governance & Foundations

| Topic | Priority & Rationale | Research Status | Discussion Status | Drafting Status | Validation Status | Next Action |
| :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **Project Risk & Engineering Tailoring** | **High:** Required to prevent over-engineering small projects or leaving critical systems vulnerable. | Verified | Scaffolding | Draft | Walkthrough 1 & 2 | Finalize lightweight intake risk questionnaire |
| **Review Gates & Evidence** | **High:** Defines mandatory technical evidence required before client milestone releases. | Verified | Scaffolding | Draft | Walkthrough 5 | Draft PR and Release Gate checklists |
| **Roles & Ownership** | **Medium:** Clarifies tech lead and reviewer accountability as team scales. | Ongoing | Scaffolding | Stubs | Pending | Founder discussion on technical authority |
| **Exceptions & Escalation** | **Medium:** Prevents unapproved shortcuts from becoming permanent technical debt. | Ongoing | Scaffolding | Stubs | Walkthrough 5 | Create Exception Request issue template |
| **Engineering Decisions (ADRs)** | **High:** Preserves technical decision rationale and prevents circular architectural debates. | Verified | Scaffolding | Stubs | Pending | Standardize project ADR Markdown format |

---

## 2. Core Engineering Standards

| Topic | Priority & Rationale | Research Status | Discussion Status | Drafting Status | Validation Status | Next Action |
| :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **Environments, Config & Secrets** | **Critical:** Accidental secret leaks create catastrophic commercial and legal liability. | Verified | Scaffolding | Draft | Walkthrough 2 | Deploy Gitleaks pre-commit hooks to starter repo |
| **Code Quality & Review** | **High:** Foundation of technical quality and peer context sharing. | Verified | Scaffolding | Draft | Walkthrough 2 & 5 | Draft PR template with self-review checklist |
| **Testing & Quality Engineering** | **High:** Predictor of continuous delivery performance (DORA); prevents regressions. | Verified | Scaffolding | Draft | Walkthrough 2 | Select standard test runner per stack |
| **CI/CD & Release Engineering** | **High:** Automates quality checks and deployment safety. | Verified | Scaffolding | Draft | Walkthrough 1, 2, 5 | Build reusable GitHub Actions composite workflows |
| **UX, UI & Accessibility (WCAG 2.2)** | **Medium:** Essential for public web interfaces and legal compliance. | Verified | Scaffolding | Draft | Walkthrough 1 | Configure automated axe-core scanning in CI |
| **Dependencies & Supply Chain** | **High:** Open-source vulnerabilities and license compliance risks (NIST SSDF). | Verified | Scaffolding | Draft | Walkthrough 4 | Establish approved open-source license whitelist |
| **API & Integration Engineering** | **High:** Core discipline for automation, backend, and third-party integrations. | Verified | Scaffolding | Draft | Walkthrough 3 | Standardize OpenAPI Spectral linting & RFC 7807 |
| **Data, Databases & Migrations** | **Critical:** Data loss and failed schema migrations cause extended outages. | Verified | Scaffolding | Draft | Walkthrough 5 | Draft database down-migration verification rule |
| **Security & Privacy Engineering** | **Critical:** Protects against OWASP Top 10 vulnerabilities and PII data leaks. | Verified | Scaffolding | Draft | Walkthrough 2 | Configure Semgrep SAST rulesets in starter repo |
| **Observability & Readiness** | **Medium:** Ensures production systems are monitorable and alertable. | Ongoing | Scaffolding | Stubs | Walkthrough 3 | Standardize JSON logger with PII masking |
| **Backup & Incident Recovery** | **High:** Protects business continuity and recovery time objectives (RTO/RPO). | Ongoing | Scaffolding | Stubs | Walkthrough 5 | Draft Blameless Post-Mortem template |
| **Technical Documentation** | **Medium:** Ensures system maintainability and client handover clarity. | Verified | Scaffolding | Stubs | Walkthrough 6 | Build standard `README.md` and `RUNBOOK.md` |
| **AI-Assisted Development** | **Medium:** Balances developer productivity with code security and IP hygiene. | Ongoing | Scaffolding | Draft | Walkthrough 2 | Review commercial AI tool data-sharing terms |
| **Performance & Capacity** | **Low:** Tailored to high-traffic deliverables; premature for basic MVPs. | Ongoing | Scaffolding | Stubs | Pending | Draft k6 baseline load test script |

---

## 3. Delivery Lifecycle Execution

| Topic | Priority & Rationale | Research Status | Discussion Status | Drafting Status | Validation Status | Next Action |
| :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **01 Technical Intake & Handoff** | **High:** Prevents accepting unfeasible projects or misaligned scopes. | Verified | Scaffolding | Draft | Walkthrough 1–4 | Align with Sales on intake brief template |
| **02 Discovery & Requirements** | **Critical:** Requirements ambiguity is the primary cause of agency project failure. | Verified | Scaffolding | Draft | Walkthrough 1–4 | Draft User Story & Acceptance Criteria template |
| **03 Existing System Assessment** | **High:** Essential for safe codebase takeovers and legacy migrations. | Ongoing | Scaffolding | Stubs | Walkthrough 4 | Create Codebase Audit Checklist |
| **04 Experience & Solution Design** | **High:** De-risks architecture before writing production code. | Verified | Scaffolding | Draft | Walkthrough 2 | Draft Solution Architecture Document outline |
| **05 Feasibility & Estimation** | **High:** Directly drives commercial profitability and fixed-price safety. | Ongoing | Scaffolding | Stubs | Pending | Build Three-Point Estimation spreadsheet |
| **06 Project Engineering Setup** | **High:** Eliminates environment setup bottlenecks. | Verified | Scaffolding | Draft | Walkthrough 1, 2 | Build reusable project starter repository |
| **07 Iterative Implementation** | **High:** Daily sprint rhythm and PR velocity. | Verified | Scaffolding | Stubs | Walkthrough 2 | Define Definition of Ready (DoR) gate |
| **08 Verification & Acceptance** | **Critical:** Gate for client sign-off and milestone revenue collection. | Verified | Scaffolding | Draft | Walkthrough 2 | Draft standard UAT Protocol |
| **09 Release & Deployment** | **Critical:** Production release safety and rollback preparedness. | Verified | Scaffolding | Draft | Walkthrough 5 | Draft Production Release Runbook template |
| **10 Handover & Transition** | **High:** Prevents post-project support scope creep and stranded credentials. | Verified | Scaffolding | Stubs | Walkthrough 6 | Draft Technical Handover Acceptance Form |
| **11 Operation & Maintenance** | **Medium:** Supports recurring maintenance retainer revenue. | Ongoing | Scaffolding | Stubs | Walkthrough 3 | Define SLA response times with Sales |
| **12 Retirement & Client Exit** | **Low:** Needed only when systems reach end-of-life or clients exit. | Ongoing | Scaffolding | Stubs | Walkthrough 7 | Draft System Decommissioning Checklist |

---

## 4. Service Specialties & Engagement Patterns

| Topic | Priority & Rationale | Research Status | Discussion Status | Drafting Status | Validation Status | Next Action |
| :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **Web Applications & Websites** | **High:** Primary expected client demand area. | Ongoing | Scaffolding | Stubs | Walkthrough 1 | Evaluate headless CMS pairings |
| **Automation & Business Systems** | **High:** High-margin agency niche; requires idempotency standards. | Ongoing | Scaffolding | Stubs | Walkthrough 3 | Test self-hosted vs cloud n8n/Make patterns |
| **Backend APIs & Integrations** | **High:** Foundational to both web and automation specialties. | Ongoing | Scaffolding | Stubs | Walkthrough 2, 3 | Draft API design standards |
| **AI Applications & Agents** | **Medium:** High market interest; requires strict eval and cost guardrails. | Ongoing | Scaffolding | Stubs | Pending | Draft RAG evaluation benchmark |
| **Existing Project Takeovers** | **High:** Common client scenario; requires strong liability boundaries. | Ongoing | Scaffolding | Stubs | Walkthrough 4 | Draft Takeover Liability Addendum |
| **Prototypes & POCs** | **High:** Low-risk commercial entry point for new clients. | Ongoing | Scaffolding | Stubs | Walkthrough 1 | Draft Prototype Risk Waiver template |
| **Ongoing Maintenance** | **Medium:** Predictable recurring agency revenue stream. | Ongoing | Scaffolding | Stubs | Walkthrough 3 | Align maintenance hours allocation with Finance |
| **Modernization & Migrations** | **Medium:** Complex, high-value consulting engagements. | Ongoing | Scaffolding | Stubs | Walkthrough 4 | Document Strangler Fig reference design |
| **Mobile Applications** | **Low:** High distribution complexity; evaluate demand first. | Ongoing | Scaffolding | Stubs | Pending | Research cross-platform framework trade-offs |
| **Cloud & Platform Engineering** | **Low:** Specialized; offer primarily as part of web/API delivery. | Ongoing | Scaffolding | Stubs | Pending | Standardize baseline Terraform modules |
| **Desktop Applications** | **Low:** Niche requirement; activate only upon explicit client demand. | Ongoing | Scaffolding | Stubs | Pending | Evaluate Tauri vs Electron footprint |
| **Data Engineering & Analytics** | **Low:** Specialized; evaluate client data scale requirements first. | Ongoing | Scaffolding | Stubs | Pending | Evaluate lightweight dbt-core patterns |
