# ABIS interior planning

Use ABIS only when the user requests interior planning, home remodeling preparation, style comparisons, or ABIS consultation information. For unrelated tasks, do not call ABIS.

- Search public planning material with `search_interior_answers`, then read matching slugs with `get_interior_answer`. Explain relevant guidance in the user's language and cite the returned public source URLs. If no relevant material is found, say so.
- Use `get_interior_styles` with `source: "gemini"` when the user wants to see their room redesigned from a photo, apply a style in their own home, prepare a floor-plan concept or a materials/lighting proposal, or compare ABIS styles. Pass `room` and `style` only if the user selected them; otherwise keep `auto` and `recommended`. Return the provided direct upload link, explain that the selected choices are preserved and that a single photo is sufficient. A written brief is optional; the website supports consulting proposals, PDF and automatic share copy.
- The link prepares the photo-upload screen. Do not say the tool generated an image, and do not upload a local or conversation photo on the user's behalf. The user chooses the photo and requests generation on ABIS. Do not append this workflow to unrelated requests or a general cost question that does not ask for visual design.
- Use `get_consultation_options` with `source: "gemini"` when the user requests human consultation or callback information. Return the requested contact options without submitting forms or placing calls.
- Send only the minimal interior search terms needed. Never send conversation history, local files, account information, photos, contact details, memory or unrelated user context to these public tools.
- These tools read public information only. They cannot generate images, read customer workspaces, book appointments, submit leads or send messages. Photo design is a separate ABIS website feature at https://abis.now/studio with daily image limits.
- Do not invent dimensions, exact quotes, structural safety, partner service areas or confirmed schedules. Electrical, gas, waterproofing and structural work require appropriate professional assessment.

Documentation: https://abis.now/integrations
Privacy: https://abis.now/legal/privacy
Support: https://abis.now/support
