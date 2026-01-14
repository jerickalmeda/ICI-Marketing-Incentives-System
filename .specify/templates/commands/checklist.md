# /speckit.checklist — Execution Workflow

This document describes how the `/speckit.checklist` command is expected to
generate checklists using `.specify/templates/checklist-template.md`.

## Inputs

- User's checklist request
- Feature context (spec/plan/tasks if available)
- Constitution: `.specify/memory/constitution.md`

## Output

- A checklist markdown file scoped to the user's request

## Quality Bar

- Checklist items must be concrete, checkable, and numbered.
- When relevant, include constitution compliance checks (auditability, RBAC,
  privacy/internal-only, no hard-coded incentives).
