# Contributing to Dopamine-Sbox projects

Thank you for helping improve our s&box community projects.

## Before opening an issue

1. Read the repository README and existing documentation.
2. Search open and closed issues for the same behavior.
3. Confirm whether the problem belongs to the community project or to s&box
   itself. Engine defects should normally be reported to
   [Facepunch/sbox-issues](https://github.com/Facepunch/sbox-issues).
4. Remove tokens, passwords, private endpoints, player identifiers, and other
   sensitive information from logs and screenshots.

## Bug reports

Include enough information for another person to reproduce the result:

- the repository revision, release, or container digest;
- the s&box or `sbox-public` revision when relevant;
- operating system, runtime, and hardware architecture;
- game package, map or scene, and launch configuration;
- exact reproduction steps, expected behavior, and actual behavior;
- relevant redacted logs.

For dedicated-server reports, also identify whether the runtime is native Linux
or Wine, whether the failure is local or panel-hosted, and whether readiness,
client join, query, graceful stop, or forced kill is affected.

## GitHub workflow

Use the shared [GitHub workflow](GITHUB_WORKFLOW.md) for issue labels,
cross-repository references, pull-request linking, review expectations, and
release evidence. When a change fixes an issue, link it with `Fixes #123` or the
full issue URL so GitHub closes it after merge.

Use permanent links when referencing code outside the current pull request, and
include enough validation detail for maintainers to repeat the check. For new
projects, start from the closest repository template listed in
[`TEMPLATE_REPOSITORIES.md`](TEMPLATE_REPOSITORIES.md) instead of copying a live
project by hand.

## Pull requests

- Keep each pull request focused on one change.
- Explain the user-visible behavior and why the change is needed.
- Add or update tests and documentation when behavior changes.
- Run the repository's documented validation commands before requesting review.
- Do not commit generated files, build output, credentials, or local environment
  files unless the repository explicitly requires them.
- Preserve compatibility claims only when they are backed by reproducible tests.
- Link related issues, previous decisions, or external upstream reports.

Maintainers may ask for a smaller change, additional evidence, or revisions
before merging. By contributing, you agree that your contribution is provided
under the license of the repository receiving it.
