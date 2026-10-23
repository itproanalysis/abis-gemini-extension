# ABIS Interior for Gemini CLI

Find public Korean interior planning answers, practical checklists and style references. When requested, retrieve ABIS and Dongbang Interior phone, Soomgo and callback links.

## Install

```sh
gemini extensions install https://github.com/itproanalysis/abis-gemini-extension
```

Restart Gemini CLI and use `/mcp` to check `abis`. This is a remote Streamable HTTP connection. No ABIS login, API key, local server, dependency install or additional executable is needed. Gemini CLI itself uses your existing Google authentication and applicable plan.

For a downloaded ZIP, extract the archive and run `gemini extensions install <extracted-folder>` instead. Do not install the ZIP file directly.

## Examples

- 좁은 거실의 가구 배치를 ABIS 자료로 설명하고 확인할 치수와 출처를 알려줘.
- ABIS의 모던·내추럴·미니멀·클래식·빈티지 스타일을 비교해줘.
- 욕실 공사 전에 확인할 ABIS 체크리스트와 요청할 때 이용할 수 있는 상담 방법을 알려줘.

## Tools and limits

`search_interior_answers`, `get_interior_answer`, `get_interior_styles` and `get_consultation_options` read public material only. They do not access customer data, generate paid images, place calls, submit leads or book appointments. Photos and AI photo design are separate website features. Planning guidance does not replace measured plans, structural assessments or fixed quotations. Contact and visit times must be agreed separately.

This extension is for **Gemini CLI**. Installing it does not list ABIS in the consumer Gemini app or enable it for every Google account. Supported Gemini app accounts can separately add the public MCP URL in Connected Apps, subject to Google's current availability and consent flow.

## Privacy and support

The extension has no scripts, hooks, local file readers, credentials or analytics. Minimal search terms are sent to `https://abis.now/api/mcp/public`. ABIS returns public content and uses temporary rate-limit identifiers; it does not store raw public-tool queries in its application database. Hosting providers may keep technical request logs. Do not send personal data or full conversation history. Gemini's handling of conversations and tools is governed by Google's own policies.

- [Setup, scope and live preview](https://abis.now/integrations)
- [Privacy policy](https://abis.now/legal/privacy)
- [Terms](https://abis.now/legal/terms)
- [Support](https://abis.now/support)
- [ABIS](https://abis.now)

License: MIT, for this extension's configuration and documentation only. The ABIS service and backend are separate.
