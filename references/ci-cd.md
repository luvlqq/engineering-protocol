# CI/CD

- Follow the project's release and deployment policy.
- Use pinned, compatible tool and runtime versions.
- Verify downloaded tool integrity.
- Separate deployment credentials by access scope.
- Protect deployment variables and release references.

## Deployments

Wait for deployment health verification.

Fail the pipeline when deployment validation fails.

Require explicit approval for high-risk deployments.

## Environment Variables

Prevent deployment credentials from leaking into
build or test environments.

Use project-defined variable naming conventions.

## Runners

Manage caches and runner resources according
to the available infrastructure.

Do not remove unrelated images, caches, or volumes.

## Tests

Use isolated test environments.

Account for parallel execution, database isolation,
and asynchronous operation timeouts.

Do not sacrifice correctness for execution speed.
