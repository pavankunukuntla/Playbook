---
title: "Specialty: Cloud and Platform Engineering"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../03-delivery-lifecycle/README.md"
  - "../04-engineering-standards/ci-cd-and-release-engineering.md"
  - "../04-engineering-standards/environments-configuration-and-secrets.md"
  - "../04-engineering-standards/security-and-privacy-engineering.md"
---

# Specialty: Cloud and Platform Engineering

```yaml
specialty: cloud-and-platform-engineering
activation_status: unconfirmed
prescribed_stack: none # Intentionally unconfirmed
```

## 1. Purpose
Explores the candidate technical requirements, infrastructure-as-code practices, cloud security postures, and environment management architectures for delivering scalable cloud infrastructure and internal developer platforms.

## 2. Proposed Scope
- Cloud infrastructure architecture (AWS, Google Cloud, Azure, Hetzner, modern PaaS).
- Infrastructure as Code (IaC) tooling (e.g., Terraform, OpenTofu, Pulumi, AWS CDK).
- Containerization and orchestration (Docker, Docker Compose, Kubernetes, ECS, Nomad).
- Serverless architecture (Cloud Run, AWS Lambda, edge functions).
- Networking, DNS, TLS/SSL certificates, CDN routing, and Web Application Firewalls (WAF).
- Cloud security posture management (least-privilege IAM, security groups, VPC isolation).
- Cloud billing management, cost monitoring, budget alerts, and resource tagging.
- Automated provisioning of isolated ephemeral preview, staging, and production environments.

## 3. Applicability
Relevant when provisioning, migrating, securing, or managing cloud environments. (Activation status: **unconfirmed**).

## 4. Related Documents
- Shared Lifecycle: [`../03-delivery-lifecycle/README.md`](../03-delivery-lifecycle/README.md).
- Engineering Standards:
  - [`../04-engineering-standards/ci-cd-and-release-engineering.md`](../04-engineering-standards/ci-cd-and-release-engineering.md): Deployment pipeline automation.
  - [`../04-engineering-standards/environments-configuration-and-secrets.md`](../04-engineering-standards/environments-configuration-and-secrets.md): Cloud secrets and configuration.
  - [`../04-engineering-standards/security-and-privacy-engineering.md`](../04-engineering-standards/security-and-privacy-engineering.md): Cloud network security and IAM.

## 5. Specialty-Specific Research Questions
- What default cloud deployment model (managed PaaS like Vercel/Fly.io vs. hyperscaler container platforms like AWS ECS / GCP Cloud Run) best minimizes agency operational overhead?
- How should cloud accounts be structured between the agency and the client (client-owned billing account vs. agency-managed pass-through)?
- What IaC framework provides the most maintainable codebase for non-specialist client engineers post-handover?

## 6. Known Unknowns
- Client internal capability to maintain Kubernetes clusters or complex Terraform modules after project exit.
- Commercial liability for cloud infrastructure security breaches post-handover.
- Cloud cost variability and spike protection policies.

## 7. Candidate Evidence and Artifacts
- Infrastructure as Code (IaC) Baseline Terraform / OpenTofu Modules.
- Cloud Account IAM Least-Privilege Baseline Architecture.
- Cloud Infrastructure Transfer & Billing Migration Checklist.

## 8. Next Action
Formulate architectural recommendation on client-owned vs. agency-managed cloud account ownership models.
