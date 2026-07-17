---
name: think-on-topic
description: Target one explicitly requested move, modifier, or artifact projection at a named topic or the clearly current topic. Use only when the user invokes think-on-topic or explicitly asks to apply a control to a topic; never change target silently.
---

# Think On Topic

Context: the full relevant conversation and explicitly supplied material.

Default target: the topic named by the user, otherwise the clearly current topic.

- Resolve the human label; infer the topic only when unambiguous.
- Ask one brief question only when multiple plausible topics would materially change the result.
- Apply this selector to a move, modifier, or projection in the same request, or to the next explicit control.
- Expire it immediately after that control.
- Include every relevant axis under the topic.
- Change only the target. Reintroduce outside evidence or dependencies when they materially affect the result.
- Do not perform an operation or create persistent state by itself.

When invoked alone, respond only:

`Scope set: topic "<resolved topic>" · Applies to: next control`
