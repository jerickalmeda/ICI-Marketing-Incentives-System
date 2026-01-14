# /speckit.constitution — Execution Workflow

This document describes how the `/speckit.constitution` command is expected to
maintain `.specify/memory/constitution.md`.

## Required Behavior

- Fill any placeholders in the constitution template.
- Keep the document declarative and testable (MUST/SHOULD language).
- Maintain semantic versioning and update dates in ISO format (YYYY-MM-DD).
- Prepend a Sync Impact Report describing the changes and impacted templates.
- Propagate required updates to `.specify/templates/*` and command docs.
