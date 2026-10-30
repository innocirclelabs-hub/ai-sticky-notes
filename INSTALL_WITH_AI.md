# Ask Your AI Assistant to Install AI Sticky Notes

This document is for people who want to give a **GitHub repository link** to an AI assistant with **permission to work on their own computer** and have it handle the mechanical setup.

**The AI cannot invent a release asset, bypass Chrome's extension approval, or create an MCP account that you do not have.** The installation instructions are designed to be repeatable and safe.

## Copy this English prompt into your AI assistant

> Help me install AI Sticky Notes for **ChatGPT web** from this GitHub repository: https://github.com/innocirclelabs-hub/ai-sticky-notes.
>
> Use only the **verified Releases assets** from that repository. Do **not** clone, install or execute arbitrary third-party forks, copied scripts, or GitHub's auto-generated source-code ZIP. Read the repository's `INSTALL.md`, `RIGHTS_AND_SCOPE.md`, and release notes first.
>
> 1. Check my OS, installed Chrome version, and whether an official early-access ZIP release exists. If it does not exist, **stop and tell me it has not been released yet**.
> 2. Download the official ZIP and verify its SHA-256 checksum against the repository's published release digest.
> 3. Extract the ZIP to a stable directory under my user profile; verify that `manifest.json` and the expected extension files are present. Do not change unrelated extensions, browser profiles, ChatGPT projects or chats.
> 4. Open `chrome://extensions`. Explain or, **only with my explicit permission and available computer control**, perform the developer-mode and **Load unpacked** steps. Never claim Chrome silently approved or installed an extension when it did not.
> 5. Open my existing ChatGPT web conversation and help me verify that the note appears, persists on reload and stays within that conversation.
> 6. Check whether I have a **legitimate per-user MCP connection** supported by this release and ChatGPT account. If one is unavailable, clearly label the result **browser-local preview only**, not full AI integration. Do not reuse the developer's tunnel, token, local service or keys.
> 7. For supported full integration, guide me through the official ChatGPT Plugins connection and approved authentication. Do not store credentials in plaintext, logs or a GitHub Issue.
> 8. Run the short acceptance checklist: a clean new conversation, a whole work plan approved once, persistent must-follow rules, correct progress after verified work, and no accidental cross-conversation sharing.
> 9. Report exactly what passed, what failed and what needs my manual consent. Do not bypass a platform or browser security restriction to complete a blocked step.
>
> The planned distribution terms are **individual personal, noncommercial use only**; no software license is granted by this documentation. Read the actual operative terms attached to an available release. Confirm that my intended use is permitted before starting. Codex support is planned for later, **not available now**.

## For installation assistants without computer access

An AI assistant **without local file/browser controls** can explain the steps and help interpret the error messages, but cannot honestly claim to have downloaded, installed, clicked or tested the extension.

## What never to do

- Never run unreviewed `curl | sh`, `irm | iex`, a copied PowerShell one-liner from a random post, or a binary from an unverified mirror.
- Never request the repository maintainer's private MCP token, OpenAI account credentials or ChatGPT session cookie.
- Never share private screenshots, saved notes or raw error logs in public GitHub Issues.
- Never mark full AI integration PASS solely because the sticky-note UI appears.

**Current target:** ChatGPT web on desktop Chrome. **Future:** Codex integration.
