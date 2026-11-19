# ABIS interior planning

Use ABIS only when the user requests interior planning, home remodeling preparation, style comparisons, or ABIS consultation information. For unrelated tasks, do not call ABIS.

- Search public planning material with `search_interior_answers`, then read matching slugs with `get_interior_answer`. Explain relevant guidance in the user's language and cite the returned public source URLs. If no relevant material is found, say so.
- When the user asks for actual construction examples or reviews, use `search_construction_cases` and cite its returned case URLs. Never present an AI concept as a completed construction photograph or invent matching dimensions and prices.
- For a visual proposal for the user's own space, call `start_interior_design` with `source: "gemini"` and set `inputKind` to `photo` or `floorplan` when explicit. Pass only known room, style and concerns. Show `action.label` and `action.url` in the first reply. Use `get_interior_styles` for the style catalog.
- The link prepares the photo-upload screen. Do not say the tool generated an image, and do not upload a local or conversation photo on the user's behalf. The user chooses the photo and requests generation on ABIS. Do not append this workflow to unrelated requests or a general cost question that does not ask for visual design.
- Use `get_consultation_options` with `source: "gemini"` when the user requests human consultation or callback information. Return the requested contact options without submitting forms or placing calls.
- Send only the minimal interior search terms needed. Never send conversation history, local files, account information, photos, contact details, memory or unrelated user context to these public tools.
- These tools read public information only. They cannot generate images, read customer workspaces, book appointments, submit leads or send messages. Photo design is a separate ABIS website feature at https://abis.now/studio with daily image limits.
- Do not invent dimensions, exact quotes, structural safety, partner service areas or confirmed schedules. Electrical, gas, waterproofing and structural work require appropriate professional assessment.

Documentation: https://abis.now/integrations
Privacy: https://abis.now/legal/privacy
Support: https://abis.now/consultation


For file preparation, supported image formats or how to review a 3D floor plan, read and cite the guide `floorplan-to-3d`. Use its `designStart` upload action only when useful to the user.

## 1.6.0 style comparison and expanded Korean remodeling guides

Use `get_interior_styles` or the `abis://interior/styles` resource (and the `compare_interior_styles` prompt) to cite the five visual style guides at `https://abis.now/styles`. `start_interior_design` now also returns `styleGuideUrl`, and `search_interior_answers` covers 31 public topics including entrance doors, old villas, partition walls, balcony extensions, old apartment renovations and estimate comparison.

## 1.3.0 construction references

Cite the answer URL for planning advice and the case URL for work documented in `caseReferences`. Retrieve a specific case with `search_construction_cases` and its exact public `id`. Use related planning guides when they address the question.

## 1.2.0 consulting shortcuts

The public server also offers named photo/floorplan consulting prompts and public product facts. Preserve room/style/concern selections, return the website upload link and do not claim an unseen image was analyzed or generated. English product introduction: https://abis.now/en; the current app interface and proposals are Korean.

## 1.1.0 consulting handoff

The six public tools cover answers, guidance, the style catalog, design entry, real construction cases and consultation links. Optional needs are storage, light, circulation, care, retain and layout (at most three explicitly selected IDs). Room, style and concerns are preserved in the upload entry. The preparation guide is not a diagnosis of an unseen image. The website shows priorities, retained elements and consultation checks, with PDF and automatic sharing. Never send photos, contacts or conversation history to public tools. A public MCP endpoint and downloadable package do not imply official directory approval.
