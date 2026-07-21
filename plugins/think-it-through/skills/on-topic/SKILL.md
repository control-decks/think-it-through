---
name: on-topic
description: Apply an explicit command combo to a named topic or the clearly current topic. Use only when the user invokes on-topic or asks to apply commands to a topic; never change the Binding silently.
disable-model-invocation: true
---

# 🎯 Think On Topic

**ID:** `think-it-through/on-topic`\
**HACP:** `0.4`\
**Kind:** `binding`\
**Mode:** `select`\
**Traits:** `semantic`\
**Default Binding:** Named topic, otherwise unambiguous current topic\
**Accepts:** `hacp/content`, `hacp/result`\
**Produces:** `hacp/binding`\
**Duration:** `once`

**Effect:** Resolve the human label and bind the explicit combo to that topic
and its relevant axes. A multi-exchange operation keeps the Binding until its
loop completes.

**Limits:** Ask once if several topics could change the result. Do not play
another card or create persistent state.

## Format

When invoked alone, respond only:

`Binding set: topic "<topic>" · Applies to: next explicit combo`

In a combo, use `🎯 **Topic: <topic>**` as the first item in the trace. Ask one clarification if another binding card appears in the same combo.
