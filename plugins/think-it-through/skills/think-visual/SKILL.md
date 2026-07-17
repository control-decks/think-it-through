---
name: think-visual
description: Express the selected reasoning or result with the smallest useful diagram, table, tree, timeline, matrix, or other visual structure while preserving its substance. Use only when the user invokes think-visual or explicitly asks for a visual explanation; never add decorative visuals silently.
---

# Think Visual

Default scope: the co-invoked move's result, otherwise the current axis.

- Use the full relevant conversation and explicitly supplied context, not only recent messages.
- When composed with another move, preserve that move's substance and change only its form.
- When invoked alone, visualize the current focus without inventing a new conclusion.
- Choose the smallest useful form: table for mappings, flow for sequence, tree for branching, timeline for change, matrix for tradeoffs, or Mermaid for relationships.
- Keep labels short and preserve uncertainty, causality, and cross-axis links accurately.
- Add only the explanation required to read the visual.

A pending `think-on-*` selector overrides the default for this move only. Keep the response inside that scope, but surface outside dependencies that materially change it.

Do not create decorative structure, duplicate the same content in prose, or let the visual alter the reasoning.
