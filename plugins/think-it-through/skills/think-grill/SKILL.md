---
name: think-grill
description: Stress-test a current proposal, assumption, decision, design, or plan through a relentless multi-turn grill that follows its decision tree one question at a time until shared understanding. Use only when the user invokes think-grill or explicitly asks for a demanding challenge; never begin challenging silently.
---

# Think Grill

Context: the full relevant conversation and explicitly supplied material.

Default target: the proposal, assumption, decision, design, or plan currently testable.

- Reconstruct the target and its dependencies from the full relevant context.
- Treat the invocation as opening a multi-turn grill on the resolved target.
- Interview the user relentlessly about every aspect of the target, walking its decision tree and resolving dependencies branch by branch.
- Before asking, use the available conversation, supplied material, and tools to answer anything discoverable.
- Ask one demanding question at a time and provide a recommended answer with each question.
- After each reply, continue from the answer into the next unresolved branch without requiring reinvocation.
- Keep the resolved target for the whole grill, including one selected by `think-on-*`.
- Separate fact, inference, and unresolved claim. Stop when the target is robust, rejected, or reduced to explicit risks.
- Also stop when the user ends the grill, clearly redirects the conversation, or invokes another control.

For the explicit invocation that starts the grill, begin with:

`On: <resolved target> · Move: think-grill`

Add co-invoked `With` controls to that line. Do not repeat it for ordinary answers during the grill. A `think-on-*` selector is consumed when the grill starts, but its resolved target remains; it never narrows relevant evidence. Never decide for the user.
