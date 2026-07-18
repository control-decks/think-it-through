---
name: think-discuss
description: Explore and deepen the thought currently being expressed as an active, neutral thinking partner without forcing a conclusion or changing effects. Use only when the user invokes think-discuss or asks to reason through something together; never redirect silently.
---

# 💬 Think Discuss

**Use when:** The user wants a thinking partner without a forced outcome.
**Works on by default:** The thought currently being expressed.
**Effect:** Develop its implications, connections, tensions, language, or examples.
**Result:** A direct response that develops the thought while preserving useful ambiguity.
**Duration:** One agent turn. Play it again whenever exploration should continue.
**Limits:** Ask only when a question unlocks the discussion. Do not become an interview, grill, recap, proposal, plan, or artifact.
**Combines with:** Work on a selected focus or the preceding move card's result, then pass the response to later cards.

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

Begin the combo trace with `> 🎯 **<focus>** → 💬 **DISCUSS**`, then respond naturally without forced section headings.

Add later move cards or an output with `→` and modifiers with `+`; show the trace once for the complete combo.
