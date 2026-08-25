# Template repository plan

Use these as repository templates rather than one-off copied repos. Each
template should include README structure, issue and PR guidance, validation
commands, a release checklist, baseline workflows, and security-safe examples.

## Dopamine-Sbox templates

| Template | Purpose |
| --- | --- |
| `sbox-game-template` | Base for s&box games with scenes, code layout, validation commands, playtest notes, screenshot guidance, package/release checklist, and privacy-safe bug reports. |
| `sbox-addon-template` | Base for s&box addons that extend editor/game behavior, including package metadata, smoke checks, example scene, and compatibility notes. |
| `sbox-library-template` | Base for reusable s&box libraries, shared components, helper APIs, examples, semantic versioning notes, and downstream integration tests. |
| `sbox-map-template` | Base for s&box map packages with scene/map metadata, navmesh validation, lighting/build notes, screenshots, playtest checklist, and map-specific stats/achievements notes. |
| `sbox-tooling-template` | Base for editor tools, MCP helpers, asset utilities, CLI scripts, and diagnostics for s&box projects. |
| `pterodactyl-pelican-egg-template` | Base for dedicated-server eggs: local native/Wine smoke test, egg generation, panel test, stop/restart validation, artifacts, and publishing docs. |
| `cloudflare-discord-bot-template` | Base for Cloudflare Workers, Hono apps, Discord webhooks/bots, signature validation, routing config, legal pages, and deployment docs. |
| `docs-guide-template` | Base for community guides, compatibility docs, benchmark reports, troubleshooting guides, and release-noted documentation. |

## GameForge templates

| Template | Purpose |
| --- | --- |
| `pterodactyl-pelican-egg-template` | Shared GameForge-facing egg pipeline for game dedicated servers and panel validation. |
| `cloudflare-discord-bot-template` | Shared bot/webhook/worker template for GameForge automation and community integrations. |
| `docs-guide-template` | Shared documentation template for hosting guides, compatibility matrices, and support runbooks. |

## Pterodactyl/Pelican egg pipeline

The egg template should encode this flow:

1. Build or fetch the dedicated server artifact.
2. Run local native Linux smoke tests.
3. Run local Wine/Windows smoke tests when relevant.
4. Validate graceful stop, forced stop fallback, query visibility, console
   interactivity, map/game rotation, and client join behavior where available.
5. Generate Pterodactyl and Pelican egg JSON from versioned source data.
6. Upload to a test panel using secrets from the configured CI environment.
7. Boot the panel server, validate install/start/stop/logs/artifacts, then
   destroy the test server.
8. Publish the egg, validation evidence, changelog, and compatibility notes.

Never print panel keys, Steam keys, Discord tokens, private panel URLs, private
IP addresses, or full user identifiers in workflow logs.

## Template creation checklist

- Mark the GitHub repository as a template after the initial files land.
- Add `CODEOWNERS` and default branch protection/ruleset recommendations.
- Add `SECURITY.md`, `SUPPORT.md`, `CONTRIBUTING.md`, issue forms, and PR
  template unless inherited from the org `.github` repository.
- Add a `VALIDATION.md` file with commands that a contributor can run locally.
- Add a `RELEASE.md` file with tag, changelog, artifact, and Discord relay
  expectations.
- Add a placeholder GitHub Actions workflow only when it can run without
  credentials.
