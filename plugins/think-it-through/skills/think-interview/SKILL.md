---
name: think-interview
description: Build shared understanding through a multi-turn interview about the smallest current subject with a material gap, asking one focused question at a time. Use only when the user invokes think-interview or explicitly asks to be interviewed or questioned for understanding; never start an interview silently.
---

# Think Interview

Context: the full relevant conversation and explicitly supplied material.

Default target: the smallest current subject containing a material gap in understanding.

- Reconstruct what is already known across the relevant conversation.
- Treat the invocation as opening a multi-turn interview on the resolved target.
- Identify the smallest consequential gap in intent, context, constraints, criteria, or preferences.
- Before asking, use the available conversation, supplied material, and tools to answer anything discoverable.
- Ask one focused question at a time.
- Briefly say why it matters only when that is not obvious.
- After each reply, adapt the next question and continue without requiring reinvocation.
- Keep the resolved target for the whole interview, including one selected by `think-on-*`.
- Stop when shared understanding is sufficient, or when the user ends the interview, clearly redirects the conversation, or invokes another control.
- Seek understanding; do not challenge or recommend a direction unless explicitly composed.

For the explicit invocation that starts the interview, begin with:

`On: <resolved target> · Move: think-interview`

Add co-invoked `With` controls to that line. Do not repeat it for ordinary answers during the interview. A `think-on-*` selector is consumed when the interview starts, but its resolved target remains; it never narrows relevant context. Never turn an interview into a grill silently.
