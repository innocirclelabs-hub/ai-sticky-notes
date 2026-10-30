# Install AI Sticky Notes — GitHub Early Access

**Platform:** ChatGPT **web**, Google Chrome desktop (Windows-first early access).  
**Codex:** Planned for a future release, **not** currently supported.  
**Distribution:** GitHub Release before any official Chrome Web Store publication.

> **Release status (October 31, 2026):** This documentation is public, but the extension ZIP and self-service MCP onboarding are **not yet released**. These steps apply only once an approved download appears. Please do not attempt to use someone else's private MCP tunnel or credentials. Once a release appears, follow the steps below.

## Before you start

You need:
- A desktop Google Chrome browser and access to an existing ChatGPT conversation.
- Permission to install an unpacked Chrome extension on your computer.
- A release ZIP obtained directly from this repository's **Releases** tab (not from a third-party website).
- For AI-linked sync and automatic model-side updates, an authorized MCP connection to the official service or an expressly supported per-user instance. **Browser-local mode does not provide full AI integration.**

## Step 1 — Download an official beta release

1. Open the **Releases** tab of this GitHub repository.
2. Download the latest `AI-Sticky-Notes-ChatGPT-Web-vX.Y.Z.zip` release asset (the first candidate is named `AI-Sticky-Notes-ChatGPT-Web-v0.4.26-dev.zip`), **not** GitHub's automatically generated “Source code (zip)” archive. If there is no uploaded release, the beta is not yet available.
3. Verify the SHA-256 digest printed in the release notes against the downloaded ZIP.
4. Unzip to a directory you can keep, for example `Documents\AI-Sticky-Notes-Beta`.

The selected directory must directly contain `manifest.json`, `overlay.js`, `overlay.css`, `background.js` and `bridge-client.js`. Do not delete or move this folder after installation without updating Chrome.

**Never copy a maintainer's local SQLite database, API key, tunnel profile, service credential or session token.** Those are not installation requirements and must not ship in the release.

## Step 2 — Install the extension without the Chrome Web Store

1. Open **`chrome://extensions`** in Chrome.
2. Turn **Developer mode** ON.
3. Choose **Load unpacked**.
4. Select the **unzipped directory containing `manifest.json`**, not the ZIP file.
5. Confirm that Chrome shows **AI Sticky Notes** with the same blue/yellow icon and version `0.4.26-dev` (development preview). The numeric manifest version is `0.4.26`.
6. Open an existing conversation at `https://chatgpt.com/`. Click the Chrome extension icon (you may pin it to the toolbar) to show the note.

Chrome may display developer-mode warnings because the package was installed outside the Chrome Web Store. Only install a release from a source you trust.

## Step 3 — Choose your connection mode

### A. Browser-local preview

The unpacked extension can keep browser-local task and rule notes in the currently open ChatGPT conversation and can suggest candidates from newly added user instructions.

**Limitations:** `MCP not connected` means the language model does not automatically read these notes or mark finished tasks from trusted tool evidence. This is a limited preview, **not the complete AI-assisted product**.

### B. Full AI-assisted MCP mode

**Available only after a supported per-user MCP service is released or explicitly provided to the tester.**

1. Follow the release's **per-user** MCP connection instructions, which must include a trusted HTTPS MCP endpoint or authorized Secure MCP Tunnel route.
2. In ChatGPT's Plugins area, choose **Add custom MCP server** (when available to your account/workspace), then set up the provided server, authentication, and permissions.
3. Install/enable the resulting AI Sticky Notes plugin for an **existing ChatGPT web conversation**.
4. Use `Open AI Sticky Notes` in the connected plugin so the app can issue a **short-lived pairing proof** for that real conversation.
5. Confirm that the floating Chrome note says **AI connected** before expecting explicit AI tool read-back or evidence-based completion. A visible note is not proof that the model has read it.

Do not expose your MCP access token in a GitHub Issue, shared screenshot, ChatGPT prompt or terminal history. This release must not ask users to enter the maintainer's API keys.

**Important compatibility warning:** Not every ChatGPT account/workspace permits custom MCP connections or write-enabled tools. If the option is absent or a tool is blocked, record that as **not supported on this account** rather than inventing a workaround.

## Step 4 — Quick acceptance check

- In a clean **newly chosen** conversation, open the sticky note. It must have **no inherited notes** from another conversation.
- Ask ChatGPT to plan a short task with one must-follow condition. If an MCP-backed AI tool is available, it should propose a **single review plan** with tasks and constraints.
- Click **Approve entire plan & start** just **once**. No separate approvals per item.
- Verify that actual completed tasks retain red strikethroughs and that progress updates only after a confirmed result.
- Fold/unfold one constraint card without changing another. Reopen the tab and confirm notes persist.
- Check that your notes never appear in a different conversation unless you explicitly choose to share them.

In browser-local preview, the AI read-back and automatic completion steps must be labeled **not available**, not passed.

## Updates and uninstall

For **unpacked GitHub releases**, Chrome does **not** install new versions automatically:

- Download and validate the newer release ZIP.
- Back up any browser-local notes using a supported export/import flow **if available**. **Do not remove the previous extension or delete Chrome storage until you know your data can be recovered.**
- Replace the files at the current installed extension directory only after preserving data, then click its **Reload** icon in `chrome://extensions`.
- Refresh existing ChatGPT tabs that still carry invalidated old content scripts.
- Verify extension version, note visibility and absence of newly generated Chrome extension errors.

**Uninstalling or clearing extension data may remove browser-local notes.** Review data/export support before proceeding.

## Get help

Use GitHub [Issues](SUPPORT.md) for non-sensitive bug reports, installation questions and feature requests. Never post private conversations, keys or session IDs.

For AI-assisted installation, see [INSTALL_WITH_AI.md](INSTALL_WITH_AI.md).  
For proposed personal-use restrictions, see [Rights and scope](RIGHTS_AND_SCOPE.md).
