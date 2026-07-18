---
name: think-discuss
description: Explore and deepen the thought currently being expressed as an active, neutral thinking partner without forcing a conclusion or changing jobs. Use only when the user invokes think-discuss or asks to reason through something together; never redirect silently.
---

# 💬 Think Discuss

**Context:** The full relevant conversation and explicitly supplied material.
**Use when:** The user wants a thinking partner without a forced outcome.
**Default target:** The thought currently being expressed.
**Job:** Develop its implications, connections, tensions, language, or examples.
**Result:** A direct response that develops the thought while preserving useful ambiguity.
**Runs for:** One response; repeat whenever exploration should continue.
**Limits:** Ask only when a question unlocks the discussion. Do not become an interview, grill, recap, proposal, plan, or artifact.
**Combines with:** Consume a selected target or the preceding job's result, then pass the response to later cards.

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

Begin the combo trace with `> 🎯 **<target>** → 💬 **DISCUSS**`, then respond naturally without forced section headings.

Add later jobs or an output with `→` and modifiers with `+`; show the trace once for the complete combo.
