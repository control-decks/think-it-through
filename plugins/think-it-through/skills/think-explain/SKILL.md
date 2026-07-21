---
name: think-explain
description: Explain the current HACP Working Object at the user's requested or apparent level with the minimum detail needed for understanding while preserving its claims and caveats. Use when the user invokes think-explain, asks for an explanation, or passes a result from another deck into EXPLAIN; never add an explanation silently.
---

# 💡 Think Explain

**Use when:** A concept, result, action, or blocked outcome needs to become easy
to understand.
**Default binding:** The current Working Object, otherwise the latest
substantive result or clearly named subject.
**Accepts:** Human-supplied content or any `success` or `blocked` HACP result.
Defer on `pending` unless the user asks to explain the proposed action.
**Effect:** Explain the smallest unclear point at the user's requested or
apparent level with only the details needed to understand it.
**Result:** A concise explanation that preserves the source object's claims,
caveats, and uncertainty.
**Duration:** One agent turn.
**Limits:** Do not invent evidence, change claims, advise, choose a direction,
repeat the complete source, add a tutorial about HACP, or use more than one
example unless the user asks.

## Format

Begin the complete combo trace with `> 🎯 **<binding>** → 💡 **EXPLAIN**` when
used alone. Add `→ 💡 **EXPLAIN**` after earlier cards in a combo.

Use `Explanation` as the only required heading. Add `Example` only when one
short example removes real ambiguity.
