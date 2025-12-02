# HDF5 Safety, Security & Privacy (SSP) SIG — Charter

## 1. Purpose

The SSP SIG exists to advance the safety, security, and privacy posture of
the HDF5 library, file format, and ecosystem by:

- Coordinating community expertise across implementations and deployments.
- Setting shared, practical practices and default configurations.
- Driving actionable improvements in code, documentation, tooling, and
  operations.

## 2. Scope

### 2.1 In scope

- **Standards & Guidance**
  - Secure defaults and hardening recommendations.
  - Coding standards for SSP-relevant changes.
  - Privacy-by-design recommendations for data stored in HDF5.

- **Risk & Audit**
  - Taxonomy of threats and vulnerabilities across:
    - File format
    - Library
    - Library extensions (filters, VFDs, VOL connectors, bindings)
    - Toolchain and dependencies
    - Operational and usage patterns
    - Privacy and data handling
    - Supply chain and distribution
  - Minimum audit checklist and periodic review cycles.

- **Incident Readiness**
  - Vulnerability intake and triage workflows.
  - Coordinated disclosure and embargo handling.
  - Release hygiene (changelogs, SBOM guidance).

- **Education & Outreach**
  - Patterns and anti-patterns, reference configs, sample code.
  - Short primers and best-practice guides.

- **Ecosystem Interfaces**
  - Guidance for connectors, filters, VFDs, VOL connectors, and packaging.

### 2.2 Out of scope

- Routine product management or feature prioritization unrelated to SSP.
- Vendor-specific procurement or sales activities.
- Formal compliance certifications (e.g., FedRAMP) beyond technical input.

## 3. Membership & Roles

### 3.1 Membership

- **Open membership** for individuals and organizations who agree to:
  - The project’s Code of Conduct.
  - The responsibilities listed in this charter.

- **Voting members** are those who:
  - Have attended at least two meetings in the last rolling quarter; and
  - Have made at least one substantive contribution (PR, doc, issue triage,
    or agenda item) in that period.

### 3.2 Roles

- **Chair (1)**
  - Curates agendas and facilitates meetings.
  - Ensures follow-through on actions.

- **Vice-Chair (1)**
  - Backup to the Chair.
  - Coordinates working sessions and subgroups.

- **Secretary (1)**
  - Maintains minutes, decision log, and action tracker.
  - Ensures public artifacts are discoverable.

- **Editors (2–4)**
  - Maintain SSP guides, checklists, and templates.

- **Liaisons (as needed)**
  - Serve as points-of-contact to related working groups (release, packaging,
    docs, bindings, HSDS, etc.).

Role terms are **6 months**, renewable, and selected by voting members.

## 4. Operating Rhythm

- **Regular meetings:** e.g., bi-weekly 60-minute calls.
- **Quarterly review:** longer session to review metrics, backlog, and roadmap.
- **Artifacts:**
  - SSP Handbook (living documentation).
  - Minimum audit checklist and guidance.
  - Threat catalogs, mitigations, and reference configurations.
  - Decision log (see `DECISION_LOG.md`).

Meeting agendas and minutes are published in this repository via GitHub issues,
except for sensitive security content, which is handled under the disclosure
policy in `SECURITY.md`.

## 5. Decision-Making

- **Default mode:** rough consensus after a written proposal and a minimum
  comment period (e.g., 72 hours).
- **Formal vote:** simple majority of voting members present; quorum is 50%
  of voting members.
- **Fast-track:** Chairs may approve low-risk editorial updates,
  recorded in the decision log.
- **Appeals:** any voting member may request reconsideration at the next
  meeting with new information.

## 6. Workstreams

Work typically begins with a **Proposal** issue using the SSP Proposal template.

Common workstreams include (but are not limited to):

- Secure defaults and hardening guidance.
- Vulnerability disclosure and triage workflow.
- SBOM and supply-chain guidance.
- Privacy patterns and data-handling guidance.
- Ecosystem and connector guidance.
- Audit and readiness exercises.

## 7. Code of Conduct & Antitrust

The SSP SIG adheres to the project-wide Code of Conduct (see
`CODE_OF_CONDUCT.md`) and avoids discussion of pricing, customer
allocation, or other anti-competitive topics.

## 8. Effective Date & Review

- **Effective date:** _[to be filled in at first ratification]_.
- The charter is reviewed and re-ratified every **6 months** or as needed.
