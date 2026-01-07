# Security Policy — <PROJECT_NAME>

**Document ID:** SECURITY.md  
**Security Policy Version:** v1.0  
**Last Reviewed:** <YYYY-MM-DD>  
**Applies To:** <ORG>/<REPO> (default branch: <BRANCH>)  
**Aligned Framework:** HDF5 SSP SIG Policy Manual (Control Set: <SAFE_OSE_CONTROL_SET_VERSION>)

---

## 1. Purpose

This document explains how to report security issues for **<PROJECT_NAME>**, what versions are supported, and what you can expect from our vulnerability response process.

> **Do not** file public issues for suspected vulnerabilities.

---

## 2. Scope

In scope:
- Vulnerabilities in this repository’s source code, build artifacts, official releases, and official documentation.
- Supply-chain issues directly affecting official artifacts we publish (e.g., compromised release pipeline, signing keys, or distributed binaries).

Out of scope (unless demonstrably impacts this project’s official artifacts):
- Vulnerabilities in **third‑party dependencies** (report to upstream first; you may notify us if exploitation materially affects <PROJECT_NAME> users).
- Vulnerabilities requiring unrealistic configurations or non-default threat assumptions (we will still review, but severity may differ).

---

## 3. Definitions

- **Vulnerability:** A weakness that can be exploited to impact confidentiality, integrity, or availability.
- **Security Incident:** A confirmed compromise or active exploitation affecting project users, infrastructure, signing keys, or release artifacts.
- **Coordinated Disclosure:** A private reporting + remediation period before public disclosure, coordinated with the reporter.
- **PSIRT:** Product Security Incident Response Team (or designated security responders for this project).

---

## 4. Supported Versions & Security Fix Policy (HDF5-SHINES-COMPAT)

| Version Line | Supported for Security Fixes? | Notes |
|---|---:|---|
| <e.g., 1.14.x latest patch> | ✅/❌ | <policy> |
| <e.g., 1.12.x> | ✅/❌ | <policy> |
| <e.g., 1.10.x> | ✅/❌ | <policy> |

**Security fix policy:**
- We provide security fixes for: <e.g., “latest stable release only” / “latest + LTS line(s)”>.
- When a fix is released, we will document it in: <release notes / advisories location>.
- If a vulnerability only affects unsupported versions, we may still publish guidance/workarounds.

---

## 5. Reporting a Vulnerability (HDF5-SHINES-VULN)

### 5.1 Preferred reporting channel (private)
Use one of the following **private** channels:

1) **GitHub Security Advisories (preferred):**  
   Create a private report at: `<https://github.com/HDFGroup/<REPO>/security/advisories/new>`

2) **Security email (fallback):**  
   Send to: `<SECURITY_CONTACT_EMAIL>`  
   Optional PGP key / fingerprint: `<PGP_FINGERPRINT_OR_LINK>`

If you are unsure whether your finding is a vulnerability, please still report privately.

### 5.2 What to include
To help us triage quickly, include:
- Affected component(s) and versions/commit(s)
- Impact assessment (what an attacker can gain/do)
- Reproduction steps or proof-of-concept (PoC), if available
- Any constraints (platform, compiler, environment, file samples)
- Suggested fix or mitigation, if you have one

> Please avoid sharing sensitive data. If you must share a malicious file sample, clearly label it and include minimal reproduction steps.

---

## 6. What to Expect from Us (HDF5-SHINES-VULN / HDF5-SHINES-IR)

We aim to:
- **Acknowledge** receipt within: <X business days>
- Provide an **initial triage** (severity + next steps) within: <Y business days>
- Coordinate on a **fix and disclosure plan**, including whether a CVE/GHSA will be issued
- Provide **credit** in advisories/releases if desired (unless you request anonymity)

We may ask for additional details or testing help during remediation.

---

## 7. Disclosure Policy (HDF5-SHINES-VULN)

- We practice **coordinated disclosure**. Please do not publicly disclose details until we agree on timing.
- We may publish:
  - A **GitHub Security Advisory (GHSA)** and/or
  - A **CVE** (assignment handled by: <ORG_CVE_PROCESS>)
- We will strive to publish enough detail for users to mitigate while avoiding unnecessary exploit enablement.

---

## 8. Secure Build, Provenance, and Distribution (HDF5-SHINES-BUILD)

For official releases, we aim to provide (where applicable):
- **Signed** release artifacts and/or packages (method: <codesigning/sigstore/gpg>)
- **Checksums** (e.g., SHA-256) for downloadable artifacts
- **SBOM** (software bill of materials) for releases (format: <SPDX/CycloneDX>)
- Provenance/attestations (e.g., SLSA) when available

Where to verify official artifacts:
- Official releases page: `<RELEASES_URL>`
- Checksums/signatures: `<CHECKSUMS_OR_SIGNATURES_URL>`
- Provenance/attestations: `<PROVENANCE_URL>`

> Only trust binaries obtained from official channels listed above.

---

## 9. Dependency & Licensing Security (HDF5-SHINES-DEP)

We manage dependency risk by:
- Tracking third-party dependencies (including transitive dependencies where feasible)
- Monitoring vulnerability disclosures (e.g., OSV/NVD/GHSA) for relevant components
- Reviewing licensing impacts for redistributed components (policy reference: Safe‑OSE HDF5-SHINES-DEPS)

Where to find dependency inventories/SBOMs:
- `<SBOM_LOCATION_IN_REPO_OR_RELEASES>`
- `<DEPENDENCY_MANIFEST_PATHS>`

---

## 10. Security Testing & Fuzzing (HDF5-SHINES-TEST)

We use (as applicable):
- Static analysis: <tooling>
- Dynamic analysis / sanitizers: <tooling>
- Fuzzing: <tooling or OSS-Fuzz link>
- Regression tests for past vulnerabilities

Where to find evidence:
- CI workflows: `<.github/workflows/...>`
- Fuzz harnesses/tests: `<path>`
- Sanitizer configs: `<path>`

---

## 11. Plugin & Extension Governance (HDF5-SHINES-PLUG)

If <PROJECT_NAME> supports plugins/extensions (e.g., filters, connectors, drivers), we treat them as part of the security boundary.

Policy highlights:
- Plugins/extensions must have clear ownership/maintainers.
- Officially distributed plugins must have documented provenance and integrity protections.
- The project may support **integrity verification** for plugins (e.g., digital signatures) where feasible.

Where to find plugin governance details:
- Plugin registry/list: `<URL_OR_PATH>`
- Signing/verification instructions: `<URL_OR_PATH>`
- Loading controls / allowlists: `<URL_OR_PATH>`

---

## 12. Cryptography and Key Management (HDF5-SHINES-CRYPTO)

If the project uses cryptography (signing, encryption, TLS, etc.):
- We prefer modern, well-reviewed crypto libraries and algorithms.
- Keys used for signing official artifacts are protected and access-controlled.
- We rotate/revoke keys when compromise is suspected.

Where to find crypto details:
- Cryptography design notes: `<URL_OR_PATH>`
- Public signing keys: `<URL_OR_PATH>`

---

## 13. Secure Configuration & Hardening (HDF5-SHINES-HARD)

We provide guidance for secure use and deployment, including:
- Recommended secure defaults (when feasible)
- Hardening guidance (e.g., least privilege, sandboxing, input handling practices)
- Network/service hardening (if applicable)

Where to find secure configuration guidance:
- Security hardening guide: `<URL_OR_PATH>`
- Deployment docs: `<URL_OR_PATH>`

---

## 14. Incident Response & Evidence Retention (HDF5-SHINES-IR)

If you believe there is an **active incident** (compromised releases, leaked signing keys, in-the-wild exploitation), report immediately via the channels in Section 5 and include “URGENT” in the subject.

We will:
- Triage and contain the incident
- Preserve relevant evidence (logs/artifacts) according to HDF5 SSP policy
- Communicate remediation guidance to users as appropriate

---

## 15. Security Announcements

We publish security updates via:
- GitHub advisories: `<https://github.com/HDFGroup/<REPO>/security/advisories>`
- Release notes: `<RELEASE_NOTES_URL>`
- Project channels (optional): `<MAILING_LIST_OR_FORUM>`

---

## 16. Repo-Specific Overrides (REQUIRED)

This section lists **only** the ways this repository deviates from the HDF5 SSP policy default posture.

### 16.1 Overrides Summary
- **Supported versions policy differs?** <yes/no + explanation>
- **Reporting channel differs?** <yes/no + explanation>
- **Disclosure timeline differs?** <yes/no + explanation>
- **Artifact signing/provenance differs?** <yes/no + explanation>
- **Plugin model differs?** <yes/no + explanation>
- **Deployment hardening differs?** <yes/no + explanation>

### 16.2 Product Notes
<Describe product-specific threat model considerations and key security boundaries in 5–10 bullets.>

---

## 17. HDF5-SHINES Control Alignment (AUDIT-AID)

This file provides evidence/coverage for the following HDF5‑SHINES controls:

| Safe‑OSE Control ID | Control Name | Covered Here? | Section(s) |
|---|---:|---:|---|
| HDF5-SHINES-VULN-01 | Vulnerability intake (private channel) | ✅ | 5 |
| HDF5-SHINES-VULN-02 | Coordinated disclosure | ✅ | 7 |
| HDF5-SHINES-COMP-01 | Supported versions & security fixes | ✅ | 4 |
| HDF5-SHINES-IR-01 | Incident reporting + escalation | ✅ | 14 |
| HDF5-SHINES-BUILD-01 | Secure distribution & verification | ✅ | 8 |
| HDF5-SHINES-DEP-01 | Dependency risk management pointers | ✅ | 9 |
| HDF5-SHINES-TEST-01 | Security testing/fuzzing pointers | ✅ | 10 |
| HDF5-SHINES-PLUG-01 | Plugin governance pointers | ✅/N/A | 11 |
| HDF5-SHINES-CRYPTO-01 | Crypto/key management pointers | ✅/N/A | 12 |
| HDF5-SHINES-HARD-01 | Secure configuration guidance | ✅/N/A | 13 |

For the authoritative requirements, see the [HDF5 SSP SIG Policy Manual](../policy/README.md).
