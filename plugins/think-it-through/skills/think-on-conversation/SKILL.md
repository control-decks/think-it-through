---
name: think-on-conversation
description: Scope one explicitly requested conversation move to the entire current chat plus any context or checkpoints the user explicitly supplied. Use only when the user invokes think-on-conversation or explicitly asks to apply the next move across the whole conversation; never change scope silently.
---

# Think On Conversation

Selected scope: the full available conversation.

- Apply this scope to a move in the same request or, when invoked alone, to the next explicit move.
- Expire the selector immediately after that one move.
- Include every relevant topic and axis from the current chat and explicitly supplied context.
- Narrow the move's output, not the evidence it may use.
- Surface dependencies outside the apparent scope when they materially change the result.

Do not perform a primary move by yourself or imply memory across separate chats.
