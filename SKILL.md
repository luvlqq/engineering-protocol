---
name: engineering-protocol
description: >
  Apply a risk-based engineering workflow to software
  development, debugging, refactoring, infrastructure,
  Git operations, CI/CD, and production changes.
  Use when implementing, reviewing, validating, or
  planning technical changes.
---

# Engineering Protocol

## Core Principles

- Understand before modifying.
- Fix root causes, not symptoms.
- Prefer minimal, focused changes.
- Preserve existing architectural boundaries.
- Verify results with evidence, not assumptions.
- Never expose secrets.
- Never overwrite unrelated user changes.
- Never bypass quality gates.
- Do not commit, push, or deploy without authorization.

## Task Classification

Classify the task before execution.

### L0 — Trivial

Documentation, typos, mechanical changes.

Workflow:
Inspect → Change → Verify.

### L1 — Standard

Bug fixes, endpoints, isolated features.

Workflow:
Research → Implement → Test → Review.

### L2 — Complex

Refactoring, new modules, architectural changes,
cross-service changes.

Workflow:
Research → Plan → Review Plan → Implement →
Independent Review → Verify.

### L3 — Critical

Production operations, security-sensitive changes,
destructive or irreversible operations.

Workflow:
Research → Risk Assessment → Human Approval →
Backup → Plan → Execute → Verify → Recovery.

Increase the risk level whenever uncertainty,
blast radius, or irreversibility increases.

## Context Routing

Read only the references relevant to the task.

| Operation | Reference |
|---|---|
| Implementation or refactoring | [references/development.md](references/development.md) |
| Testing and validation | [references/verification.md](references/verification.md) |
| Production operations | [references/production.md](references/production.md) |
| Secrets and security | [references/security.md](references/security.md) |
| Git operations | [references/git.md](references/git.md) |
| CI/CD changes | [references/ci-cd.md](references/ci-cd.md) |
| Local environment | [references/local-environment.md](references/local-environment.md) |
| Documentation | [references/documentation.md](references/documentation.md) |

Do not load all references by default.

Read applicable project-specific documentation.
Do not invent missing project conventions.

## Execution Rules

Use subagents when independent research,
context isolation, parallel execution, or
independent review provides a meaningful benefit.

Keep assignments narrow and explicit.

Do not parallelize conflicting changes.

Prefer deterministic tools for deterministic tasks.

## Verification

Every completion claim requires evidence.

Validate review findings before applying fixes.

Never weaken tests, linters, architecture rules,
security policies, or quality gates to pass checks.

After three unsuccessful repair attempts,
report the blocker instead of continuing indefinitely.

## Definition of Done

A task is complete when:

- Requirements are satisfied.
- Changes remain within scope.
- Relevant checks have passed.
- Review findings have been addressed.
- No unauthorized side effects occurred.
- Documentation is updated when necessary.

Report skipped checks, unresolved risks,
and remaining limitations explicitly.

## Continuous Improvement

When a recurring mistake is identified:

1. Identify the root cause.
2. Inspect existing instructions.
3. Propose a minimal improvement.
4. Prefer automated enforcement where possible.
5. Obtain approval before changing shared rules.
