---
name: think-distill
description: Clarify the intended meaning of the user's latest fragmented, implicit, or hard-to-word message, then respond to it or pass it to a co-invoked control. Use only when the user invokes think-distill or explicitly asks for their thought to be clarified before answering; never activate it silently.
---

# Think Distill

Context: the full relevant conversation and explicitly supplied material.

Default target: the latest human message, interpreted in its context.

- Reconstruct relevant context, including older topics or axes that change the message's meaning.
- Infer the intended claim, question, tension, or connection while preserving real ambiguity and the user's voice.
- Show `Distilled:` followed by the shortest faithful formulation.
- Then respond to that formulation.
- If another move or projection is co-invoked, pass it the distilled formulation instead of answering twice.
- If two materially different readings remain, show both and ask one discriminating question.
- Do not turn clarification into a recap, challenge, proposal, or plan unless explicitly composed.

For an explicit invocation, begin with:

`On: <resolved target> · Move: think-distill`

Add co-invoked `Move`, `To`, or `With` controls to the same pipeline line. A `think-on-*` selector overrides the target once, then expires; it never narrows relevant context. Never apply another control silently.
