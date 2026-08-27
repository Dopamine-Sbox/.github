# Security Policy & Secret Management

The **Dopamine-Sbox** organization enforces strict security standards to protect game source code, player authentication services, dedicated servers, and developer credentials.

---

## 🛡️ Comprehensive Security Documentation

For exhaustive guides on secret management, pre-commit scanners, session token safety, and emergency git scrubbing, consult our central knowledge base:

- 📖 [**Special-Documentation / Security & Credentials Hub**](https://github.com/Dopamine-Sbox/Special-Documentation/tree/main/security-and-credentials)
- 🔐 [**Commit & PR Security (Signing & Pre-commit Scanners)**](https://github.com/Dopamine-Sbox/Special-Documentation/blob/main/security-and-credentials/commit-and-pr-security.md)
- 🔑 [**Credentials & Secrets Management (`.env` & Vaults)**](https://github.com/Dopamine-Sbox/Special-Documentation/blob/main/security-and-credentials/credentials-and-secrets-management.md)
- 🍪 [**Sessions, Cookies & Logins Protection**](https://github.com/Dopamine-Sbox/Special-Documentation/blob/main/security-and-credentials/sessions-cookies-and-logins.md)
- 🛡️ [**Universal `.gitignore` Template**](https://github.com/Dopamine-Sbox/Special-Documentation/blob/main/security-and-credentials/universal-gitignore-rules.md)
- 🚨 [**Incident Response & Secret Revocation Runbook**](https://github.com/Dopamine-Sbox/Special-Documentation/blob/main/security-and-credentials/incident-response-and-revocation.md)

---

## 📋 Supported Versions

Security fixes are actively applied to the latest version on the default branch (`main`) across all repositories and published releases.

---

## 🚨 Reporting a Vulnerability

**Please do not disclose a vulnerability, credential, private endpoint, token, or exploit in a public issue, pull request, discussion, log, or screenshot.**

1. Navigate to the affected repository's **Security** tab and click **Report a vulnerability** to open a private advisory.
2. Include:
   - Affected repository and commit SHA;
   - Security impact and affected systems;
   - Minimal reproduction steps or proof-of-concept;
   - Whether the issue is actively being exploited.
3. If private reporting is unavailable, open a minimal issue requesting private contact with maintainers without including vulnerability details.

---

## 🔑 Leaked Credentials & Immediate Remediation

If a third-party secret (Steam Web API Key, Discord Bot Token, Cloudflare Token, RCON Password, Browser Cookie) is accidentally committed:
1. **Revoke and rotate the credential immediately** at the issuing service provider.
2. Follow our [Incident Response Runbook](https://github.com/Dopamine-Sbox/Special-Documentation/blob/main/security-and-credentials/incident-response-and-revocation.md) to purge the git history via `git-filter-repo`.
