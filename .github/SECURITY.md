# Security Reporting

Please **do not** disclose security vulnerabilities, private MCP endpoints, session IDs, authentication tokens, internal server architecture or reproducible exploit details in public GitHub Issues.

**Private vulnerability reporting is enabled for this repository.** Use [Report a vulnerability privately](https://github.com/innocirclelabs-hub/ai-sticky-notes/security/advisories/new), or open **Security → Advisories → Report a vulnerability**. If that private form is unavailable to your account, do not post sensitive details publicly; request a private reporting channel without describing the vulnerability.

For ordinary non-security bugs, use [SUPPORT.md](../SUPPORT.md) and the public issue templates after redacting private data.

**Scope:** The repository contains documentation and images. The v0.4.27-beta.1 Windows prerelease includes a compiled local engine, Chrome extension, setup helper and third-party runtimes for invited evaluation. The original private backend source and any user credentials, databases or private connection files are not public attachments. See [PRIVACY.md](../PRIVACY.md) and the testing permission.

The helper accepts only a credential reference; the official tunnel client resolves the tester's own credential. Never upload the referenced file, connection settings, note database or unredacted logs. Use a restricted runtime credential, never the publisher's credentials. Do not test against other users' accounts or bypass authentication controls without written authorization.
