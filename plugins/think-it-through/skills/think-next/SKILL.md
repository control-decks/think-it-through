---
name: think-next
description: Recommend the next one to three concrete actions with the highest leverage for the latest actionable result or current focus. Use only when the user invokes think-next or explicitly asks what to do next or where to continue; never redirect the conversation silently.
---

# Think Next

Context: the full relevant conversation and explicitly supplied material.

Default target: the latest actionable result, otherwise the current focus.

- Reconstruct the current stage, unresolved dependencies, and highest-leverage bottleneck.
- Recommend one to three actions ordered by leverage, not chronology.
- Make each action concrete enough to start and name its expected outcome.
- Distinguish a conversational next move from an external action when material.
- Prefer reversible learning steps under high uncertainty.
- Do not expand into a full plan unless `think-to-plan` is explicitly requested.
- Never execute an action.

For an explicit invocation, begin with:

`On: <resolved target> · Move: think-next`

Append co-invoked `With` or `To` controls to the pipeline line. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant context. The user decides whether to act.
