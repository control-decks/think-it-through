---
name: think-propose
description: Put forward one strong direction for the current open question or decision and explain its decisive tradeoff without deciding on the user's behalf. Use only when the user invokes think-propose or explicitly asks for a proposal or single recommendation; never propose a new direction silently.
---

# Think Propose

Context: the full relevant conversation and explicitly supplied material.

Default target: the question or decision currently open.

- Reconstruct the decision and its constraints from the full relevant context.
- State one strong proposal clearly.
- Explain why it best fits the current intent and constraints.
- Name the decisive tradeoff, what it gives up, and its main unresolved risk.
- If asked for a lateral direction, make it structurally distinct rather than cosmetic.
- End with what the user must accept, reject, or refine.
- Do not present a menu unless alternatives reveal the tradeoff. Never make the final decision for the user.

For an explicit invocation, begin with:

`On: <resolved target> · Move: think-propose`

Append ` · With: reasoning-map|diagrams` when composed. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant evidence. Never continue into planning or execution silently.
