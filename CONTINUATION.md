# Continue the same work in a new conversation

**v0.4.29-beta.3 · Explicit same-project continuation · Windows / ChatGPT Web test build**

A conversation reaching its limit should not reset your task list. Continue one selected work group in another existing ChatGPT conversation without copying it into a second independently editable job.

## Three steps

1. Open or create your next conversation using ChatGPT itself, inside the **same ChatGPT project**. Connect AI Sticky Notes there using your own existing installation. If needed, explicitly ask the AI to open AI Sticky Notes once so that conversation can be paired.
2. In an empty task list, choose **Continue previous work**. When the conversation already has tasks, find that item inside the existing settings/more menu. Choose the intended task group, check its name, completion ratio and included rules, then press **Continue this work** once.
3. Ask the AI to continue that task. It must call `get_working_context` and use the matching work context before acting. The note itself does not inject a message or a Context attachment into the composer.

**Example:** a source work group with five verified tasks out of seven appears as **5/7 · 71%** in the destination. Completing the next real task advances that same group to **6/7 · 86%**, rather than creating a new 0/7 copy.

## What is preserved

The work-group and item IDs, order, approval status, completed checkmarks/red strikethroughs, evidence and timestamps remain attached to the same work. The saved group-fold choice is carried when available. Factual saved resume information can include the goal, scope, last checkpoint, remaining problems, artifact references and running-operation identifiers.

Only rules belonging to the selected work group travel with it. Conversation-only rules and unrelated work remain in the source conversation. Review the included-rules detail before accepting. If a necessary rule was stored only as a conversation-wide note, explicitly add it to the continued work; the software does not guess its scope.

The old conversation retains a read-only snapshot of the handoff under its collapsed history. It cannot keep editing the transferred work. Other work in the old conversation can continue normally.

## Projects and simultaneous work

Candidates are restricted to the same authenticated account and **verified project**. Titles are labels, not identity. Two projects with the same visible name do not become one project. Several jobs within a project remain separate groups and separate progress totals. There is no global 'current work' switch.

Only one destination can accept a particular current work state. If another conversation accepts first, or source work changes while the preview is open, refresh the selection; the stale request is rejected. Repeating a successful request does not duplicate the work.

## No last source message required

The feature uses the latest persisted work state. You do not need to obtain one final response from a source conversation that has already reached its limit. Work done outside the note store but not yet recorded is not inferred as completed. Inspect its actual result before retrying or marking it done.

## Boundaries

- The initial implementation requires a verified ChatGPT project. Unknown-project, ungrouped or different-project handoffs are refused rather than guessed.
- An unapproved draft remains unapproved after continuation. Existing external-tool permissions and costly or destructive approvals are not transferred.
- Archived and trashed groups are not silently activated; explicitly restore a group in its original conversation when that is really intended.
- Saved file paths and running job identifiers are references, not execution instructions. Verify access, file versions and job state before continuing. Do not rerun an unresolved operation simply because the conversation changed.
- Existing selected share grants are not broadened or resurrected. Old conversation messages cannot be erased by a handoff.
- The runtime must be available, and the destination must be paired to the same actual installation/account. This is not cloud backup or cross-device data migration.
- No automatic @Context note-summary attachment is added by this flow.

## Quick check

Use non-sensitive sample work. Stop at 5/7 in A, continue it in B, confirm the five evidence records and selected rule, then complete one actual step. Refresh B and confirm 6/7 remains. Verify A cannot apply its old update, and another project's work stays unchanged. Record results in TEST_CHECKLIST.md; a local diagnostic is not your account's end-to-end result.

## 한국어 요약

같은 ChatGPT 프로젝트의 새 대화에서 포스트잇을 연결한 다음 **이전 작업 이어받기 → 작업 선택 → 이 작업 이어받기**를 한 번 누르세요. 기존 대화가 이미 한도에 걸렸어도 마지막 저장된 작업을 가져올 수 있습니다. 5/7 완료와 근거가 유지되며 다른 프로젝트·다른 작업은 합치지 않습니다. 새 AI에게 이어서 진행하도록 요청하면 실제 MCP로 작업별 규칙과 재개 정보를 읽어야 합니다. 입력창에 문맥을 강제로 붙이지 않습니다. 프로젝트가 확인되지 않는 경우는 자동으로 추측하지 않습니다.