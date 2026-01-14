# /speckit.spec — Execution Workflow

This document describes how the `/speckit.spec` command is expected to populate
feature specifications using `.specify/templates/spec-template.md`.

## Inputs

- User description: "$ARGUMENTS"
- Constitution: `.specify/memory/constitution.md`

## Output

- `/specs/[###-feature-name]/spec.md`

## Required Steps

1. Write prioritized, independently testable user stories.
2. Include acceptance scenarios for each story.
3. Fill **Requirements** and include **Constitution Constraints**.
4. If data is involved, define key entities at a conceptual level.
5. Provide measurable success criteria.

## Quality Bar

- All requirements MUST comply with the constitution.
- Avoid vague requirements; prefer MUST + clear conditions.
