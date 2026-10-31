# Install the colleague-test package — v0.4.28-beta.1

**Windows 10/11 x64, desktop Chrome. This is an installable testing prerelease, not a production release.**

[Download the complete Windows ZIP](https://github.com/innocirclelabs-hub/ai-sticky-notes/releases/download/v0.4.28-beta.1/AI-Sticky-Notes-Windows-v0.4.28-beta.1.zip) · [Release and SHA-256 checksum](https://github.com/innocirclelabs-hub/ai-sticky-notes/releases/tag/v0.4.28-beta.1)

## 1. Extract and run

Download **AI-Sticky-Notes-Windows-v0.4.28-beta.1.zip**, not GitHub's automatic Source code ZIP. Verify the SHA-256 against `SHA256SUMS.txt` on the same release. Extract the complete folder to a permanent directory under your own user profile. Keep all subfolders together.

Open **AI-Sticky-Notes-Setup.exe**. Node.js, the private compiled engine and the official tunnel runtime are included. No Python, npm, Git, administrator install, firewall opening or developer database is required. This prerelease helper is not code-signed; inspect the official source of the download and checksum before choosing whether to run it. Do not disable antivirus or organizational security policy.

Click **Local diagnostic**. It creates a temporary empty database on an unused loopback port and checks the actual bundled runtime. It does not use your account key, inspect existing notes, or certify your ChatGPT account. A successful result has eleven PASS checks.

## 2. Load the extension

Use **Copy extension path** and **Chrome extensions** in Setup. In `chrome://extensions`, enable Developer mode, choose **Load unpacked**, and select the package's **extension** folder containing `manifest.json`. Confirm AI Sticky Notes **0.4.28-beta.1**. This browser approval is deliberately not bypassed.

The extension can display local notes before AI connection, but that is not the completed test. Continue below.

## 3. Authorize your own OpenAI tunnel

Full AI integration uses your own supported ChatGPT/OpenAI account. The package neither includes the publisher's connection nor creates an account for you.

Use OpenAI's secure API-key setup flow in your own account, following the [official tunnel permissions guide](https://github.com/openai/tunnel-client/blob/v0.0.18/docs/permissions.md) for a **runtime** credential with **Tunnels Read + Use**. Do not use an admin key for the running connection. Your account or workspace must permit creating/selecting a Secure MCP Tunnel and adding a custom MCP server.

The Setup **Tunnel settings** button opens the official Platform page. Create a tunnel for your own relevant ChatGPT workspace and copy its complete tunnel ID into Setup. Account/workspace permissions and any provider terms or charges are controlled by OpenAI; this package does not purchase credits or enable billing.

The second field takes a **credential reference, not the key itself**:

- Use **Choose my key file** to select the dedicated key file obtained through the secure official setup/download flow. The helper stores only its path; the official OpenAI tunnel client reads the key. Keep that dedicated file private and outside the downloaded product folder, Git repositories and shared/cloud-synced directories.
- An already provisioned environment-variable reference such as `env:CONTROL_PLANE_API_KEY` is also supported by the official client. The value must already be available to the launched process.

Never paste a key into a ChatGPT message, issue, screenshot, the Tunnel ID field or the reference field. The helper does not read, decrypt, copy or upload the key file itself. This prerelease does not claim to provide an encrypted credential vault.

Review the [invited testing permission](EVALUATION_PERMISSION.md), check the evaluation box and click **Save & start**. Wait for **Local MCP: READY** and **OpenAI tunnel: READY**. The engine binds only to `127.0.0.1:8791`; the tunnel is outbound. If the port is occupied, the helper refuses to replace the existing service.

## 4. Add it in your own ChatGPT

Click **ChatGPT connection**. Use the account's **Add custom MCP server** entry, select **Tunnel**, choose or enter your own tunnel ID, and name it **AI Sticky Notes**. Complete the host's explicit permissions. See [OpenAI's connection guide](https://developers.openai.com/plugins/deploy/connect-chatgpt).

Keep Setup running. Closing its window hides an active connection in the Windows tray; **Stop connection** or **Exit** ends only this package's processes. There is no automatic Windows-startup installation.

In an existing test conversation, enable the resulting app and ask:

> Open AI Sticky Notes in this conversation. Read `list_notes` and `get_working_context`. Then propose a two-step sample task with one must-follow rule. Do not use another conversation's notes.

The user-requested open issues a short-lived pairing proof for that actual conversation. The floating note should report **AI connected**. Approve the plan once, ask the AI to perform the sample task, and check its real tool reads and evidence-based completion. **A visible note or tunnel READY alone is not proof of AI integration.**

## 5. Test and report

Follow [TEST_CHECKLIST.md](TEST_CHECKLIST.md). Record actual pass/fail results from your own account. Test on non-sensitive sample notes first. The purpose of this prerelease is to collect that external-user result; it is not a prerequisite that must already be passed before downloading.

## Data, updating and removal

Notes are created on your PC under `%APPDATA%\AI-Sticky-Notes-Beta\notes.sqlite`; no publisher notes are included. `connection.json` stores your tunnel ID and credential **reference**, not its contents. The Chrome extension keeps its own per-conversation view/local-note state. [Privacy details](PRIVACY.md).

Stop the helper before replacing package files. Preserve the extension directory identity and data; do not uninstall/clear extension storage simply to update. Replacing files and reloading the existing extension is different from deleting notes. To remove the beta, stop/exit, remove the Chrome extension through Chrome, and remove the extracted folder. Keep your notes/data until you have exported anything needed. Revoke your own tunnel credential separately through OpenAI when no longer needed.

Codex, macOS/Linux, mobile and Chrome Web Store distribution are outside this testing package.

## Continue after a conversation limit

See [CONTINUATION.md](CONTINUATION.md) for the compact, one-confirmation same-project handoff. Keep both old and new work groups distinct. Update both the runtime package and the included extension to this version; do not clear your note database or Chrome storage.
