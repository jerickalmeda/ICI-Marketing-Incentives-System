# /speckit.tasks — Execution Workflow

This document describes how the `/speckit.tasks` command is expected to generate
an actionable task list using `.specify/templates/tasks-template.md`.

## Inputs

- `/specs/[###-feature-name]/spec.md`
- `/specs/[###-feature-name]/plan.md`
- Optional: research.md, data-model.md, contracts/
- Constitution: `.specify/memory/constitution.md`

## Output

- `/specs/[###-feature-name]/tasks.md`

## Required Steps

1. Translate user stories into phased tasks (setup, foundational, per story, polish).
2. Include exact file paths for implementation tasks.
3. When the feature touches recruitment/status/incentives/hierarchy:
   - Add tasks for audit logging (awards, reversals, status transitions)
   - Ensure incentives are config-driven (no hard-coded values)
   - Add RBAC and hierarchy integrity safeguards
4. Include tests only if the spec explicitly requests them.
