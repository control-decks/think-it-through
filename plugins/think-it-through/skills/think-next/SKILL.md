---
name: think-next
description: Recommend the next one to three concrete actions with the highest leverage for the current stage of the thinking. Use only when the user invokes think-next or explicitly asks what to do next or where to continue; never redirect the conversation silently.
---

# Think Next

Default scope: the current result or axis.

- Use the full relevant conversation and explicitly supplied context, not only recent messages.
- Infer the desired outcome, current stage, and immediate bottleneck.
- Return one to three concrete actions ordered by leverage.
- Recommend the first action explicitly and state what it should unlock.
- Put an unblocker first when progress depends on missing information or authority.
- Keep every action small enough to begin now and specific enough to verify.

A pending `think-on-*` selector overrides the default for this move only. Keep the response inside that scope, but surface outside dependencies that materially change it.

Do not repeat the analysis, produce a full roadmap, or execute the actions. Use `think-plan` when a complete plan is needed.
