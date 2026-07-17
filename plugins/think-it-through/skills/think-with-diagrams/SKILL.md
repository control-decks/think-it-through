---
name: think-with-diagrams
description: Add the smallest useful diagram to a co-invoked or current result while preserving its substance. Use only when the user invokes think-with-diagrams or explicitly asks for a diagrammatic representation; never add decorative visuals silently.
---

# Think With Diagrams

Context: the full relevant conversation and explicitly supplied material.

Default target: the co-invoked result, otherwise the latest substantive result or current focus.

- Apply immediately to the result produced in the same request, or to the current result when invoked alone.
- Preserve every material claim, qualification, and uncertainty.
- Choose the smallest useful form: flow, tree, timeline, matrix, table, or Mermaid diagram.
- Encode real relationships such as sequence, hierarchy, dependency, contrast, or feedback.
- Do not decorate, duplicate surrounding prose, or introduce a new conclusion.
- For a brief or plan, place diagrams where they improve reuse rather than collecting them ornamentally.
- If no diagram would improve understanding, say so briefly and keep the representation minimal.
- Create no persistent modifier state.

For an explicit composition, append ` · With: diagrams`.

When standalone, begin with `On: <resolved target> · With: diagrams`. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant context. Never apply another control silently.
