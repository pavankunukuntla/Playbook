---
title: "Specialty: Web Applications and Websites"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../03-delivery-lifecycle/README.md"
  - "../04-engineering-standards/ux-ui-and-accessibility.md"
  - "../04-engineering-standards/security-and-privacy-engineering.md"
  - "../04-engineering-standards/ci-cd-and-release-engineering.md"
---

# Specialty: Web Applications and Websites

```yaml
specialty: web-applications-and-websites
activation_status: unconfirmed
prescribed_stack: none # Intentionally unconfirmed
```

## 1. Purpose
Explores the candidate technical requirements, constraints, and architecture considerations for delivering responsive web applications, single-page applications (SPAs), server-rendered portals, and high-performance marketing websites.

## 2. Proposed Scope
- Client-facing web applications, administrative portals, and SaaS dashboards.
- Content-managed marketing websites, headless CMS integrations, and landing pages.
- Client-side rendering (CSR), server-side rendering (SSR), and static site generation (SSG) patterns.
- Responsive layout design across modern mobile, tablet, and desktop viewports.
- Web accessibility conformance (WCAG 2.2 Level AA).
- Search engine optimization (SEO) technical baselines and Core Web Vitals optimization.

## 3. Applicability
Relevant when scoping, designing, or implementing web-based user interfaces. (Activation status: **unconfirmed**).

## 4. Related Documents
- Shared Lifecycle: [`../03-delivery-lifecycle/README.md`](../03-delivery-lifecycle/README.md).
- Engineering Standards:
  - [`../04-engineering-standards/ux-ui-and-accessibility.md`](../04-engineering-standards/ux-ui-and-accessibility.md): Accessibility and UI standards.
  - [`../04-engineering-standards/security-and-privacy-engineering.md`](../04-engineering-standards/security-and-privacy-engineering.md): Web security (XSS, CSRF, CSP headers).
  - [`../04-engineering-standards/ci-cd-and-release-engineering.md`](../04-engineering-standards/ci-cd-and-release-engineering.md): Front-end build and hosting pipelines.

## 5. Specialty-Specific Research Questions
- What default architectural patterns (e.g., SSR frameworks vs. static Jamstack with API backends) provide the best balance of developer velocity and client maintainability?
- How should headless CMS options (e.g., Sanity, Strapi, Contentful) be evaluated against client non-technical editor requirements?
- What automated testing frameworks (e.g., Playwright, Cypress) provide reliable E2E coverage without high maintenance overhead?

## 6. Known Unknowns
- Baseline client budget expectations for web application projects.
- Standard client expectations regarding legacy browser support (e.g., older Safari versions).
- Long-term hosting and domain management ownership models post-handover.

## 7. Candidate Evidence and Artifacts
- Web Application Architecture Checklist.
- Automated Core Web Vitals and Lighthouse CI audit configurations.
- WCAG 2.2 AA accessibility verification report template.

## 8. Next Action
Conduct trade-off research on primary modern web application architectures and headless CMS pairings.
