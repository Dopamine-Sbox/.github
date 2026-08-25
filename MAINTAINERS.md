# Maintainer guide

## Triage

- Confirm the report belongs to our project before asking for more details.
- Apply `needs-repro` when the report lacks a repeatable case.
- Apply `needs-redaction` and hide/edit content if a report contains secrets or
  private information.
- Use `blocked-upstream` when the next action belongs in Facepunch/sbox-issues
  or another upstream project.

## Review

- Require evidence for compatibility, performance, security, and release claims.
- Prefer small PRs with explicit validation over broad refactors.
- Ask contributors to use permalinks and line ranges for code evidence.
- Use CODEOWNERS to route sensitive paths to the right maintainers.

## Releases

- Tag releases only after documented validation passes.
- Include commit SHA, s&box revision when relevant, operating system, runtime,
  panel type, and known limitations.
- For Discord relay announcements, highlight user-visible changes, migration
  steps, and security notes without exposing private operational details.

## Security

- Move vulnerability details out of public issues immediately.
- Rotate leaked credentials before investigating broader impact.
- Keep public advisories factual and avoid publishing exploit steps before a fix
  is available.
