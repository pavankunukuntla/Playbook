---
title: "Specialty: Desktop Applications"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../03-delivery-lifecycle/README.md"
  - "../04-engineering-standards/ci-cd-and-release-engineering.md"
  - "../04-engineering-standards/security-and-privacy-engineering.md"
---

# Specialty: Desktop Applications

```yaml
specialty: desktop-applications
activation_status: unconfirmed
prescribed_stack: none # Intentionally unconfirmed
```

## 1. Purpose
Explores the candidate technical requirements, cross-platform packaging, operating system integration constraints, and release engineering practices for delivering desktop applications across macOS, Windows, and Linux.

## 2. Proposed Scope
- Cross-platform desktop application frameworks (e.g., Tauri, Electron, Flutter Desktop).
- Operating system level integrations: file system access, local databases (SQLite), hardware peripherals, background tray processes.
- Desktop application packaging, bundling, and distribution (DMG, MSI/EXE, AppImage/DEB).
- Operating system code signing, certificate management, notarization (Apple Notarization, Windows SmartScreen).
- Secure auto-update mechanisms and differential patching.
- Local sandbox security, permissions, and inter-process communication (IPC) validation.

## 3. Applicability
Relevant when scoping, designing, or implementing native or cross-platform desktop software. (Activation status: **unconfirmed**).

## 4. Related Documents
- Shared Lifecycle: [`../03-delivery-lifecycle/README.md`](../03-delivery-lifecycle/README.md).
- Engineering Standards:
  - [`../04-engineering-standards/ci-cd-and-release-engineering.md`](../04-engineering-standards/ci-cd-and-release-engineering.md): Desktop cross-compilation and automated release packaging.
  - [`../04-engineering-standards/security-and-privacy-engineering.md`](../04-engineering-standards/security-and-privacy-engineering.md): OS permission boundaries and secure IPC.
  - [`../04-engineering-standards/environments-configuration-and-secrets.md`](../04-engineering-standards/environments-configuration-and-secrets.md): Code signing certificate security.

## 5. Specialty-Specific Research Questions
- Does Tauri provide sufficient ecosystem maturity and plugin support to serve as our primary desktop recommendation over Electron?
- What are the ongoing costs and operational complexities of maintaining Windows EV Code Signing certificates and Apple Developer accounts for client desktop software?
- How are auto-update servers and binary distribution endpoints best architected to minimize bandwidth costs?

## 6. Known Unknowns
- Commercial market demand for desktop-specific solutions compared to responsive web portals.
- Client technical capability to maintain desktop code signing and notarization workflows post-handover.
- Testing complexity across multiple OS versions and hardware variations.

## 7. Candidate Evidence and Artifacts
- Cross-Platform Desktop Packaging & CI Build Matrix.
- Apple Notarization & Windows Code Signing Verification Runbook.
- Desktop Secure Auto-Update & Rollback Protocol.

## 8. Next Action
Conduct comparative performance and binary footprint evaluation between Tauri and Electron.
