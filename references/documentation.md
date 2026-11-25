# Documentation

## Knowledge Placement

- Architecture and behavior: project documentation.
- Significant decisions and trade-offs: ADR.
- Environment-specific facts: operations documentation.
- Reusable procedures: skills or runbooks.
- Unrelated findings: deferred work.

Keep documentation consistent with implementation.

Never document secret values.

## Runbooks

Every operational step should define:

1. Action.
2. Command.
3. Expected result.
4. Stop conditions.
5. Recovery procedure.

Update runbooks when execution reveals incorrect
assumptions or missing steps.

## Operational Scripts

Plan mode must not mutate system state.

Apply mode must follow the approved execution plan
and recovery strategy.

Return explicit success or failure status.

Never print secrets.
