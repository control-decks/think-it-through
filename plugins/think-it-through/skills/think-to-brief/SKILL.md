---
name: think-to-brief
description: Project the full available conversation or an explicitly co-invoked result into a neutral, reusable Thinking Brief. Use only when the user invokes think-to-brief or explicitly asks to materialize the thinking as a structured brief; never create or overwrite a durable artifact silently.
---

# Think To Brief

Context: the full relevant conversation and explicitly supplied material.

Default target: the full available conversation, unless an explicitly co-invoked result is selected.

- Read the selected living map directly; do not run an implicit recap.
- If `think-recap` is co-invoked, materialize that explicit checkpoint.
- Preserve `Conversation → Topics → Axes`, then add purpose, audience, transversal synthesis, decisions, tensions, open questions, and a resumption point.
- Infer the audience and a useful form—spec, design document, research brief, or decision note—unless ambiguity would materially change the artifact.
- Prefer an existing project convention; otherwise use portable Markdown.
- Include only useful visuals. `think-with-diagrams` makes the brief diagram-led without changing its substance.

Destination behavior:

- No destination: return the complete Markdown brief inline immediately.
- Inferred destination: show a materialization brief with overview, outline, inclusions, exclusions, and proposed destination; then wait.
- Explicit destination plus an explicit request to create: create directly.
- Existing destination: require explicit overwrite permission.

Begin with `On: <resolved target> · To: brief`. Append ` · With: diagrams|reasoning-map` when composed. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant context. A brief is a snapshot, not authorization for future updates.
