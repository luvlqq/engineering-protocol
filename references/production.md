# Production Operations

Production mutations require explicit authorization.
By default, the owner executes production commands.

## Preparation

For every operation, provide:

- Target environment.
- Expected impact.
- Command and expected output.
- Stop conditions.
- Recovery or rollback procedure.

## Execution Sequence

1. Establish a baseline.
2. Verify backups and recovery readiness.
3. Validate the execution plan.
4. Obtain approval.
5. Execute the change.
6. Verify system health.
7. Restore normal operations.

Do not parallelize sensitive operations.

## Infrastructure

Inspect plans for unexpected replacements,
resource creation, deletion, and drift.

Investigate drift before applying changes.
Do not hide unexplained drift.

## Rollouts

Follow project-specific topology and quorum rules.
Wait for health checks between rollout stages.

Check available capacity before increasing load.

## Recovery

Automatically roll back only safely reversible
operations with a validated recovery procedure.

Otherwise stop, preserve state, and escalate.
