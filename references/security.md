# Security and Secrets

- Never expose secret values in prompts, logs,
  command arguments, commits, or documentation.
- Use approved secret management mechanisms.
- Access only the minimum required secret material.
- Do not inspect sensitive files unnecessarily.
- Prefer short-lived credentials.
- Apply least privilege.
- Revoke temporary elevated access after use.

## Secret Exposure

If a secret is exposed:

1. Report the exposure without repeating its value.
2. Recommend immediate revocation or rotation.
3. Identify affected consumers.
4. Verify remediation when authorized.

## Key Recovery

Ensure approved recovery procedures exist for
irreplaceable keys before production use.

## Repository Hygiene

Scan staged changes for secrets.

Exclude sensitive temporary files, state snapshots,
and credentials from version control.

Document secret references, ownership,
expiration, and rotation procedures only.
