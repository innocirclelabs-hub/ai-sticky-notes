# Pairing recovery — AI Sticky Notes v0.4.29-beta.3

**Windows desktop Chrome test build.** A ChatGPT open_postit tool result and a floating yellow note are NOT proof of real AI connection. The actual note must say AI connected / AI 연결됨.

## First try automatic pairing

Start your local Setup and your own authorized OpenAI tunnel. Enable AI Sticky Notes in the existing ChatGPT conversation and ask "포스트잇 열어줘". The plugin shows only a small connection notice. Check the floating note for "AI 연결됨".

## If the floating note still says AI 연결 대기

1. In the small ChatGPT connection notice expand **자동 연결이 안 됐나요?** (it can expand automatically after a short timeout).
2. Click **일회용 연결 코드 복사**. If clipboard permission is blocked, select the revealed code and press Ctrl+C.
3. In the existing movable yellow floating note, expand **연결 코드 직접 입력** near its bottom. Paste the code into that box; click **연결**.
4. Check the note changes to **AI 연결됨**. A code expires in about 90 seconds and is single-use; request "포스트잇 다시 열어줘" to obtain a new code after expiration.
5. Have ChatGPT actually call its list_notes/get_working_context tools for THIS conversation before saying AI read the notes.

The one-time code is a live authentication secret. NEVER paste it into the ChatGPT message, screenshots, issue tracker, support messages, GitHub, diagnostics, or raw logs. It must only travel between the host notice and the dedicated floating note connection control on YOUR PC. The code is not included in the safe local diagnostic report.

## What changed in beta.3

The old plugin notice could say "check the floating note" even when its automatic cross-origin postMessage was silently dropped. The new notice waits for a browser response, offers a single-use manual fallback on timeout, and the Chrome bridge acknowledges only after an authenticated pairing response. The Chrome overlay remains the only full editable note UI; no publisher-hosted service or key is introduced.

## 한국어 요약

ChatGPT에서 포스트잇을 열었지만 오른쪽 이동형 포스트잇에 **AI 연결 대기**가 보인다면, 채팅 안의 작은 연결 안내에서 **자동 연결이 안 됐나요? → 일회용 연결 코드 복사**를 누르세요. 다음으로 오른쪽 포스트잇 아래 **연결 코드 직접 입력 → 붙여넣기 → 연결**을 수행합니다. 약 90초가 지나면 새 코드를 요청해야 합니다. 인증 코드는 채팅에 보내거나 타인에게 공유하면 안 됩니다.