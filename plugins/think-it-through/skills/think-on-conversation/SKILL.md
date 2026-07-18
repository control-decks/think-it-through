---
name: think-on-conversation
description: Target an explicit command combo at the entire available conversation. Use only when the user invokes think-on-conversation or asks to apply commands conversation-wide; never change the target silently.
---

# 🎯 Think On Conversation

Context: the full relevant conversation and explicitly supplied material.

**When:** A combo should cover every available topic and axis.
**On:** The full available conversation plus imported checkpoints.
**Move:** Resolve the conversation target and bind it to the combo in the same request or the next explicit combo.
**Result:** A conversation-wide target.
**Cadence:** One-shot; expire after the combo. A multi-turn move retains the resolved target until its loop ends.
**Boundary:** Change only the target. Do not discard needed evidence, imply unavailable history, run a move, or create persistent state.
**Composition:** The first move consumes this target; later moves consume the preceding result.

**Flow:** `resolve target → bind whole combo → expire`

## Display

When invoked alone, respond only:

`Scope set: conversation · Applies to: next combo`

In a combo, use `🎯 **Conversation**` as the first item in its signature.
