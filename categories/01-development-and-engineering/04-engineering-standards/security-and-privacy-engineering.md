---
title: "Standard: Security and Privacy Engineering"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../00-research-and-validation/evidence-register.md"
  - "./environments-configuration-and-secrets.md"
  - "../../12-legal-security-and-risk-management/README.md"
---

# Standard: Security and Privacy Engineering

## 1. Purpose
Establishes proposed technical standards for secure software development, threat modeling, protection against common web vulnerabilities (OWASP Top 10), cryptographic baselines, and data privacy by design.

## 2. Proposed Scope
- Threat modeling during solution design (identifying assets, trust boundaries, attack vectors, and mitigations).
- Defenses against the OWASP Top 10:
  - Injection prevention: mandatory parameterized queries / ORMs, zero raw string concatenation in SQL.
  - Authentication and session security: secure cookie flags (`HttpOnly`, `Secure`, `SameSite=Lax/Strict`), robust password hashing (Argon2id or bcrypt).
  - Cross-Site Scripting (XSS) and Cross-Site Request Forgery (CSRF) defenses: context-aware output encoding, Content Security Policy (CSP) headers.
  - Broken Access Control: mandatory server-side authorization checks on every endpoint (never trusting client parameters).
- Cryptographic standards: TLS 1.3 in transit, AES-GCM-256 at rest, modern key derivation.
- Automated security testing in CI: Static Application Security Testing (SAST) and container vulnerability scanning.
- Data privacy engineering: data minimization, PII masking, audit logging of sensitive access, and GDPR right-to-be-forgotten mechanics.

## 3. Applicability
Universal across all software, infrastructure, and automation deliverables, tailored according to project risk tier.

## 4. Related Documents
- [`../00-research-and-validation/evidence-register.md`](../00-research-and-validation/evidence-register.md): NIST SP 800-218 (Produce Well-Secured Software).
- [`./environments-configuration-and-secrets.md`](./environments-configuration-and-secrets.md): Secrets hygiene.
- [`../../12-legal-security-and-risk-management/README.md`](../../12-legal-security-and-risk-management/README.md): Organizational security policy and compliance.

## 5. Questions to Research or Decide
- What automated SAST tool (e.g., Semgrep, SonarQube, CodeQL) provides actionable alerts with low false-positive rates?
- When is a third-party penetration test required for a client project prior to commercial release?
- What is our internal procedure for receiving and resolving security vulnerability reports from external researchers?

## 6. Candidate Evidence and Artifacts
- Project Threat Model & Security Architecture Document.
- Automated CI SAST / SCA Security Scan Log.
- Pre-Release Security Verification Checklist.

## 7. Next Action
Configure automated Semgrep rulesets covering OWASP Top 10 in agency repository templates.
