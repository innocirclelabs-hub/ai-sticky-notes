# Data and privacy in the colleague beta

The note store runs locally and binds to loopback only. The Chrome extension is restricted to ChatGPT pages and the local note service. It stores notes/view preferences and per-conversation pairing credentials in its extension storage. The runtime stores its new note database under the current Windows user's AI-Sticky-Notes-Beta application-data directory.

When you enable and use the MCP app, relevant note/tool content travels through your authorized OpenAI tunnel into ChatGPT to fulfill your tool requests. This is **not an offline-only product**. Sharing is explicit and limited by the verified project/session checks; revoking access cannot erase content already sent in past messages.

The setup helper stores a tunnel ID and a credential reference. It never collects or reads the actual OpenAI key. The official tunnel client resolves the env:/file: reference locally. Protect that external credential file and use least privilege. This package does not include a developer account, key, tunnel profile or existing notes.

The local diagnostic uses an isolated temporary database and emits pass/fail checks without real conversation contents. Share only that sanitized diagnostic report and redacted errors when reporting a problem. Do not attach the runtime database, connection.json, a key file, private transcript or complete screenshots of other chats.

Stopping the connection preserves your notes. Uninstalling or clearing extension storage can erase browser-local data. Export or preserve data before removal. No third-party advertising, analytics or remote-update agent is added by this beta setup helper.

## Continuation records

An explicit same-project continuation stores a local handoff snapshot and the selected work-group resume metadata in the existing note database. The original conversation can read its handoff-time snapshot, not later private destination edits. Only the selected group moves; unrelated conversation rules are not automatically copied. This history is not public GitHub content or a cross-device backup.
