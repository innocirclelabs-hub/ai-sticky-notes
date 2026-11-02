# v0.4.29-beta.2 — Safe connection diagnostics

This invited Windows beta is a diagnostics-focused patch, not a production service or root-cause fix for the colleague's unobserved PC.

- Report actual loopback 8791 occupancy and expected-product health separately from the isolated 11-check local diagnostic.
- Observe child process output in memory only; export fixed error codes and counts, not source lines or credentials.
- Save safe local diagnostics after startup failure, unexpected process exit or tunnel readiness change.
- Add Copy safe connection report in Setup and optional read-only CLI.
- Do not expose raw key, tunnel ID, credential-file path, note content, host session, or arbitrary process text.
- Keep earlier local MCP, Chrome extension and same-project continuation. Does not create a publisher server.
- A tunnel OAuth discovery warning alone is not proof of an unusable tunnel.
- External colleague's own account and time-to-first-use acceptance remain unverified.

Read CONNECTION_DIAGNOSTICS.md and TEST_CHECKLIST.md.