# ABIS Interior for Gemini CLI

Prepare an ABIS photo-design entry with selected room/style choices, consulting proposals, PDF and automatic sharing. Read public interior planning answers and, when requested, verified consultation links.

## Install

```sh
gemini extensions install https://github.com/itproanalysis/abis-gemini-extension
```

Restart Gemini CLI and use `/mcp` to check `abis`. This is a remote Streamable HTTP connection. No ABIS login, API key, local server, dependency install or additional executable is needed. Gemini CLI itself uses your existing Google authentication and applicable plan.

For a downloaded ZIP, extract the archive and run `gemini extensions install <extracted-folder>` instead. Do not install the ZIP file directly.

## Examples

- 좁은 거실의 가구 배치를 ABIS 자료로 설명하고 확인할 치수와 출처를 알려줘.
- 우리 집 사진으로 인테리어 시안과 자재·조명 제안서를 만들고 싶어요.
- 주방을 내추럴 스타일로 바꿔보고 싶어요. 사진 선택 화면으로 연결해줘.
- 욕실 공사 전에 확인할 ABIS 체크리스트와 요청할 때 이용할 수 있는 상담 방법을 알려줘.

## Tools and limits

`search_interior_answers`, `get_interior_answer`, `get_interior_styles` and `get_consultation_options` read public material only. They do not access customer data, generate paid images, place calls, submit leads or book appointments. Photos and AI photo design are separate website features. Planning guidance does not replace measured plans, structural assessments or fixed quotations. Contact and visit times must be agreed separately.

For photo redesign and style-in-your-home requests, `get_interior_styles` accepts `source: "gemini"` and optional `room`/`style`; `designWorkflow.url` opens the ABIS photo-selection screen with those choices preserved. Keep automatic recommendation when the user has not chosen. The user selects one photo and requests generation on the website; the written brief is optional. Preparing this link does not upload an image or start a generation job.

This extension is for **Gemini CLI**. Installing it does not list ABIS in the consumer Gemini app or enable it for every Google account. Supported Gemini app accounts can separately add the public MCP URL in Connected Apps, subject to Google's current availability and consent flow.

## Privacy and support

The extension has no scripts, hooks, local file readers, credentials or analytics. Minimal search terms are sent to `https://abis.now/api/mcp/public`. ABIS returns public content and uses temporary rate-limit identifiers; it does not store raw public-tool queries in its application database. Hosting providers may keep technical request logs. Do not send personal data or full conversation history. Gemini's handling of conversations and tools is governed by Google's own policies.

- [Setup, scope and live preview](https://abis.now/integrations)
- [Privacy policy](https://abis.now/legal/privacy)
- [Terms](https://abis.now/legal/terms)
- [Support](https://abis.now/support)
- [ABIS](https://abis.now)

License: MIT, for this extension's configuration and documentation only. The ABIS service and backend are separate.
