# Open Questions Register

This register documents unresolved architectural, operational, and commercial questions facing the agency.

> [!NOTE]
> Questions in this register require founder research, debate, and formal resolution. When a question is resolved, the decision should be recorded as an Operating Decision Record in [`decisions/`](./decisions/README.md) or incorporated into an approved policy/playbook, and this register updated accordingly.

---

## 1. Questions Register Table

| ID | Category | Domain | Question Summary | Priority | Status |
| :---: | :--- | :--- | :--- | :---: | :---: |
| **OQ-01** | `03 Strategy` | Core Offering | What exact technical services and target customer profiles (ICP) form our primary initial focus? | High | Open |
| **OQ-02** | `03 Strategy` | Governance | How are founder responsibilities and primary ownership divided across the 13 categories? | High | Open |
| **OQ-03** | `03 Strategy` | Decision Rights | What specific actions require unanimous founder consent versus individual delegated authority? | High | Open |
| **OQ-04** | `05 Sales` | Commercial Model | What service delivery and commercial models will we offer (fixed-scope, retainers, T&M, value-based)? | High | Open |
| **OQ-05** | `05 Sales` | Pricing Limits | What is our minimum acceptable engagement size, hourly floor, and discounting policy? | High | Open |
| **OQ-06** | `10 Finance` | Spend Controls | What specific financial approval thresholds and corporate card limits apply to founders and contributors? | High | Open |
| **OQ-07** | `10 Finance` | Cash Reserves | What minimum cash reserve target (e.g., 3 vs. 6 months operating expenses) will the agency maintain? | Medium | Open |
| **OQ-08** | `10 Finance` | Payment Terms | What are our standard payment terms (e.g., upfront deposit %, net terms, late payment interest)? | High | Open |
| **OQ-09** | `11 Delivery` | Client Support | What standard post-delivery warranty window and SLA commitments will be included in project SOWs? | Medium | Open |
| **OQ-10** | `01 Engineering` | Technology Stack | What are our default, sanctioned technology stacks for custom software and automation deliverables? | High | Open |
| **OQ-11** | `04 People` | Team Composition | What will be our initial operational staffing model (founders + freelancers/contractors vs. full-time hires)? | Medium | Open |
| **OQ-12** | `09 Operations` | Tool Ecosystem | Which project management (e.g., Linear, GitHub, Notion) and internal communication platforms will we standardize on? | Medium | Open |
| **OQ-13** | `13 Knowledge` | Notion vs Markdown | What is the definitive relationship, source of truth, and synchronization boundary between Notion and Markdown? | High | Open |
| **OQ-14** | `12 Legal/Risk` | Legal Counsel | Which licensed legal counsel and CPA firm will be retained to formalize commercial contracts and tax compliance? | High | Open |
| **OQ-15** | `12 Legal/Risk` | Secrets Hygiene | What enterprise password manager and 2FA enforcement mechanisms will be mandatory across all team members? | High | Open |
| **OQ-16** | `13 Knowledge` | Review Cadence | What periodic cadence (quarterly vs semi-annually) will govern systematic knowledge base audits and recertification? | Low | Open |

---

## 2. In-Depth Context for Critical Unresolved Decisions

### OQ-01: Exact Services and Target Customer Types
- **Context:** An agency attempting to offer "all software, all automation, to all businesses" lacks positioning power and repeatable delivery processes.
- **Trade-offs:** Highly bespoke custom software allows larger deal sizes but makes estimation and repeatability difficult. Productized automation or specialized integrations allow rapid delivery and marketing clarity, but may cap initial deal size.
- **Next Step:** Founder workshop to narrow the initial launch catalog to 1-2 core, high-confidence offerings.

### OQ-02 & OQ-03: Category Ownership & Founder Decision Rights
- **Context:** While one person may wear multiple hats across the 13 categories, ambiguity regarding who holds final authority leads to operational paralysis.
- **Trade-offs:** Requiring unanimous agreement on every hire, expense, or proposal slows execution. Delegating full autonomy without clear spending/contracting boundaries risks financial exposure.
- **Next Step:** Draft an Operating Decision Record establishing the *Founder Decision Rights & Authority Matrix*.

### OQ-04 & OQ-05: Pricing and Service Delivery Models
- **Context:** Different pricing models attract different buyers and require different project management controls.
- **Trade-offs:**
  - *Fixed-Price:* Attractive to clients with strict budgets; transfers scope and overrun risk entirely to the agency.
  - *Time & Materials (T&M):* Eliminates estimation risk for agency; transfers budget uncertainty to client.
  - *Monthly Retainers:* Provides predictable agency cash flow; requires strict boundaries to prevent scope creep.
- **Next Step:** Define standard engagement models and pricing floors in Category 05 (Sales) and Category 10 (Finance).

### OQ-06 & OQ-08: Financial Controls and Client Payment Terms
- **Context:** Early-stage agencies frequently fail from cash flow timing gaps (e.g., paying contractors Net-15 while clients pay Net-60).
- **Trade-offs:** Demanding 50% upfront deposits may encounter friction from enterprise procurement; offering generous terms strains working capital reserves.
- **Next Step:** Formulate formal policies in Category 10 (Finance) mandating deposit requirements before work commencement.

### OQ-13: Notion vs. Markdown Ownership
- **Context:** Notion is often favored for rapid brainstorming and visual drag-and-drop notes, while Git-backed Markdown provides version control, branch protection, code-adjacent documentation, and clean ingestion for AI coding agents.
- **Trade-offs:** Maintaining dual copies without bidirectional sync creates divergence. Building complex two-way sync integrations introduces fragility and maintenance overhead.
- **Next Step:** Evaluate adopting a clear one-way boundary (e.g., Notion for raw brainstorming/inbox; Git/Markdown as the sole canonical source of truth for approved operating documents). Record formal consensus in an ODR.
