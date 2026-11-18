---
title: "Specialty: Mobile Applications"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../03-delivery-lifecycle/README.md"
  - "../04-engineering-standards/api-and-integration-engineering.md"
  - "../04-engineering-standards/ci-cd-and-release-engineering.md"
---

# Specialty: Mobile Applications

```yaml
specialty: mobile-applications
activation_status: unconfirmed
prescribed_stack: none # Intentionally unconfirmed
```

## 1. Purpose
Explores the candidate technical requirements, constraints, and release engineering challenges for delivering native or cross-platform mobile applications for iOS and Android.

## 2. Proposed Scope
- Cross-platform mobile development (e.g., React Native, Flutter) and native platform considerations.
- Mobile client architecture, offline storage, local caching, and synchronization.
- Push notification infrastructure and device permission handling.
- App store compliance (Apple App Store Review Guidelines, Google Play Developer Policies).
- Code signing, provisioning profiles, keystore management, and certificate rotation.
- Mobile distribution channels (TestFlight, Google Play Internal Testing, public store releases).

## 3. Applicability
Relevant when scoping, developing, or maintaining client mobile applications. (Activation status: **unconfirmed**).

## 4. Related Documents
- Shared Lifecycle: [`../03-delivery-lifecycle/README.md`](../03-delivery-lifecycle/README.md).
- Engineering Standards:
  - [`../04-engineering-standards/api-and-integration-engineering.md`](../04-engineering-standards/api-and-integration-engineering.md): Mobile-optimized backend endpoints.
  - [`../04-engineering-standards/ci-cd-and-release-engineering.md`](../04-engineering-standards/ci-cd-and-release-engineering.md): Mobile build pipelines (Fastlane, cloud builders).
  - [`../04-engineering-standards/environments-configuration-and-secrets.md`](../04-engineering-standards/environments-configuration-and-secrets.md): Keystore and certificate security.

## 5. Specialty-Specific Research Questions
- What cross-platform mobile framework best aligns with the agency's existing engineering skill profile?
- How do we structure client contracts to account for unpredictable app store review delays and rejection risks?
- What mobile crash reporting and telemetry tools (e.g., Sentry, Firebase Crashlytics) should be standard?
- How should over-the-air (OTA) updates (e.g., Expo EAS Update) be governed to avoid app store policy violations?

## 6. Known Unknowns
- Client organizational readiness to maintain Apple Developer Program and Google Play Console accounts.
- In-house technical capability depth for native iOS/Android bridge debugging.
- Long-term maintenance cost models for OS version deprecations and hardware updates.

## 7. Candidate Evidence and Artifacts
- App Store Submission & Compliance Checklist.
- Mobile Keystore and Provisioning Profile Security Runbook.
- Mobile Release Verification Test Matrix.

## 8. Next Action
Evaluate whether mobile development should be offered directly or initially delivered via responsive web applications and PWAs.
