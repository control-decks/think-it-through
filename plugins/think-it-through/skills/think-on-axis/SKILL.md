---
name: think-on-axis
description: Target an explicit command combo at a named axis or the clearly current axis. Use only when the user invokes think-on-axis or asks to apply commands to an axis; never change the target silently.
---

# 🎯 Think On Axis

**Context:** The full relevant conversation and explicitly supplied material.
**Use when:** A combo should focus on one branch inside a topic.
**Default target:** The named axis, otherwise the unambiguous current axis.
**Job:** Resolve the human label and apply that axis to the combo in the same request or the next explicit combo.
**Result:** An axis-level target.
**Runs for:** One combo, then clear. A multi-turn interview or grill keeps the selected target until its loop ends.
**Limits:** Ask once if several axes could change the result. The agent can still use relevant context outside the target. Do not create a new axis, run another command, or create persistent state.
**Combines with:** Apply before all jobs in semantic order, even when written elsewhere. The first job consumes this target; later jobs consume the preceding result.

## Flow

`resolve target → apply to whole combo → apply once, then clear`

## Format

When invoked alone, respond only:

`Target set: axis "<axis>" · Applies to: next combo`

In a combo, use `🎯 **Axis: <axis>**` as the first item in the trace. Ask one clarification if another selector appears in the same combo.
