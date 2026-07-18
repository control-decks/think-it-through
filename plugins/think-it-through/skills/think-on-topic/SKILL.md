---
name: think-on-topic
description: Apply an explicit command combo to a named topic or the clearly current topic. Use only when the user invokes think-on-topic or asks to apply commands to a topic; never change the focus silently.
---

# 🎯 Think On Topic

**Use when:** A combo should focus on one topic and its relevant axes.
**Works on by default:** The named topic, otherwise the unambiguous current topic.
**Effect:** Resolve the human label and apply that topic to the combo in the same request or the next explicit combo.
**Result:** A topic-level focus.
**Duration:** One combo, then clear. A multi-exchange interview or grill keeps the selected focus until its loop ends.
**Limits:** Ask once if several topics could change the result. The agent can still use relevant context outside the focus. Do not run another command or create persistent state.
**Combines with:** Apply before all move cards in semantic order, even when written elsewhere. The first move works on this focus; later moves work on the preceding result.

## Flow

`resolve focus → apply to whole combo → apply once, then clear`

## Format

When invoked alone, respond only:

`Focus set: topic "<topic>" · Applies to: next combo`

In a combo, use `🎯 **Topic: <topic>**` as the first item in the trace. Ask one clarification if another focus card appears in the same combo.
