# Evidence-Based Verification

Never claim verification without evidence.

## Validation Methods

Select applicable checks:

- Unit, integration, and end-to-end tests.
- Static and dependency analysis.
- Configuration rendering and parsing.
- Infrastructure validate and plan.
- Patch applicability checks.
- Build and runtime verification.

## Review Findings

Confirm findings using reproduction, failing tests,
static analysis, or code inspection.

Do not implement speculative fixes.

## Environment

Reproduce relevant CI conditions:

- Environment variables.
- Dependency versions.
- Workspace configuration.
- Runtime and platform differences.

Use compatible, pinned tool versions.

## Results

Report:

- Commands executed.
- Passed and failed checks.
- Skipped checks and reasons.
- Remaining risks.

Never weaken verification to obtain a passing result.
