# Colleague acceptance checklist

Use your own Windows PC, Chrome and supported ChatGPT account. This checklist is intentionally to be performed **after downloading the test release**.

| Test | Record actual result |
|---|---|
| Complete ZIP checksum and local diagnostic | PASS / FAIL + error |
| Load included extension; version 0.4.29-beta.1 | PASS / FAIL |
| Own tunnel and credential reference; local + tunnel READY | PASS / FAIL / account permission unavailable |
| Own ChatGPT custom MCP connected; real list_notes and get_working_context | PASS / FAIL |
| One review approval for a sample two-step plan | PASS / FAIL |
| Actual work completed; evidence stored and red strikethrough, correct percent | PASS / FAIL |
| Persistent rule referenced by real AI tool read | PASS / FAIL |
| Reload: same notes and folded state restored | PASS / FAIL |
| Old completed group and new pending group independently fold | PASS / FAIL |
| Archive/export/trash/restore operate only on selected sample task group | PASS / FAIL |
| Two actual test chats private by default | PASS / FAIL |
| One explicit same-project test note shared read-only then revoked | PASS / FAIL |
| No unsolicited Context attachment | PASS / FAIL |
| Close/reopen helper, stop/start, and no other services changed | PASS / FAIL |

Do not mark an AI-connected test passed merely because local diagnostics or a screenshot passed. Do not publish note contents, session identifiers, tokens or private URLs with the results. Use the repository issue forms for redacted results; use private vulnerability reporting for security concerns.

## New conversation continuation

- Start a non-sensitive seven-task sample in A and verify five actual completions.
- Pair B in the same verified project. Candidate discovery must not occur before you choose Continue previous work.
- Select the intended group and confirm once. Check 5/7, unchanged item IDs, five evidence records and only relevant rules.
- Ask B AI to read real working context and complete one actually verified remaining step: 6/7.
- Refresh B: state and chosen fold restore. A retains read-only handoff history and rejects its old update.
- Check another job and another project remain unchanged. Unknown or different project is refused.
- Repeat an already-accepted request: no duplicate group. Test stale preview conflict using sample data.
- Confirm no automatic Context attachment appears.

Do not report skipped account/UI checks as PASS.

## First-use / onboarding evaluation (v0.4.29 beta)

- [ ] Record elapsed time separately for download/extraction, Chrome extension, personal OpenAI tunnel/credential, ChatGPT custom MCP approval and first confirmed AI tool read.
- [ ] Starting from plugin command Open AI Sticky Notes: only a SMALL pairing notice should appear, no duplicate full editable note card. Actual floating note must open and show AI connected.
- [ ] From an empty Chrome task view: without onboarding knowledge, the in-note first-use hint shows one next action. Dismissing it persists for the same conversation. The extension icon can restore a hidden note.
- [ ] Setup local READY vs tunnel READY vs current conversation AI connected are not conflated.
- [ ] Setup's Open ChatGPT + copy first request copies the phrase but never sends it; user chooses the real chat and sends.
- [ ] On missing extension, missing tunnel permission or denied custom-MCP approval, display the limiting step; do not claim setup is complete.
- [ ] After connection, ask for an actual sample task, approve plan once, verify read tool call and evidence-marked completion, then refresh and confirm state.
- [ ] Confirm no auto @Context attachment, no automatic account credential upload and no new server account.
- [ ] Compare manual plugin entry and extension-icon entry, record which action was confusing and how long it took. Local tests are not a colleague-user acceptance result.
