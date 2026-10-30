# AI Sticky Notes

<img src="assets/ai-sticky-notes-icon.png" width="112" alt="AI Sticky Notes: a smiling yellow sticky note">

**Keep the plan visible. Keep the rules in view.**

A movable sticky note for your existing ChatGPT conversations: tasks, verified progress, and persistent must-follow rules—without losing them in a long conversation.

**Development build: `0.4.26-dev` · ChatGPT Web / desktop Chrome · Proprietary**

> **Availability — October 31, 2026:** This public repository contains documentation, product screenshots, and feedback templates. **No public installer ZIP or self-service MCP connection is available yet.** The planned GitHub Early Access release is intended to let people actually try the product before a Chrome Web Store release. Software distribution will follow only after the license, external-user onboarding, and clean-environment checks are complete. GitHub's automatically generated “Source code” archive contains these public materials, not the application.

[Installation guide](INSTALL.md) · [Install with an AI assistant](INSTALL_WITH_AI.md) · [Version and support](VERSION.md) · [Release readiness](RELEASE_READINESS.md) · [Feedback](SUPPORT.md) · [Rights and scope](RIGHTS_AND_SCOPE.md)

## A plan you can keep track of

**Tasks and rules stay separate.** Completed tasks keep their red strikethroughs and recorded completion evidence. Must-follow rules are not completed or silently removed when a job finishes.

**Approve the whole plan once.** Review a proposed task plan and its constraints together. Evidence-backed completion requires a connected, authorized AI/MCP workflow; the extension alone does not give an AI model access to your notes.

**One conversation, distinct jobs.** Every approved plan has its own task group. A completed **7/7 · 100%** job can stay folded while a new **0/3 · 0%** job is open. Each group has a large completion mark, a title, and independent expand/collapse controls. Finishing an old job does not inflate the next job's progress.

**Keep the history, clear the workspace.** Archive completed groups, export their task history and evidence to Markdown, or move a completed group to recoverable Trash with one confirmation. Guardrails remain active. Completion never automatically deletes a group.

**A small, flexible interface.** Drag and resize the note, fold the entire panel or individual rule cards, switch English/Korean without translating note text, and request native Picture-in-Picture pinning where the browser supports it.

**Your conversation is the boundary.** Notes are private to their source conversation by default. Sharing is explicit, limited to a verified project, and revocable. Revocation stops later access; it cannot erase text that was already sent in an earlier conversation message.

**No forced composer attachments.** Current AI note access uses explicit MCP tool reads rather than repeatedly attaching note summaries to the ChatGPT message composer. AI compliance is not guaranteed merely because a note is visible.

## Product examples

| University assignment | Small responsive website |
|---|---|
| ![Completed assignment plan in an isolated product UI demonstration](screenshots/student-04-complete.png) | ![Completed website plan in an isolated product UI demonstration](screenshots/web-04-complete.png) |
| [Assignment walkthrough](USE_CASE_01_STUDENT_ASSIGNMENT.md) | [Website walkthrough](USE_CASE_02_SIMPLE_WEB_PAGE.md) |

The eleven screenshots are real browser captures from **scripted, isolated demonstrations with sample data**, not recordings of autonomous AI in a logged-in ChatGPT conversation. They illustrate the core workflow and may not show every control added in the latest build. [Screenshot provenance](SCREENSHOTS.md).

## Installation and release status

The planned download will be a separately attached extension ZIP in this repository's [Releases](https://github.com/innocirclelabs-hub/ai-sticky-notes/releases), with a checksum and the approved distribution terms. Until that asset exists, this repository is **not an installable release**.

Browser-local mode and full AI-linked mode are different. Full AI read-back, evidence-based updates, and synchronized sharing require a separately authorized per-user MCP connection and host support. Never reuse the maintainer's private tunnel, database, keys, or session credentials.

**Current development scope:** ChatGPT Web on desktop Chrome, Windows-first. **Codex, mobile, and other browsers are not advertised as available.**

## Feedback and rights

Use [Issues](https://github.com/innocirclelabs-hub/ai-sticky-notes/issues/new/choose) for non-sensitive bug reports, installation questions, or feature requests. Please redact private conversation text and credentials. Security reports follow the [security policy](.github/SECURITY.md).

AI Sticky Notes is proprietary, **not an open-source release**. The intended software-use policy is free personal, unpaid, noncommercial use by individuals; business, institutional, professional, resale, and OEM use require a separate written commercial license. Those are planned distribution terms, **not a software license granted by this documentation**. See [Rights and scope](RIGHTS_AND_SCOPE.md).

The private product source, backend, authentication system, user data, and development history are not part of this repository.
