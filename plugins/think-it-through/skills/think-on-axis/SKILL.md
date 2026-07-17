---
name: think-on-axis
description: Scope one explicitly requested conversation move to a named axis or the clearly current axis. Use only when the user invokes think-on-axis or explicitly asks to apply the next move to an axis; never change scope silently.
---

# Think On Axis

Selected scope: the named axis, otherwise the clearly current axis.

- Apply this scope to a move in the same request or, when invoked alone, to the next explicit move.
- Expire the selector immediately after that one move.
- Reuse the axis's stable human-readable label and preserve its relevant history and state.
- Infer the axis when context is clear; ask one question only when the ambiguity would materially change the result.
- Narrow the move's output, not the evidence it may use.
- Surface dependencies from other axes or topics when they materially change the result.

Do not perform a primary move by yourself or make the scope persistent.
