---
name: think-interview
description: Build shared understanding through a multi-turn interview about the smallest current subject with a material gap, asking one focused question at a time. Use only when the user invokes think-interview or asks to be interviewed for understanding; never start it silently.
---

# 🔎 Think Interview

Context: the full relevant conversation and explicitly supplied material.

**When:** A material gap prevents shared understanding.
**On:** The smallest current subject that contains that gap.
**Move:** Resolve discoverable facts, then ask one focused question at a time and adapt to each answer.
**Result:** Enough shared understanding to continue without guessing.
**Cadence:** Multi-turn. Retain the target until understanding is sufficient or the user stops, redirects, or invokes another card.
**Boundary:** Stay neutral. Do not challenge, recommend, or turn the interview into a grill.
**Composition:** A selector binds the target for the full loop. A modifier can represent the evolving understanding.

## Flow

```mermaid
flowchart TD
    A["Resolved target"] --> B["Reconstruct what is known"]
    B --> C["Find smallest material gap"]
    C --> D["Search available sources"]
    D --> E{"Gap remains?"}
    E -->|No| F["Complete shared understanding"]
    E -->|Yes| G["Ask one focused question"]
    G --> H["Integrate the answer"]
    H --> I{"Understanding sufficient?"}
    I -->|Yes| F
    I -->|No| C
```

## Display

Start with `> 🔎 **INTERVIEW** · <target>`. Repeat this compact badge on every interview turn.

Show `Question`. Add `Why it matters` only when the reason is unclear. At completion, state the shared understanding. Do not include a recommendation.
