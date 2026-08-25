---
name: hermes-skill-requesting-code-review
description: Run a pre-commit quality and security pass and prepare a focused review request. Use when a user asks for this workflow or a closely related task.
---

# Requesting Code Review

Prepare changes for review using a repeatable pre-commit quality gate.

## Workflow

1. Inspect the diff and identify behavior changes, touched interfaces, and risk areas.
2. Run focused tests first, then lint, formatting, type checks, and security scans available in the repository.
3. Look for secrets, unsafe input handling, missing authorization, race conditions, error swallowing, and untested edge cases.
4. Fix only issues in scope and preserve unrelated user work.
5. Prepare a review request with summary, test commands/results, risks, and follow-ups.
6. Leave unresolved uncertainty visible.

Never claim a check passed if it was not run or if its output was incomplete.
