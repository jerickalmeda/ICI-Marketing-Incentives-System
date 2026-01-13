<!--
SYNC IMPACT REPORT
==================
Version Update: 0.0.0 -> 1.0.0 (Initial Constitution Adoption)
Modified Principles:
  - Replaced generic template placeholders with specific project principles:
    1. Authority
    2. System Scope
    3. Data Integrity
    4. Incentive Rules
    5. Access Control
    6. User Experience
    7. Performance
    8. Compliance
    9. Extensibility
    10. Prohibited Practices
Added Sections:
  - Detailed Governance & Amendment Procedure (Section 11)
Removed Sections:
  - Generic template structure (Core Principles I-V)
Templates Status:
  - .specify/templates/plan-template.md: ✅ Compatible (Dynamic Constitution Check)
  - .specify/templates/spec-template.md: ✅ Compatible
  - .specify/templates/tasks-template.md: ✅ Compatible
Follow-up:
  - None
-->
# Constitution — ICI Marketing Incentives System

## 1. Authority of This Constitution
This document defines the **non-negotiable rules** governing the ICI Marketing Incentives System.

All specifications, implementation plans, task breakdowns, and code **must comply** with this constitution.  
In case of conflict, **this document takes precedence**.

## 2. System Scope & Intent
- This is an **internal institutional system** for Iligan Computer Institute.
- The system exists solely to **track, validate, and award recruitment-based incentives**.
- The system must **not function as or resemble a public MLM or referral platform**.

## 3. Data Integrity & Auditability

### 3.1 Auditability
- All recruitment, status, and incentive data **must be auditable**.
- Incentive origins must be **fully traceable** to recruitment events.
- Incentive computations must be **explainable and reproducible**.

### 3.2 Immutability Rules
- No silent data mutation is allowed.
- All status changes, incentive awards, reversals, or corrections **must be logged**.
- Historical records must remain accessible and intact.

### 3.3 Tree Integrity
- Recruitment relationships **must form a valid tree structure**.
- Cycles are strictly prohibited.
- A user **cannot exist simultaneously as upline and downline** within the same branch.

## 4. Incentive Rules Enforcement

- Incentives **must not be awarded immediately upon registration**.
- Incentives are awarded **only when eligibility conditions are met**.
- If a recruited student is:
  - **Cancelled** → no incentive
  - **Not Enrolled** → no incentive
- Incentive values:
  - Are **centrally configurable**
  - Must **never be hard-coded**

## 5. Role-Based Access Control

- Access must be strictly **role-based**.
- Users may only access data relevant to their role.
- Administrative actions must be:
  - Explicit
  - Logged
- Students and teachers:
  - Cannot alter incentive rules
  - Cannot manipulate recruitment hierarchies

## 6. User Experience Principles

- The system must prioritize **clarity over complexity**.
- Interfaces must be:
  - Intuitive
  - Purpose-built
  - Professional and non-generic
- Tree views must:
  - Be readable on mobile devices
  - Clearly communicate uplines and downlines

## 7. Performance & Connectivity Constraints

- The system must function under:
  - Low bandwidth conditions
  - Intermittent connectivity
- Critical operations must:
  - Fail safely
  - Never corrupt data

## 8. Privacy & Regulatory Compliance

- The system must comply with **Philippine data privacy regulations**.
- Personal data must:
  - Be accessed only when necessary
  - Be protected from unauthorized access
- The system is:
  - Internal-only
  - Not publicly accessible
  - Not usable without authentication

## 9. Extensibility Without Breakage

- Incentive rules may evolve over time.
- Recruitment statuses may expand.
- Historical data must remain valid, interpretable, and consistent.

## 10. Prohibited Practices

The following are strictly prohibited:
- Hard-coded incentive logic
- Unlogged administrative actions
- Automatic incentive awarding without validation
- Public referral sharing mechanisms
- UI patterns that obscure incentive computation logic

## 11. Governance

### Amendment Procedure
1. **Proposal**: Amendments must be submitted as a formal Pull Request.
2. **Review**: Changes must be reviewed by the system architect/owner.
3. **Approval**: Ratification requires explicit sign-off; silent merge is not ratification.
4. **Versioning**:
   - **Major**: Fundamental change to core rules (e.g., changing from MLM-prohibited to MLM-allowed).
   - **Minor**: New principle added or meaningful clarification.
   - **Patch**: Typo fixes or non-semantic wording changes.

### Compliance
- All new feature specifications must be cross-checked against this constitution.
- Non-compliant code must be rejected at review.
- The `plan-template` Constitution Check gate is mandatory.

**Version**: 1.0.0 | **Ratified**: 2026-01-13 | **Last Amended**: 2026-01-13
