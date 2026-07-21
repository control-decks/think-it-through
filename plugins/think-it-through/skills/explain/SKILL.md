---
name: explain
description: Explain the current HACP Working Object at the user's requested or apparent level with the minimum detail needed for understanding while preserving its claims and caveats. Use when the user invokes explain, asks for an explanation, or passes a result from another deck into EXPLAIN; never add an explanation silently.
disable-model-invocation: true
---

# 💡 Think Explain

**ID:** `think-it-through/explain`\
**HACP:** `0.4`\
**Kind:** `presentation`\
**Mode:** `render`\
**Traits:** `read-only`, `semantic`\
**Default Binding:** Current Working Object, latest substantive result, or
clearly named subject\
**Accepts:** `hacp/content`, `hacp/result`; accept `success` and `blocked`, and
defer `pending` unless the human asks to explain the proposed action\
**Produces:** `think-it-through/explanation`\
**Duration:** `once`

**Effect:** Explain the smallest unclear point at the human's requested or
apparent level while preserving the object's claims, caveats, and uncertainty.

**Limits:** Do not invent evidence, change claims, advise, choose a direction,
repeat the complete source, explain HACP automatically, or use more than one
example unless requested.

## Format

Begin the complete combo trace with `> 🎯 **<binding>** → 💡 **EXPLAIN**` when
used alone. Add `→ 💡 **EXPLAIN**` after earlier cards in a combo.

Use `Explanation` as the only required heading. Add `Example` only when one
short example removes real ambiguity.
