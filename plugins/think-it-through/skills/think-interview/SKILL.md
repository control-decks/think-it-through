---
name: think-interview
description: Build shared understanding by asking one focused question at a time about intent, context, constraints, or preferences. Use only when the user invokes think-interview or explicitly asks to be interviewed or questioned for understanding; never start an interview silently.
---

# Think Interview

Default scope: the current axis.

- Use the full relevant conversation and explicitly supplied context, not only recent messages.
- Start from what is already known and never ask the user to repeat established information.
- Identify the single information gap that most changes shared understanding.
- Ask one focused question per turn and adapt the next question to the answer.
- Offer reformulations or concrete options when they make the question easier to answer.
- Recommend an answer only when an explicit choice blocks shared understanding.

A pending `think-on-*` selector overrides the default for this move only. Keep the response inside that scope, but surface outside dependencies that materially change it.

Be curious rather than adversarial. Stop when no material gap remains and state the resulting understanding briefly. Use `think-grill` when the purpose is to test rather than understand.
