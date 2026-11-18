# AI Contribution and Assistant Guidelines

This guide defines the mandatory rules, boundaries, and behavioral standards for any Artificial Intelligence (AI) assistant, autonomous agent, or language model contributing to, modifying, or reading this operating knowledge base.

---

## 1. Prime Directives for AI Contributors

Any AI assistant interacting with this repository must adhere strictly to the following 10 rules:

### Rule 1: Read Context Before Proposing Changes
Before generating or modifying documentation, you **MUST** read:
1. The root [`README.md`](./README.md) and [`structure-guide.md`](./structure-guide.md).
2. The specific `README.md` file of the category being modified.
3. Relevant existing templates in [`templates/`](./templates/README.md).

### Rule 2: Preserve the Agreed 13-Category Taxonomy
The 13 operational categories and their numeric prefixes (`01-development-and-engineering` through `13-knowledge-systems-and-automation`) are fixed.
- **DO NOT** rename, merge, delete, or introduce new top-level categories.
- Sub-disciplines belong as Markdown documents within their respective existing category folders.

### Rule 3: Rigorously Distinguish Proposals from Approved Instructions
- Draft material, candidate practices, and external research **MUST NEVER** be presented as binding or approved company rules.
- Maintain accurate metadata frontmatter at all times. Use `status: proposed` or `status: draft` for all newly authored work.
- Only human founders can authorize `status: approved`.

### Rule 4: Never Invent Facts, Sources, Owners, or Thresholds
- **DO NOT** invent external citations, benchmark data, client case studies, or legal requirements.
- **DO NOT** invent dollar thresholds, spending limits, pricing numbers, or staffing requirements.
- **DO NOT** invent founder assignments or review dates. If an owner or date is unknown, explicitly set `owner: null` (or `"unassigned"`) and `last_reviewed: null`.

### Rule 5: Always Use Standardized Templates
- When creating a new document, you must copy and follow the corresponding template from [`templates/`](./templates/README.md).
- Ensure all required template sections (Purpose, Scope, Inputs, Procedure, Exceptions, Escalation, Change History) are present.

### Rule 6: Link Instead of Duplicating
- Never copy procedures, checklists, or policies across multiple files.
- Establish the single source of truth in the owning category, and use relative Markdown links (e.g., linking directly to the owning category's policy file) from other documents.

### Rule 7: Record Uncertainties in Open Questions
- When encountering ambiguous requirements, conflicting trade-offs, or unmade operational decisions, explicitly record them in [`open-questions.md`](./open-questions.md) or the relevant category's Open Questions section.
- Do not make silent assumptions on behalf of the agency founders.

### Rule 8: Absolute Prohibition on Sensitive Information
This repository documents *how* sensitive assets are managed, not the assets themselves.
- **NEVER** write or commit real passwords, API tokens, private SSH keys, banking details, personal identification numbers, employee private records, or proprietary client data.
- Always use clearly labeled fictional placeholders (e.g., `sk-placeholder-token-do-not-use`, `user@example.com`).

### Rule 9: Human-in-the-Loop for Consequential Policy Changes
- Any document that imposes a mandatory obligation (Policy), commits agency resources, changes financial limits, or alters legal liabilities must be marked as `status: proposed` and flagged explicitly for human founder review.
- AI contributors cannot ratify company policy.

### Rule 10: Keep Changes Strictly Scoped
- Confine edits and additions strictly to the file(s) or category requested by the user.
- Do not perform sweeping refactors, directory renames, or unrequested file reorganizations without explicit human instruction.

---

## 2. Standard Metadata Verification Checklist for AI Output

Before completing any task that creates or edits a Markdown file, verify:

```yaml
---
title: "Descriptive Human Title"
document_type: policy | playbook | workflow | checklist | template | reference | research-note | decision-record | meeting-note | retrospective
category: "XX-category-name"
status: proposed # Never output approved unless validating existing approved text
owner: null # unassigned unless explicitly instructed
last_reviewed: null # unassigned unless explicitly instructed
related_documents:
  - "../relative/path/to/related.md"
---
```

- [ ] Frontmatter contains valid YAML syntax.
- [ ] Relative paths use forward slashes (`/`) and exact case matching.
- [ ] No placeholder links point to non-existent files.
- [ ] No confidential secrets or fabricated citations exist in the document body.
