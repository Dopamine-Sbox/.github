# GitHub workflow

This document defines the default GitHub workflow for Dopamine-Sbox projects and
the conventions we mirror into GameForge repositories where useful.

## Issues and discussions

- Use issues for reproducible bugs, scoped feature requests, security-safe
  compatibility reports, and release blockers.
- Use discussions for setup questions, design ideas, hardware comparisons,
  playtest impressions, and broad community support when enabled.
- Route engine bugs to Facepunch/sbox-issues unless the report is about our
  integration, scripts, game code, docs, or packaging.
- Remove tokens, private endpoints, personal data, and player identifiers from
  logs and screenshots before posting.

## Pull requests

- Keep PRs focused on one user-visible change.
- Link related issues with `Fixes #123`, `Closes owner/repo#123`, or
  `Refs owner/repo#123`.
- Include validation commands and results in the PR body.
- Use GitHub permalinks for code evidence: press `y` on a file page before
  copying links, and use line ranges such as `#L10-L25`.
- Prefer screenshots, videos, or logs for UI, editor, panel, or game behavior
  changes when they materially improve review quality.

## Labels

Recommended labels for organization repositories:

- `bug`
- `enhancement`
- `documentation`
- `security`
- `sbox-engine`
- `server-hosting`
- `pterodactyl`
- `pelican`
- `discord`
- `cloudflare`
- `gameplay`
- `needs-repro`
- `needs-redaction`
- `blocked-upstream`
- `good-first-issue`
- `help-wanted`

## Branch protection

For maintained repositories, protect the default branch with:

- pull request required before merge;
- required status checks for build/test/lint workflows;
- code-owner review required when a repository has a CODEOWNERS file;
- dismiss stale approvals when new commits are pushed;
- block force pushes and branch deletion;
- require signed or linear history only when the repo can support it without
  slowing normal contribution.

## Discord relay

GitHub-to-Discord relay output should prioritize signal:

- group noisy push events where possible;
- highlight releases, security fixes, failed checks, and breaking changes;
- include issue/PR links and compare links;
- suppress secrets and private data;
- route by organization, repository, branch, event type, and labels.
