# v0.4.27-beta.1 — installable colleague test

October 31, 2026. This prerelease replaces the previous docs-only handoff with a complete Windows testing package.

Included: setup/helper EXE, the Chrome extension, bundled Node runtime, private engine as compiled bytecode, official OpenAI tunnel runtime, per-file checksums, local diagnostic, first-run guides and third-party licenses. No developer credentials, real notes, tunnel profile, private source or internal tests are included.

The helper has no raw key input, no key decryption/storage and no automatic startup installation. It passes a user-selected env:/file: reference to the official tunnel client. Closing a running setup hides it in the tray; Stop/Exit ends this package only.

Core note/batch/accordion features remain those validated in the development build. Package diagnostics use temporary sample data. External live-account acceptance is deliberately a tester task after download, not an already-passed claim or a prerequisite for distributing this test.

[Install](INSTALL.md) · [Test checklist](TEST_CHECKLIST.md) · [Release](https://github.com/innocirclelabs-hub/ai-sticky-notes/releases/tag/v0.4.27-beta.1)
