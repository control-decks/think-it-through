---
name: on-conversation
description: Apply an explicit command combo to the entire available conversation. Use only when the user invokes on-conversation or asks to apply commands conversation-wide; never change the Binding silently.
disable-model-invocation: true
---

# 🎯 Think On Conversation

**ID:** `think-it-through/on-conversation`\
**HACP:** `0.4`\
**Kind:** `binding`\
**Mode:** `select`\
**Traits:** `semantic`\
**Default Binding:** Full available conversation plus supplied checkpoints\
**Accepts:** `hacp/content`, `hacp/result`\
**Produces:** `hacp/binding`\
**Duration:** `once`

**Effect:** Bind the explicit combo to every available topic and axis. A
multi-exchange operation keeps the Binding until its loop completes.

**Limits:** Change only the Binding. Do not imply unavailable history, play
another card, or create persistent state.

## Format

When invoked alone, respond only:

`Binding set: conversation · Applies to: next explicit combo`

In a combo, use `🎯 **Conversation**` as the first item in the trace. Ask one clarification if another binding card appears in the same combo.
