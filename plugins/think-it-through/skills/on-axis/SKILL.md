---
name: on-axis
description: Apply an explicit command combo to a named axis or the clearly current axis. Use only when the user invokes on-axis or asks to apply commands to an axis; never change the Binding silently.
disable-model-invocation: true
---

# 🎯 Think On Axis

**ID:** `think-it-through/on-axis`\
**HACP:** `0.4`\
**Kind:** `binding`\
**Mode:** `select`\
**Traits:** `semantic`\
**Default Binding:** Named axis, otherwise unambiguous current axis\
**Accepts:** `hacp/content`, `hacp/result`\
**Produces:** `hacp/binding`\
**Duration:** `once`

**Effect:** Resolve the human label and bind the explicit combo to that axis.
A multi-exchange operation keeps the Binding until its loop completes.

**Limits:** Ask once if several axes could change the result. Do not create an
axis, play another card, or create persistent state.

## Format

When invoked alone, respond only:

`Binding set: axis "<axis>" · Applies to: next explicit combo`

In a combo, use `🎯 **Axis: <axis>**` as the first item in the trace. Ask one clarification if another binding card appears in the same combo.
