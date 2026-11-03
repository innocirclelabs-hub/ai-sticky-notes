# Installing AI Sticky Notes with an assistant — Windows prerelease v0.4.30-beta.1

Use this public download: https://github.com/innocirclelabs-hub/ai-sticky-notes/releases/download/v0.4.30-beta.1/AI-Sticky-Notes-Installer.exe

An assistant with authorized desktop access may download the exact EXE, verify the SHA256SUMS.txt checksum, run the installer under the current ordinary Windows user, and inspect the setup steps. **Do not request administrator privileges or replace unrelated processes.** Existing beta users must select the old installation folder to preserve their Chrome extension path, then reload that extension.

After that, the user must personally approve **Load unpacked** in Chrome, set up/authorize their own Secure MCP Tunnel credential and enable the custom MCP in ChatGPT. No assistant or installer may bypass those account approval prompts or collect raw credential contents in a message. Existing tunnel ID and credential reference are reused from the user's AppData where available.

The user verifies the yellow floating note says **AI 연결됨** and ChatGPT actually calls list_notes/get_working_context. Otherwise collect only reviewed safe diagnostics. See EASY_INSTALL.md and PAIRING_RECOVERY.md.

This prerelease does not deliver a general-purpose zero-click ChatGPT connection. It includes no seller-paid AI API or operated backend.
