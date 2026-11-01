# v0.4.29-beta.1 — One floating sticky note + first-use guidance

This invited test update addresses teammate feedback that tunnel/API setup took about an hour and starting from the plugin was confusing. It does not add or require a publisher-hosted server. A local MCP engine and the tester's own approved OpenAI tunnel are still necessary.

- The official plugin open tool serves a minimal pairing/help launcher. Full task cards remain in the draggable Chrome overlay only. Existing cached resource aliases serve the same minimal launcher when refetched.
- An explicit plugin-open one-use proof also unhides the floating note; first-time users see a dismissible, per-conversation next-action hint inside that overlay.
- The Windows Setup displays a clear next step, includes Open ChatGPT + copy first request, and distinguishes local READY, tunnel READY and actual ChatGPT pairing. It never auto-sends a message or reads/stores a raw OpenAI key.
- Installation docs, first-use test checklist and troubleshooting now match the interface.

Acceptance must separately verify first-user time and success on the colleague's own account; this package's isolated tests are not a claim that the hour-long tunnel authorization itself has been removed. ChatGPT may still render a tiny, host-owned launcher notice; the plugin cannot force the host card container to disappear. Requires Chrome extension for free movement.

Original backend source, keys, owner data, credentials, tunnel profiles and private repo are not published. No Codex/mobile/non-Windows support claim.
