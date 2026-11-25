# Git Operations

- Commit and push only when authorized.
- Preserve unrelated user changes.
- Inspect Git status and diff before editing.
- Do not amend published commits or force-push
  without explicit authorization.
- Follow project attribution and commit conventions.

## Shared Working Trees

Stage only changes belonging to the current task.

When isolation is required, prefer Git worktrees,
explicit patch staging, or a temporary Git index.

Validate the exact version intended for commit.

Never discard unrelated changes.

## Patches

Validate patches against the intended target
working tree using git apply --check.

Report conflicts instead of silently overwriting files.
