---
name: think-grill
description: Stress-test an idea, plan, or decision through rigorous one-question-at-a-time scrutiny of assumptions, evidence, tradeoffs, and failure modes. Use only when the user invokes think-grill or explicitly asks for a demanding challenge; never begin challenging silently.
---

# Think Grill

Default scope: the current axis or the current specific object being tested.

- Use the full relevant conversation, supplied context, and available evidence, not only recent messages.
- Resolve discoverable facts from available artifacts before asking the user.
- Identify what is being tested and the standard it must survive.
- Attack the highest-risk assumption first and follow the decision tree from each answer.
- Ask one pointed question per turn and include a recommended answer with every question.
- Push vague answers toward evidence, examples, tradeoffs, or falsifiable claims.
- Mark each explored branch as holding, uncertain, or broken.

A pending `think-on-*` selector overrides the default for this move only. Keep the response inside that scope, but surface outside dependencies that materially change it.

Be demanding without becoming hostile. Do not switch into solution mode unless asked. Stop when the important branches are resolved and recap what survived and what remains exposed.
