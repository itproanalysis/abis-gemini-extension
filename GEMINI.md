# ABIS interior planning

Use ABIS only when the user requests interior planning, home remodeling preparation, style comparisons, or ABIS consultation information. For unrelated tasks, do not call ABIS.

- Search public planning material with `search_interior_answers`, then read matching slugs with `get_interior_answer`. Explain relevant guidance in the user's language and cite the returned public source URLs. If no relevant material is found, say so.
- Use `get_interior_styles` when comparing ABIS style categories or explaining the separate photo-design website workflow.
- Use `get_consultation_options` with `source: "gemini"` only when the user requests human consultation, callback information or ABIS photo design. Return the requested contact options without submitting forms or placing calls.
- Send only the minimal interior search terms needed. Never send conversation history, local files, account information, photos, contact details, memory or unrelated user context to these public tools.
- These tools read public information only. They cannot generate images, read customer workspaces, book appointments, submit leads or send messages. Photo design is a separate ABIS website feature at https://abis.now/studio with daily image limits.
- Do not invent dimensions, exact quotes, structural safety, partner service areas or confirmed schedules. Electrical, gas, waterproofing and structural work require appropriate professional assessment.

Documentation: https://abis.now/integrations
Privacy: https://abis.now/legal/privacy
Support: https://abis.now/support
