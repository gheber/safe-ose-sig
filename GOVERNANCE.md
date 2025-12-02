# SSP SIG Governance

This document explains how the SSP SIG organizes its work and evolves
over time.

## 1. Relationship to the HDF5 Project

The SSP SIG is a community body focused on safety, security, and privacy
concerns across the HDF5 ecosystem. It operates under the broader
governance of the HDF5 project and coordinates with:

- Core maintainers of the HDF5 library.
- Related projects (e.g., HSDS, tools, bindings, ecosystem libraries).
- HDFG as a steward of the ecosystem.

## 2. Roles and Selection

Roles are defined in `CHARTER.md`. This document adds the selection and
replacement procedures.

### 2.1 Selection

- Any voting member may nominate themselves or be nominated (with consent).
- If multiple candidates exist for a role, an online or meeting-based vote
  is held among voting members.
- Simple majority of votes cast is sufficient.

### 2.2 Vacancies and Replacement

- If a role becomes vacant mid-term, the Chair (or Vice-Chair if Chair is
  vacant) initiates a replacement process.
- Temporary acting roles may be assigned for up to one meeting.

## 3. Decision Lifecycle

Decisions typically follow this path:

1. **Intake**
   - A GitHub issue is opened using the **SSP Proposal** template or
     a related template.
2. **Discussion**
   - Comments and feedback are collected asynchronously.
   - The item is added to a meeting agenda if a decision or direction
     is needed.
3. **Decision**
   - Consensus is sought first; if needed, a vote is taken.
   - The outcome is recorded in:
     - The original issue; and
     - `DECISION_LOG.md`.
4. **Implementation**
   - Work items are tracked as issues and PRs.
5. **Review**
   - Relevant maintainers and SIG members review completed work.

## 4. Transparency

- Meetings are announced publicly with agenda links.
- Minutes and decisions are recorded using the "SSP SIG Meeting Minutes."
  issue template (except for sensitive security details).
- Governance changes (including changes to this document or `CHARTER.md`)
  must be:
  - Proposed via GitHub issue.
  - Discussed with at least one meeting.
  - Approved with consensus or a recorded vote.

## 5. Conflict Resolution

- Minor disagreements are handled through discussion and clarification.
- If consensus cannot be reached:
  - A vote among voting members is held.
  - If the outcome is still contentious, the issue may be escalated to
    the broader HDF5 project governance for advice or final decision.

## 6. Amending this Document

- Proposed changes are submitted as pull requests referencing a GitHub issue.
- A minimum review period (e.g., 7 days) is recommended.
- Approval requires:
  - At least two approvals from voting members; and
  - No blocking objections from Chairs.
