# v0.4.28-beta.1 — Continue one work group in a new conversation

This invited testing prerelease adds explicit same-account, same-verified-project work continuation. The old dialogue need not remain writable. Original task IDs, approval, evidence and progress are retained; only the selected group changes its editing conversation. Source history is read-only. Duplicate, competing and stale handoffs are rejected without cloning the work. New scoped resume data keeps separate jobs' rules from being merged.

The normal note layout stays unchanged. The entry is a small link in an empty task list or an item in the existing settings/more menu. Review one compact card and confirm once. Nothing is automatically attached to the composer.

The private source regression suite passed 65/65 in a sequential run. New store tests cover progress/evidence, project separation, stale/duplicate fencing, drafts/archive rules and disk reopen. These code tests are distinct from real ChatGPT account checks. Consult the release verification section for actual maintainer-side observations, and run TEST_CHECKLIST.md in your own account.

The portable package retains the original setup method, bundled runtimes, per-user data directory, credential-reference-only behavior and existing evaluation terms. Private source, developer keys, tunnel profiles and databases are not distributed. Windows/ChatGPT Web test scope only.

The final continuation UI test also exercises the official widget and floating Chrome overlay with one explicit handoff, retained fold state, and zero composer messages. A preview response is no longer allowed to replace the destination conversation snapshot. The packaged compiled engine independently passed nine continuation checks. Maintainer-side actual conversations demonstrated 5/7 transfer, a sixth evidence-backed completion, and refresh restoration; this is distinct from a new external tester account.
