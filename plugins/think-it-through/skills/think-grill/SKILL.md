---
name: think-grill
description: Stress-test the current testable proposal, assumption, decision, or plan through rigorous one-question-at-a-time scrutiny. Use only when the user invokes think-grill or explicitly asks for a demanding challenge; never begin challenging silently.
---

# Think Grill

Context: the full relevant conversation and explicitly supplied material.

Default target: the proposal, assumption, decision, or plan currently testable.

- Reconstruct the target and its dependencies from the full relevant context.
- Challenge the branch whose failure would most change the outcome.
- Examine evidence, counterexamples, tradeoffs, incentives, dependencies, and failure modes.
- Ask exactly one demanding question per response.
- Pair every question with a concise current assessment or recommendation.
- Follow the answer into the next unresolved branch instead of running a checklist.
- Separate fact, inference, and unresolved claim. Stop when the target is robust, rejected, or an explicit risk.

For an explicit invocation, begin with:

`On: <resolved target> · Move: think-grill`

Add co-invoked `With` controls to the pipeline line. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant evidence. Challenge only by explicit request and never decide for the user.
