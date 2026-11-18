---
title: "Standard: Performance and Capacity"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./observability-and-operational-readiness.md"
  - "../02-service-specialties/web-applications-and-websites.md"
  - "../03-delivery-lifecycle/08-verification-and-client-acceptance.md"
---

# Standard: Performance and Capacity

## 1. Purpose
Establishes proposed standards for application performance engineering, response latency targets, Core Web Vitals compliance, caching strategies, and infrastructure capacity sizing.

## 2. Proposed Scope
- Latency objectives: target API p95 response times under 250ms for standard database queries; background job processing targets.
- Front-end performance: Google Core Web Vitals thresholds (Largest Contentful Paint < 2.5s, Interaction to Next Paint < 200ms, Cumulative Layout Shift < 0.1).
- Asset optimization: responsive image formats (WebP, AVIF), font subsetting, bundle tree-shaking, and code splitting.
- Caching architectures: edge CDN caching, HTTP cache-control headers, stale-while-revalidate patterns, and server-side Redis caching.
- Database query performance: detecting N+1 query antipatterns, missing indexes, and unpaginated list responses.
- Load and stress testing: using lightweight tools (e.g., k6, autocannon) to verify system behavior under expected peak concurrent user loads.

## 3. Applicability
Applies to web applications, public APIs, high-volume data pipelines, and client deliverables requiring defined performance SLAs.

## 4. Related Documents
- [`./observability-and-operational-readiness.md`](./observability-and-operational-readiness.md): APM and latency monitoring.
- [`../02-service-specialties/web-applications-and-websites.md`](../02-service-specialties/web-applications-and-websites.md): Web performance.
- [`../03-delivery-lifecycle/08-verification-and-client-acceptance.md`](../03-delivery-lifecycle/08-verification-and-client-acceptance.md): Verification stage.

## 5. Questions to Research or Decide
- What automated performance budget tool (e.g., Lighthouse CI) should run on pull requests?
- When is a formal load test using k6 mandatory prior to client production release?
- How do we calculate and communicate infrastructure autoscaling limits to clients to prevent unexpected cloud bills?

## 6. Candidate Evidence and Artifacts
- Lighthouse CI Automated Performance Budget Report.
- Load and Concurrency Stress Test Results (k6 report).
- Production Capacity Sizing & Cost Estimate Worksheet.

## 7. Next Action
Draft k6 baseline load test script for standard API endpoints and configure Lighthouse CI.
