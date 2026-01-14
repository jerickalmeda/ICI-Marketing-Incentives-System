# /speckit.plan — Execution Workflow

This document describes how the `/speckit.plan` command is expected to populate
an implementation plan using `.specify/templates/plan-template.md`.

## Inputs

- `/specs/[###-feature-name]/spec.md`
- Existing repo structure and conventions
- Constitution: `.specify/memory/constitution.md`

## Output

- `/specs/[###-feature-name]/plan.md`

## Required Steps

1. Summarize the feature requirements and intended approach.
2. Populate **Technical Context** with concrete stack details (or mark NEEDS CLARIFICATION).
3. Fill **Constitution Check** gates based on `.specify/memory/constitution.md`.
4. Propose a concrete **Project Structure** for the feature.
5. Record any justified complexity violations (only when necessary).

## Quality Bar

- Must be implementable without guessing.
- Must not violate the constitution (auditability, RBAC, no hard-coded incentives, internal-only, etc.).
