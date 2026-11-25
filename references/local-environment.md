# Local Environment

- Inspect the operating system, shell, and runtime
  before executing environment-specific commands.
- Use shell-compatible syntax.
- Quote arguments and paths correctly.
- Avoid unnecessary global environment changes.
- Do not install dependencies globally without approval.

## Temporary Resources

Use isolated temporary directories and containers.

Clean up only resources created for the current task.

Do not delete shared or persistent volumes.

## Resource Management

Avoid unnecessary CPU, memory, and disk consumption.

Use authorized CI infrastructure for expensive
verification when appropriate.

Monitor long-running processes and report failures.

Respect tool timeouts and execution limits.
