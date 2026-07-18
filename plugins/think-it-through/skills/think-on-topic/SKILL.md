---
name: think-on-topic
description: Target an explicit command combo at a named topic or the clearly current topic. Use only when the user invokes think-on-topic or asks to apply commands to a topic; never change the target silently.
---

# 🎯 Think On Topic

**Context:** The full relevant conversation and explicitly supplied material.
**Use when:** A combo should focus on one topic and its relevant axes.
**Default target:** The named topic, otherwise the unambiguous current topic.
**Job:** Resolve the human label and apply that topic to the combo in the same request or the next explicit combo.
**Result:** A topic-level target.
**Runs for:** One combo, then clear. A multi-turn interview or grill keeps the selected target until its loop ends.
**Limits:** Ask once if several topics could change the result. The agent can still use relevant context outside the target. Do not run another command or create persistent state.
**Combines with:** Apply before all jobs in semantic order, even when written elsewhere. The first job consumes this target; later jobs consume the preceding result.

## Flow

`resolve target → apply to whole combo → apply once, then clear`

## Format

When invoked alone, respond only:

`Target set: topic "<topic>" · Applies to: next combo`

In a combo, use `🎯 **Topic: <topic>**` as the first item in the trace. Ask one clarification if another selector appears in the same combo.
