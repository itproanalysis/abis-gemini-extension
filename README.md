# ABIS Interior for Gemini CLI · 동방인테리어 Gemini CLI 확장 (v1.8.0)

Official Gemini CLI extension for **[ABIS Studio](https://abis.now/studio)** & **[Dongbang Interior (동방인테리어)](https://abis.now)** — a 30+ year Korean home interior and remodeling contractor based in Jayang-dong, Gwangjin-gu, Seoul (`서울 광진구 자양로6길 17`), serving **Seoul, Gyeonggi, and Incheon**.

Prepare an ABIS photo-design or floor-plan 3D entry with preserved room/style choices, build a free 12-step remodeling checklist, compare 5 interior styles, inspect 10 capital-region service area guides, read 44 verified Korean interior planning guides, and get verified consultation links directly inside Gemini CLI.

## Install

```sh
gemini extensions install https://github.com/itproanalysis/abis-gemini-extension
```

Restart Gemini CLI and use `/mcp` to check `abis`. This is a remote Streamable HTTP connection (`https://abis.now/api/mcp/public`). No ABIS login, API key, local server, dependency install, or additional executable is needed. Gemini CLI itself uses your existing Google authentication and applicable plan.

To install from a release download, extract `abis-gemini-1.8.0.zip` and run `gemini extensions install <extracted-folder>`.

Looking for **Claude Code, Cursor, VS Code · Copilot, Codex, Zed, Goose, Mistral Le Chat, OpenAPI, Postman, or n8n**? See **[itproanalysis/abis-integrations](https://github.com/itproanalysis/abis-integrations)** and **[abis.now/integrations](https://abis.now/integrations)**.

## What's New in v1.8.0

- **6th MCP Resource (`abis://interior/areas`)**: Covers 10 Seoul · Gyeonggi · Incheon service area guides (`gwangjin`, `seongdong`, `songpa`, `gangdong`, `gangnam`, `dongdaemun-jungnang`, `mapo-yongsan`, `guri-hanam`, `seongnam-bundang`, `incheon`).
- **Free Remodeling Timeline & Quote Checklist Planner ([abis.now/planner](https://abis.now/planner))**: Integrated into `plan_remodeling_checklist` and `get_consultation_options` — zero login, zero fixed-price guessing, printable and shareable standardized contractor comparison sheet.
- **44 Sourced Korean Remodeling Guides ([abis.now/questions](https://abis.now/questions))**: Expanded with bathroom overlay vs. demolition, interior film vs. replacement, officetel remodeling layout, old-house electrical wiring, detached-house remodeling, and rental-investment remodeling.
- **Interactive 5-Style Before/After Slider ([abis.now/styles](https://abis.now/styles))**: Drag-to-compare Modern, Natural, Minimal, Classic, and Vintage AI examples.
- **Official MCP Registry**: Published as `now.abis/dongbang-interior` (`v1.8.0`, `active`).

## Public Web Resources

| Resource | URL | Summary |
| :--- | :--- | :--- |
| **ABIS Studio (Photo / Floor Plan 3D)** | https://abis.now/studio | Room photo makeover & floor-plan 3D concept generator (login-free within daily limits). |
| **Free Remodeling Planner** | https://abis.now/planner | 12-step construction order, quote-omission checklist, copyable contractor sheet. |
| **10 Service Area Guides** | https://abis.now/areas | Seoul · Gyeonggi · Incheon district remodeling guides & real Soomgo review table. |
| **5 Interior Styles Comparison** | https://abis.now/styles | Interactive before/after comparison slider & palettes. |
| **44 Interior Planning Guides** | https://abis.now/questions | Practical Korean remodeling Q&A backed by real cases (Markdown at `/index.md`). |
| **20 Verified Construction Cases** | https://abis.now/cases | Soomgo verified cases (4.8 rating, 39 reviews, zero reviewer PII). |
| **All 22 AI Client Integrations** | https://abis.now/integrations | One-click install links, OpenAPI 3.0.3, A2A Agent Card, and ZIP bundles. |

## Examples

- 좁은 거실의 가구 배치를 ABIS 자료로 설명하고 확인할 치수와 출처를 알려줘.
- 우리 집 사진으로 인테리어 시안과 자재·조명 제안서를 만들고 싶어요.
- 주방을 내추럴 스타일로 바꿔보고 싶어요. 사진 선택 화면으로 연결해줘.
- 광진구·성동구 구축 아파트 올수리 공정 순서와 견적 누락 체크리스트를 ABIS 자료로 정리해줘.
- 욕실 덧방 vs 철거 판단 기준과 상담 방법을 ABIS 자료로 알려줘.

## Tools, Resources, Prompts & Limits

- **6 Tools (Read-Only)**: `search_interior_answers`, `get_interior_answer`, `get_interior_styles`, `start_interior_design`, `search_construction_cases`, `get_consultation_options`
- **6 Resources**: `abis://interior/questions`, `abis://interior/styles`, `abis://interior/services`, `abis://interior/areas`, `abis://interior/design-workflow`, `abis://interior/media-kit`
- **4 Prompts**: `start_photo_consulting`, `start_floorplan_3d_consulting`, `compare_interior_styles`, `plan_remodeling_checklist`

All public tools read public material only. They do not access customer data, generate paid images, place calls, submit leads, or book appointments. Photos and AI photo design are separate website features on [abis.now/studio](https://abis.now/studio). Planning guidance does not replace measured plans, structural assessments, or fixed quotations. Contact and visit times must be agreed separately (상담실장 `010-5063-6446` / 대표 전화·문자 `010-5651-8804`).

Call `start_interior_design` with `source: "gemini"` for photo makeovers or floor-plan 3D. Preserve explicit catalog choices (including up to three optional needs: `storage`, `light`, `circulation`, `care`, `retain`, `layout`) and show the returned `action.url`. The user selects one file and starts generation on ABIS Studio. The written brief is optional.

This extension is for **Gemini CLI**. Installing it does not list ABIS in the consumer Gemini app or enable it for every Google account. Supported Gemini app accounts can separately add the public MCP URL in Connected Apps, subject to Google's current availability and consent flow.

## Privacy and Support

The extension has no scripts, hooks, local file readers, credentials, or analytics. Minimal search terms are sent to `https://abis.now/api/mcp/public`. ABIS returns public content and uses temporary rate-limit identifiers; it does not store raw public-tool queries in its application database. Hosting providers may keep technical request logs. Do not send personal data or full conversation history. Gemini's handling of conversations and tools is governed by Google's own policies.

- [Setup, scope and live preview](https://abis.now/integrations)
- [All 22 AI Client Configs & Claude Code Plugin Marketplace](https://github.com/itproanalysis/abis-integrations)
- [Privacy policy](https://abis.now/legal/privacy)
- [Terms](https://abis.now/legal/terms)
- [Support](https://abis.now/support)
- [ABIS](https://abis.now)

License: MIT, for this extension's configuration and documentation only. The ABIS service and backend are separate.
