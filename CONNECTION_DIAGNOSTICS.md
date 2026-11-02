# Safe connection diagnostics — v0.4.29-beta.3

Invited Windows x64 / Chrome / ChatGPT test release. No publisher-owned server, key or tunnel.

## Before reinstalling again

1. Open AI-Sticky-Notes-Setup.exe in the complete latest ZIP folder.
2. Keep only one copy running; an existing tray instance may retain port 8791. Stop that instance via its OWN Stop connection and tray Exit. Do not kill unknown processes.
3. Click Copy safe connection report / 민감정보 제외 진단 보고서 복사. Review the JSON and send ONLY this safe report. It is also stored locally under %APPDATA%/AI-Sticky-Notes-Beta/diagnostics/connection-last.json.
4. If Setup will not open, from a PowerShell console in the extracted folder, run:

    .\AI-Sticky-Notes-Setup.exe --connection-diagnostic --output "$env:TEMP\ai-sticky-notes-safe-report.json"

This probe does not start the tunnel, connect any account, modify notes, or open credential files.

## Understanding the result

- local_port_8791: free — the actual production port was free at inspection time.
- local_port_8791: occupied_unidentified — another listener exists. Do not forcibly terminate or overwrite its owner.
- local_port_8791: listening_expected_product — the listener returned the expected product health marker; no claim of authenticated ChatGPT use.
- openai_tunnel_health: ready_observed — a local health endpoint reported READY, not a ChatGPT permission test.
- openai_tunnel_health: not_ready / not_observed / unreachable — check your personal tunnel, credential reference, workspace and network.
- configuration.saved: saved / not_saved / unreadable — reports only the status, not the saved ID or path.
- configuration.credential_reference: file_present / file_missing / environment_present / environment_not_available / invalid_reference — checks existence only, not the key itself.
- process_events: openai_tunnel:AUTH_OR_PERMISSION — process output matched a fixed category; source text is discarded.
- process_events: openai_tunnel:OAUTH_DISCOVERY_WARNING — informational warning, not conclusive proof of a connection failure.
- chatgpt_custom_mcp: not_checked_requires_account — the local helper cannot attest account permissions.
- next_action_code — a direction for diagnosis, not an automatic fix.

Local diagnostic 11/11 uses a temporary port and cannot establish that real port 8791 is free. Likewise a visible note or tunnel READY does not prove the AI called list_notes.

## Share safely

The generated report stores only fixed event codes, counts, status labels and UTC date. It must NOT include raw stdout/stderr, API keys, real tunnel IDs, credential-file contents or paths, user note bodies or conversations. Still review it before sending. Never send connection.json, notes.sqlite, key files, raw process logs or unredacted authentication screenshots.

A repeated reinstall does NOT automatically reset your OpenAI workspace tunnel or ChatGPT custom app settings.

## 한국어

설치 삭제를 반복하지 말고 설정 화면의 '민감정보 제외 진단 보고서 복사'를 눌러 JSON만 공유해 주세요. 실제 8791 포트 점유 여부, 터널 준비 상태, 설정·인증 경로 존재 여부를 구분합니다. 키 원문·터널 ID·인증 파일·대화 내용은 절대 보내지 마세요. 이 진단만으로 본인 ChatGPT 앱 권한이 확인되지는 않습니다.