---
title: "Standard: Observability and Operational Readiness"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "./backup-recovery-and-incident-engineering.md"
  - "../03-delivery-lifecycle/11-operation-maintenance-and-technical-closure.md"
---

# Standard: Observability and Operational Readiness

## 1. Purpose
Establishes proposed standards for structured application logging, metrics collection, distributed tracing, proactive alerting, and operational readiness verification to ensure systems are observable in production.

## 2. Proposed Scope
- Structured logging standards: JSON-formatted logs with standardized metadata (timestamp, log level, correlation/trace ID, service name, environment).
- Absolute prohibition against logging sensitive PII, passwords, credit card numbers, or authorization headers.
- Health check endpoints: mandatory `/healthz` (liveness) and `/readyz` (readiness) probes verifying database and downstream service connectivity.
- Distributed tracing and Application Performance Monitoring (APM) standards using open formats (e.g., OpenTelemetry, Sentry, Datadog).
- Metric collection: tracking the Four Golden Signals (Latency, Traffic, Errors, Saturation).
- Proactive alerting hygiene: defining actionable alert thresholds, routing alerts to responsible channels (Slack, email, on-call paging), and preventing alert noise.
- Operational runbooks: mandatory troubleshooting steps linked directly in alert notifications.

## 3. Applicability
Applies to all backend services, web applications, background workers, and automation pipelines deployed to staging or production.

## 4. Related Documents
- [`./backup-recovery-and-incident-engineering.md`](./backup-recovery-and-incident-engineering.md): Incident handling.
- [`../03-delivery-lifecycle/11-operation-maintenance-and-technical-closure.md`](../03-delivery-lifecycle/11-operation-maintenance-and-technical-closure.md): Maintenance operations.

## 5. Questions to Research or Decide
- What default error tracking and observability platform (e.g., Sentry, OpenTelemetry + Grafana, Datadog) should be standardized for client projects?
- What log retention window (e.g., 14 days vs. 30 days) is appropriate for client applications without enterprise compliance mandates?
- Who receives operational alert notifications outside normal agency business hours?

## 6. Candidate Evidence and Artifacts
- Standard Logger Configuration Middleware (with PII redaction rules).
- Liveness and Readiness Probe Verification Endpoints.
- Operational Runbook Template for Production Alerts.

## 7. Next Action
Draft standard JSON logging middleware with automated PII masking for starter repos.
