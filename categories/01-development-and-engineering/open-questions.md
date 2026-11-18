---
title: "Development and Engineering Open Questions"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./coverage-matrix.md"
  - "../../open-questions.md"
---

# Development and Engineering Open Questions

This register tracks unresolved architectural, operational, and technical governance questions specific to the Development and Engineering category.

> [!NOTE]
> Resolving these questions requires collaborative discussion between engineering leads, commercial leads, and agency founders. Decisions will be formalized via Operating Decision Records (ODRs) or project ADRs.

---

## 1. Questions Register

| ID | Domain | Unresolved Technical Question | Impact / Risk | Status | Next Action |
| :---: | :--- | :--- | :--- | :---: | :--- |
| **ENG-Q01** | Stack Selection | What default programming languages, backend runtimes, and frontend frameworks constitute the agency's primary default tech stack? | High: Affects starter repos, hiring, and delivery velocity. | Open | Founder technical workshop |
| **ENG-Q02** | Cloud Ownership | Should client cloud infrastructure (AWS/GCP/PaaS) be provisioned under client-owned billing accounts or agency-managed master accounts? | High: Billing liability, credit card exposure, and handover complexity. | Open | Align with Finance & Legal |
| **ENG-Q03** | Code Review Model | What is our mandatory code review standard when a client project is staffed by a solo engineer? | High: Balance between review overhead and independent quality control. | Open | Evaluate cross-project peer reviews |
| **ENG-Q04** | Commercial Warranty | What standard warranty duration (e.g., 14 days vs. 30 days) is included post-launch for bug fixes before transitioning to a paid retainer? | High: Scope creep and unpaid support friction. | Open | Align with Sales & Delivery |
| **ENG-Q05** | Legacy Liability | What legal waiver and technical baseline protects the agency from pre-existing bugs and security vulnerabilities during codebase takeovers? | Critical: Unwarranted liability for third-party legacy flaws. | Open | Consult with Legal (Cat 12) |
| **ENG-Q06** | AI Code Governance | What contractual disclosure obligations exist regarding the use of AI coding assistants, and which enterprise data-sharing tiers are mandatory? | High: Client IP confidentiality and copyright concerns. | Open | Review vendor DPA terms |
| **ENG-Q07** | Migration Verification | Should CI pipelines strictly mandate automated down-migration verification for all relational database schema changes? | Medium: Migration safety vs. developer CI pipeline speed. | Open | Pilot on Tier 3 projects |
| **ENG-Q08** | On-Call & SLAs | How will after-hours on-call support be staffed, rotated, and compensated for client maintenance retainers? | Medium: Team burnout and SLA breach penalties. | Open | Align with People & Finance |
| **ENG-Q09** | Domain & DNS Billing | Who registers and pays for client production domains, SSL certificates, and DNS services post-handover? | Medium: Recurring billing disputes and account ownership transfer. | Open | Align with Finance & Delivery |
| **ENG-Q10** | Pre-Commit Hooks | Should local pre-commit secret scanning hooks (e.g., Gitleaks) be enforced via repository configs or left to individual developer choice? | High: Preventing accidental secret leakage before remote push. | Open | Standardize in starter repos |

---

## 2. In-Depth Context on Priority Decisions

### ENG-Q01: Default Technology Stack Selection
- **Context:** Delivering technical excellence as a boutique agency requires focus. Spreading in-house knowledge across too many disparate stacks (e.g., Python + Django, TypeScript + Next.js, Go + HTMX, Ruby on Rails, PHP + Laravel) dilutes code review rigor and prevents reusable component libraries.
- **Trade-offs:** A unified TypeScript/JavaScript full-stack ecosystem (e.g., Next.js/React + Node.js/TypeScript + PostgreSQL) maximizes full-stack code reuse and shared context. However, specialized domains (AI pipelines, high-concurrency microservices, data engineering) frequently benefit from Python or Go.
- **Proposed Direction:** Standardize on TypeScript as the default language for web, mobile, and standard APIs; designate Python as the secondary sanctioned language for AI, data pipelines, and automation scripting.

### ENG-Q02: Cloud Infrastructure & Billing Account Ownership
- **Context:** When deploying staging and production infrastructure for a client, two commercial models exist:
  1. *Client-Owned:* Client creates their own AWS/GCP/Vercel organization, inputs their own credit card, and invites agency engineers as IAM users.
  2. *Agency-Managed:* Agency hosts the client on its own multi-tenant agency cloud account and re-bills the client monthly with a markup.
- **Trade-offs:** Client-owned accounts completely eliminate agency billing liability and simplify handover. However, clients frequently face procurement bottlenecks creating their own accounts. Agency-managed hosting creates cash flow exposure if a client disputes a bill or defaults.
- **Proposed Direction:** Default to client-owned cloud accounts for production deliverables; provide ephemeral agency staging environments strictly during active development.

### ENG-Q04: Post-Launch Warranty vs. Ongoing Maintenance
- **Context:** Clients frequently expect "free lifetime bug fixes" for any issue discovered after launch, leading to disputes over whether a bug is a defect in the original SOW or an environmental change (e.g., third-party API update, browser deprecation).
- **Trade-offs:** A generous warranty (e.g., 60 days) builds client goodwill but creates open-ended unpaid developer commitments. A short warranty (e.g., 14 days) requires strict acceptance testing discipline.
- **Proposed Direction:** A strict 14-day post-launch warranty limited to defects reproducing against original written acceptance criteria, followed by a mandatory transition to a monthly maintenance retainer for ongoing support.
