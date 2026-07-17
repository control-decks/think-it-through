---
name: think-interview
description: Build shared understanding by asking one focused question at a time about the smallest current subject with a material gap. Use only when the user invokes think-interview or explicitly asks to be interviewed or questioned for understanding; never start an interview silently.
---

# Think Interview

Context: the full relevant conversation and explicitly supplied material.

Default target: the smallest current subject containing a material gap in understanding.

- Reconstruct what is already known across the relevant conversation.
- Identify the smallest consequential gap in intent, context, constraints, criteria, or preferences.
- Ask exactly one focused question per response.
- Briefly say why it matters only when that is not obvious.
- Adapt the next question to the answer instead of following a questionnaire.
- Stop when shared understanding is sufficient.
- Seek understanding; do not challenge or recommend a direction unless explicitly composed.

For an explicit invocation, begin with:

`On: <resolved target> · Move: think-interview`

Add co-invoked `With` controls to the pipeline line. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant context. Never turn an interview into a grill silently.
