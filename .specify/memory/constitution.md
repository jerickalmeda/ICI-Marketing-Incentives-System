# ICI Marketing Incentives System Constitution

<!--
Sync Impact Report

- Version change: template (unversioned) -> 1.0.0
- Modified principles: N/A (initial adoption)
- Added sections: Core Principles, Non-Functional Constraints, Development Expectations, Governance
- Removed sections: N/A
- Templates requiring updates:
	- .specify/templates/plan-template.md (UPDATED)
	- .specify/templates/spec-template.md (UPDATED)
	- .specify/templates/tasks-template.md (UPDATED)
	- .specify/templates/checklist-template.md (UPDATED)
	- .specify/templates/commands/*.md (CREATED + UPDATED)
- Deferred items:
	- TODO(RATIFICATION_DATE): original adoption date not present in repo context yet
-->

## Core Principles

### 1. Authority of This Constitution
This document defines the non-negotiable rules governing the ICI Marketing Incentives System.

All specifications, implementation plans, task breakdowns, and code MUST comply with this constitution.
If any document or implementation conflicts with this constitution, this document takes precedence.

### 2. System Scope & Intent
- The system is an internal institutional system for Iligan Computer Institute.
- The system exists solely to track, validate, and award recruitment-based incentives.
- The system MUST NOT function as or resemble a public MLM or referral platform.

### 3. Data Integrity & Auditability

**Auditability**
- All recruitment, status, and incentive data MUST be auditable.
- Incentive origins MUST be fully traceable to recruitment events.
- Incentive computations MUST be explainable and reproducible.

**Immutability Rules**
- No silent data mutation is allowed.
- All status changes, incentive awards, reversals, or corrections MUST be logged.
- Historical records MUST remain accessible and intact.

**Tree Integrity**
- Recruitment relationships MUST form a valid tree structure.
- Cycles are strictly prohibited.
- A user MUST NOT exist simultaneously as upline and downline within the same branch.

### 4. Incentive Rules Enforcement
- Incentives MUST NOT be awarded immediately upon registration.
- Incentives MUST be awarded only when eligibility conditions are met.
- If a recruited student is:
	- Cancelled -> no incentive
	- Not Enrolled -> no incentive
- Incentive values MUST be centrally configurable and MUST never be hard-coded.

### 5. Role-Based Access Control
- Access MUST be strictly role-based.
- Users MUST only access data relevant to their role.
- Administrative actions MUST be explicit and MUST be logged.
- Students and teachers MUST NOT be able to alter incentive rules or manipulate recruitment hierarchies.

### 6. User Experience Principles
- The system MUST prioritize clarity over complexity.
- Interfaces MUST be intuitive, purpose-built, and professional (non-generic).
- Tree views MUST be readable on mobile devices and MUST clearly communicate uplines and downlines.

### 7. Performance & Connectivity Constraints
- The system MUST function under low bandwidth conditions and intermittent connectivity.
- Critical operations MUST fail safely and MUST NOT corrupt data.

### 8. Privacy & Regulatory Compliance
- The system MUST comply with Philippine data privacy regulations.
- Personal data MUST be accessed only when necessary and MUST be protected from unauthorized access.
- The system MUST be internal-only, MUST NOT be publicly accessible, and MUST NOT be usable without authentication.

### 9. Extensibility Without Breakage
- Incentive rules MAY evolve over time.
- Recruitment statuses MAY expand.
- Historical data MUST remain valid, interpretable, and consistent across rule/status evolution.

### 10. Prohibited Practices
The following are strictly prohibited:
- Hard-coded incentive logic
- Unlogged administrative actions
- Automatic incentive awarding without validation
- Public referral sharing mechanisms
- UI patterns that obscure incentive computation logic

## Non-Functional Constraints

The following constraints apply to all features and changes:

- Safety: Critical operations MUST be transactional (or equivalent) and must fail without partial writes.
- Audit: Any change to recruitment relationships, statuses, and incentives MUST have an audit trail.
- Configurability: Incentive amounts and thresholds MUST come from centrally managed configuration.
- Internal-only: Authentication is mandatory for all system access.
- Privacy: Minimize personal data exposure and ensure role-scoped access.

## Development Expectations

- Specs, plans, and tasks MUST include an explicit "Constitution Check" section listing the applicable principles.
- Features that touch incentives or recruitment MUST include:
	- Traceability from incentive -> recruitment event(s)
	- An explanation of computation (inputs, config, outcomes)
	- Audit logging for awards, reversals, and status transitions
- Any schema or rules evolution MUST include a migration/compatibility plan to keep historical records interpretable.

## Governance

**Amendments**
- Any amendment MUST be proposed as a documented change to this file.
- Amendments MUST include the rationale, migration/rollout considerations (if applicable), and a compliance review.

**Versioning**
- The constitution uses semantic versioning: MAJOR.MINOR.PATCH.
- MAJOR: backward-incompatible governance or principle redefinition/removal.
- MINOR: new principle/section added or materially expanded guidance.
- PATCH: clarifications, wording fixes, non-semantic refinements.

**Compliance Review Expectations**
- All plans and implementations MUST be reviewed for compliance with this constitution.
- Non-compliance is allowed only with an explicit, documented exception and approval recorded in the relevant spec/plan.

**Version**: 1.0.0 | **Ratified**: TODO(RATIFICATION_DATE): original adoption date unknown | **Last Amended**: 2026-01-14
