---
name: think-with-reasoning-map
description: Expose the reasoning structure in a result from the same combo or the current proposal or decision without inventing missing logic. Use only when the user invokes think-with-reasoning-map or asks for an argument or reasoning map; never expose one silently.
---

# 🧠 Think With Reasoning Map

**Context:** The full relevant conversation and explicitly supplied material.
**Use when:** The user needs to inspect how a claim, proposal, decision, or system holds together.
**Default target:** The final reasoning from the same combo, otherwise the current proposal or decision.
**Job:** Extract stated claims, evidence, premises, assumptions, inferences, implications, and objections, then map supported links.
**Result:** An argument map for a claim or a broader reasoning map for a decision or system.
**Runs for:** One response; does not affect later responses.
**Limits:** Mark inferred links and uncertainty. Do not add or repair evidence, causality, confidence, or reasoning. Do not challenge or decide.
**Combines with:** Apply to the final substantive result or artifact. Multiple modifiers read that same result; they do not transform one another.

## Flow

```mermaid
flowchart LR
    A["Final or latest useful reasoning"] --> B["Extract reasoning elements"]
    B --> C{"Reasoning identifiable?"}
    C -->|No| D["Ask one focused question"]
    C -->|Yes| E["Link supported elements"]
    E --> F["Mark inference and uncertainty"]
    F --> G["Preserve objections and gaps"]
    G --> H["Render reasoning map"]
```

## Format

Append `+ 🧠 **REASONING MAP**` to the complete combo trace. Used alone, begin with `> 🎯 **<target>** + 🧠 **REASONING MAP**`.

Use labels that distinguish claims, evidence, assumptions, inferences, and objections.
