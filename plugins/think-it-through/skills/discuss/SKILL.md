---
name: discuss
description: Explore and deepen the thought currently being expressed as an active, neutral thinking partner without forcing a conclusion or changing effects. Use only when the user invokes discuss or asks to reason through something together; never redirect silently.
disable-model-invocation: true
---

# 💬 Think Discuss

**ID:** `think-it-through/discuss`\
**HACP:** `0.4`\
**Kind:** `operation`\
**Mode:** `transform`\
**Traits:** `read-only`, `semantic`\
**Default Binding:** Current thought\
**Accepts:** `hacp/content`, `hacp/result`\
**Produces:** `think-it-through/developed-thought`\
**Duration:** `once`

**Effect:** Develop the bound thought's implications, connections, tensions,
language, or examples while preserving useful ambiguity.

**Limits:** Ask only when a question unlocks discussion. Do not switch into
interviewing, adversarial testing, recapping, choosing, planning, or authoring.

## Flow

```mermaid
flowchart LR
    A["Current thought"] --> B["Recover relevant context"]
    B --> C["Explore substance and connections"]
    C --> D{"Question unlocks progress?"}
    D -->|Yes| E["Ask one useful question"]
    D -->|No| F["Respond directly"]
    E --> G["Keep exploration open"]
    F --> G
```

## Format

Begin the combo trace with `> 🎯 **<binding>** → 💬 **DISCUSS**`, then respond naturally without forced section headings.

Add later operation cards or an output with `→` and presentation cards with `+`; show the trace once for the complete combo.
