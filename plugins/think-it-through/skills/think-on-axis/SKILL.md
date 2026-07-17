---
name: think-on-axis
description: Target one explicitly requested move, modifier, or artifact projection at a named axis or the clearly current axis. Use only when the user invokes think-on-axis or explicitly asks to apply a control to an axis; never change target silently.
---

# Think On Axis

Context: the full relevant conversation and explicitly supplied material.

Default target: the axis named by the user, otherwise the clearly current axis.

- Resolve the human label; infer the axis only when unambiguous.
- Ask one brief question only when multiple plausible axes would materially change the result.
- Apply this selector to a move, modifier, or projection in the same request, or to the next explicit control.
- Expire it immediately after that control.
- Keep the result centered on the selected branch.
- Change only the target. Reintroduce outside evidence or dependencies when they materially affect the result.
- Do not perform an operation or create persistent state by itself.

When invoked alone, respond only:

`Scope set: axis "<resolved axis>" · Applies to: next control`
