---
name: think-with-reasoning-map
description: Expose the structure of the reasoning behind a co-invoked result or current proposal or decision without inventing missing logic. Use only when the user invokes think-with-reasoning-map or explicitly asks for an argument or reasoning map; never expose one silently.
---

# Think With Reasoning Map

Context: the full relevant conversation and explicitly supplied material.

Default target: the reasoning co-invoked in the same request, otherwise the current proposal or decision.

- Apply immediately to the result produced in the same request, or to the current reasoning when invoked alone.
- Map identifiable claims, evidence, premises, assumptions, inferences, implications, and objections.
- Use an argument map for an argumentative claim; use a broader reasoning map for a decision or system.
- Distinguish stated reasoning from inferred links and mark uncertainty explicitly.
- Preserve objections and unsupported jumps instead of repairing them silently.
- Do not invent evidence, premises, causality, or confidence.
- Ask one focused question if no identifiable reasoning can be mapped.
- Create no persistent modifier state.

For an explicit composition, append ` · With: reasoning-map`.

When standalone, begin with `On: <resolved target> · With: reasoning-map`. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant context. Never turn mapping into a challenge or new decision silently.
