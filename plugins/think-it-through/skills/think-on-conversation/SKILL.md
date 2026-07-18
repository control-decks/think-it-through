---
name: think-on-conversation
description: Target an explicit command combo at the entire available conversation. Use only when the user invokes think-on-conversation or asks to apply commands conversation-wide; never change the target silently.
---

# 🎯 Think On Conversation

**Context:** The full relevant conversation and explicitly supplied material.
**Use when:** A combo should cover every available topic and axis.
**Default target:** The full available conversation plus supplied checkpoints.
**Job:** Resolve the conversation target and apply it to the combo in the same request or the next explicit combo.
**Result:** A conversation-wide target.
**Runs for:** One combo, then clear. A multi-turn interview or grill keeps the selected target until its loop ends.
**Limits:** Change only the target. The agent can still use relevant context outside the target. Do not imply unavailable history, run another command, or create persistent state.
**Combines with:** Apply before all jobs in semantic order, even when written elsewhere. The first job consumes this target; later jobs consume the preceding result.

## Flow

`resolve target → apply to whole combo → apply once, then clear`

## Format

When invoked alone, respond only:

`Target set: conversation · Applies to: next combo`

In a combo, use `🎯 **Conversation**` as the first item in the trace. Ask one clarification if another selector appears in the same combo.
