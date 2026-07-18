---
name: think-on-axis
description: Target an explicit command combo at a named axis or the clearly current axis. Use only when the user invokes think-on-axis or asks to apply commands to an axis; never change the target silently.
---

# 🎯 Think On Axis

Context: the full relevant conversation and explicitly supplied material.

**When:** A combo should focus on one branch inside a topic.
**On (default):** The named axis, otherwise the unambiguous current axis.
**Move:** Resolve the human label and bind that axis to the combo in the same request or the next explicit combo.
**Result:** An axis-level target.
**Cadence:** One-shot; expire after the combo. A multi-turn move retains the resolved target until its loop ends.
**Boundary:** Ask once if several axes would change the result. Do not create a new axis, remove outside dependencies, run a move, or create persistent state.
**Composition:** The first move consumes this target; later moves consume the preceding result.

**Flow:** `resolve target → bind whole combo → expire`

## Display

When invoked alone, respond only:

`Scope set: axis "<axis>" · Applies to: next combo`

In a combo, use `🎯 **Axis: <axis>**` as the first item in its signature.
