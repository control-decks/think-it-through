---
name: think-propose
description: Put forward one strong direction for the current open question or decision, with its decisive tradeoff and main risk. Use only when the user invokes think-propose or asks for one proposal or recommendation; never propose a new direction silently.
---

# 🧭 Think Propose

**Use when:** Exploration has produced an open question that needs direction.
**Works on by default:** The current open question or decision.
**Effect:** Evaluate viable directions, choose one, and expose why it fits, what it gives up, and where it can fail.
**Result:** One strong proposal that the user can accept, reject, or refine.
**Duration:** One agent turn.
**Limits:** Do not hide the decisive tradeoff, offer a soft menu, make the final decision, or continue into planning.
**Combines with:** Work on a selected focus or the preceding move card's result. Pass the proposal to another move card, an output, or modifiers.

## Flow

```mermaid
flowchart LR
    A["Open question"] --> B["Recover intent and constraints"]
    B --> C["Evaluate viable directions"]
    C --> D["Choose strongest direction"]
    D --> E["Explain fit and tradeoff"]
    E --> F["Expose main risk"]
    F --> G["Return the choice to the user"]
```

If the user requests a lateral direction, choose one that changes the structure rather than the wording.

## Format

Begin the combo trace with `> 🎯 **<focus>** → 🧭 **PROPOSE**`, followed by `Direction`, `Why`, `Tradeoff`, `Main risk`, and `Your call`.

Add later move cards or an output with `→` and modifiers with `+`; show the trace once for the complete combo.
