---
name: think-on-conversation
description: Target one explicitly requested move, modifier, or artifact projection at the entire available conversation. Use only when the user invokes think-on-conversation or explicitly asks to apply a control conversation-wide; never change target silently.
---

# Think On Conversation

Context: the full relevant conversation and explicitly supplied material.

Default target: the full available conversation.

- Apply this selector to a move, modifier, or projection in the same request, or to the next explicit control.
- Expire it immediately after that control.
- Include all identifiable topics and axes still available plus explicitly imported checkpoints.
- Do not imply access to unavailable history or another conversation.
- Change only the target. Never discard evidence or dependencies needed to reason correctly.
- Do not perform an operation or create persistent state by itself.

When invoked alone, respond only:

`Scope set: conversation · Applies to: next control`
