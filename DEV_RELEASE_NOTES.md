# v0.4.29-beta.3 — Browser pairing recovery patch

Colleague screenshots confirmed that open_postit displayed the compact host notice and the Chrome overlay existed, but the note still said AI connection pending. The complete browser pairing was not proven.

The canonical MCP UI is now launcher-v2; cached launcher-v1 and notes-v1..18 aliases remain supported. The launcher acknowledges successful browser pairing only after a no-secret Chrome extension receipt; if no acknowledgement is seen, it offers an explicitly copied, short-lived one-use code for the EXISTING floating note's manual connection field. The secret is not automatically displayed, logged or sent to ChatGPT.

The floating note remains the only full editable UI. No hosted server, new user account or credential storage is introduced. This is a recoverability fix and not proof that the exact colleague-specific message delivery failure is corrected. Confirm on their own browser.