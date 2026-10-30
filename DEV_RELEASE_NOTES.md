# Development Notes — v0.4.26-dev

**October 31, 2026 · Implemented development build, not a public software release**

## Task groups stay distinct

- Display multiple approved jobs in the same conversation as separate groups.
- Show a large completion check, task-group title, and independent completion ratio.
- Expand or collapse the whole list of tasks within each group, independently.
- Keep red strikethroughs and completion evidence when a completed group is unfolded.
- Open new unfinished work separately from older completed work. Respect explicit fold preferences.
- Preserve group-fold preferences on reload: conversation-scoped Chrome storage for the extension; session-scoped view storage for the official app widget.

## Retained from v0.4.25

- Archive a completed task group, save it as Markdown, or move it to recoverable Trash after one confirmation.
- Restore saved groups without silently regranting their previous task-sharing permissions.
- Keep must-follow rules active and separate from task cleanup.
- Keep manually added/shared tasks separate from an approved plan's progress.

## Existing workflow

A movable and resizable note, one review action for an entire plan, evidence-backed completion through authorized tools, persistent rules, English/Korean interface, and explicit project-scoped sharing. Optional native Picture-in-Picture depends on browser support and user action.

The unwanted automatic note-summary attachment behavior was corrected; routine status checks use tools rather than opening more app cards. No universal guarantee of AI compliance or automatic continuation on every host is made.

## Verification scope

The maintainer's private regression run for this build passed 57/57 tests. Independent task-group folding and reload restoration were exercised on both product UI surfaces with temporary test data. The installed development extension was updated and inspected in an existing ChatGPT conversation. Earlier live tests verified core Chrome controls and selected sharing/revocation across two actual conversations.

These are development results, not a claim that a clean external user's full installation is ready. Public download terms, per-user connectivity, and clean-environment onboarding remain release gates. Internal test runners, private session data, and service credentials are not published here.
