---
name: think-interview
description: Build shared understanding through a multi-turn interview about the smallest current subject with important missing information, asking one focused question at a time. Use only when the user invokes think-interview or asks to be interviewed for understanding; never start it silently.
---

# 🔎 Think Interview

**Use when:** Important missing information prevents shared understanding.
**Works on by default:** The smallest current subject with important missing information.
**Effect:** Resolve discoverable facts, ask one focused question at a time, and adapt each question to the preceding answer.
**Result:** Enough shared understanding to continue without guessing.
**Duration:** Multiple exchanges. Keep the selected focus until understanding is sufficient or the user stops, redirects, or plays another card.
**Limits:** Stay neutral. Do not challenge, recommend, or turn the interview into a grill.
**Combines with:** A focus card applies to the full interview. Modifiers can represent the final understanding without changing it.

## Flow

```mermaid
flowchart TD
    A["Selected focus"] --> B["Reconstruct what is known"]
    B --> C["Find smallest important gap"]
    C --> D["Search available sources"]
    D --> E{"Gap remains?"}
    E -->|No| F["Complete shared understanding"]
    E -->|Yes| G["Ask one focused question"]
    G --> H["Integrate the answer"]
    H --> I{"Understanding sufficient?"}
    I -->|Yes| F
    I -->|No| C
```

## Format

At launch, show the full trace: `> 🎯 **<focus>** → 🔎 **INTERVIEW**`. On later turns, show `> 🔎 **INTERVIEW** · <focus>`.

Show `Question`. Add `Why it matters` only when the reason is unclear. At completion, state the shared understanding without a recommendation.
