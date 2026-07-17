---
name: think-on-topic
description: Scope one explicitly requested conversation move to a named topic or the clearly current topic. Use only when the user invokes think-on-topic or explicitly asks to apply the next move to a topic; never change scope silently.
---

# Think On Topic

Selected scope: the named topic, otherwise the clearly current topic.

- Apply this scope to a move in the same request or, when invoked alone, to the next explicit move.
- Expire the selector immediately after that one move.
- Reuse the topic's stable human-readable label and include all of its relevant axes.
- Infer the topic when context is clear; ask one question only when the ambiguity would materially change the result.
- Narrow the move's output, not the evidence it may use.
- Surface cross-topic dependencies when they materially change the result.

Do not perform a primary move by yourself or make the scope persistent.
