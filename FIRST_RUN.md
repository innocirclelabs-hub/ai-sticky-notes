# First use: floating AI Sticky Notes (Windows beta v0.4.29-beta.2)

This is an invited colleague evaluation build, not the finished public service.
You do not need a terminal, Python, npm, a publisher-operated server or a publisher API key. An authorized OpenAI tunnel and the tester's own account approval are still required.

## Five actions in order

1. Unzip the official Release package. Run AI-Sticky-Notes-Setup.exe, click Local diagnostic, and install its extension directory through Chrome extensions > Developer mode > Load unpacked. Chrome must show AI Sticky Notes.
2. In Setup, select Tunnel settings and create/select a tunnel in YOUR authorized OpenAI workspace. Use a dedicated runtime credential with Tunnels Read + Use. Select the credential file or environment-variable reference; never paste the actual key into chat or Setup. This step is controlled by OpenAI account permissions and cannot be silently automated.
3. Click Save & start and confirm both Local MCP: READY and OpenAI tunnel: READY. This does not yet prove a ChatGPT conversation is connected.
4. In your ChatGPT account, enable the AI Sticky Notes custom MCP application linked to your own tunnel. Click Open ChatGPT + copy first request in Setup; paste the copied request in an EXISTING conversation and send it. The phrase is: Open AI Sticky Notes in this conversation. The helper NEVER sends a chat message automatically.
5. Look for the movable yellow sticky note OVER your Chrome chat. Confirm that this note itself says AI connected, then ask ChatGPT for a small two-step practice task, review the plan once and check the actual AI note read/completion. If the note is hidden, click the yellow Chrome extension icon. If it still says not paired, verify the tunnel and that the app is enabled in this chat.

## Why the plugin may briefly show a small connection notice

The ChatGPT tool must securely pair its host-authenticated conversation with the installed Chrome extension. Its small one-time launcher transports this short-lived pairing proof, but it is NOT a second editable sticky note. All full note interaction is in the movable Chrome overlay. The host may keep the small launcher notice visible in the conversation until you dismiss it; a third-party plugin cannot remove the host's card container by force.

If Chrome extension is missing or disabled, the plugin alone cannot draw a draggable page overlay. Install the bundled extension explicitly. Do not interpret a plugin-card display as successful browser pairing.

## What each status means

- Local MCP READY: the program on your own PC started; NOT cloud server.
- OpenAI tunnel READY: your own outgoing tunnel connected; NOT proof your chat has permission.
- Chrome overlay AI connected: current browser conversation is paired to the local program.
- AI read record: ChatGPT actually called the plugin read tool for this work. The overlay cannot force every AI reply to use a tool.

If connection fails, the Setup next-action line and TROUBLESHOOTING.md point to the relevant step. Never publish keys, tunnel identifiers, actual private notes or screenshots with credentials.

## Korean / 한국어 빠른 시작

압축 해제 → 설정 실행 → Chrome 확장 설치 → 내 OpenAI 터널 및 전용 인증 경로 승인 → 저장·연결 시작 → ChatGPT 사용자 MCP 연결 승인 → 설정의 'ChatGPT 열고 첫 요청 복사' 클릭 → 기존 대화에 붙여넣어 전송 → 화면 위 노란 포스트잇의 'AI 연결됨' 확인.

설정·연결 안내는 사용자가 해야 하는 다음 단계만 보여줍니다. 앱이 메시지를 대신 전송하지 않으며, 키 원문을 채팅이나 설치 프로그램에 붙여넣지 않습니다. 터널을 만들 권한이 없다면 이를 숨기지 않고 계정/관리자 권한 제한으로 보고합니다. 설치 진행 시간과 막힌 단계를 TEST_CHECKLIST.md에 기록하세요.

If it still fails after reinstalling, click Copy safe connection report in Setup and share only that reviewed JSON. See CONNECTION_DIAGNOSTICS.md. Do not reset the Chrome extension, account, keys or notes as a first response.