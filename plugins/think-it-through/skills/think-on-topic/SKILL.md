---
name: think-on-topic
description: Target an explicit command combo at a named topic or the clearly current topic. Use only when the user invokes think-on-topic or asks to apply commands to a topic; never change the target silently.
---

# 🎯 Think On Topic

Context: the full relevant conversation and explicitly supplied material.

**When:** A combo should focus on one topic and all its relevant axes.
**On (default):** The named topic, otherwise the unambiguous current topic.
**Move:** Resolve the human label and bind that topic to the combo in the same request or the next explicit combo.
**Result:** A topic-level target.
**Cadence:** One-shot; expire after the combo. A multi-turn move retains the resolved target until its loop ends.
**Boundary:** Ask once if several topics would change the result. Do not remove outside dependencies, run a move, or create persistent state.
**Composition:** The first move consumes this target; later moves consume the preceding result.

**Flow:** `resolve target → bind whole combo → expire`

## Display

When invoked alone, respond only:

`Scope set: topic "<topic>" · Applies to: next combo`

In a combo, use `🎯 **Topic: <topic>**` as the first item in its signature.
