---
name: think-grill
description: Stress-test a proposal, assumption, decision, design, or plan through a relentless multi-turn grill that follows its decision tree one question and recommendation at a time. Use only when the user invokes think-grill or asks for a demanding challenge; never begin silently.
---

# 🔥 Think Grill

Context: the full relevant conversation and explicitly supplied material.

**When:** A testable idea needs pressure before the user relies on it.
**On (default):** The current proposal, assumption, decision, design, or plan.
**Move:** Walk its decision tree, resolve discoverable facts, then test one unresolved branch at a time with a recommendation and demanding question.
**Result:** A target that is robust, rejected, or reduced to explicit risks.
**Cadence:** Multi-turn. Retain the target until a result or until the user stops, redirects, or invokes another card.
**Boundary:** Separate fact, inference, and unresolved claim. Do not decide for the user.
**Composition:** A selector binds the target for the full loop. A reasoning map can expose the tested logic.

## Flow

```mermaid
flowchart TD
    A["Resolved target"] --> B["Map decisions and dependencies"]
    B --> C["Search available sources"]
    C --> D["Choose weakest unresolved branch"]
    D --> E["Give recommended answer"]
    E --> F["Ask one demanding question"]
    F --> G["Integrate the answer"]
    G --> H{"Terminal result?"}
    H -->|No| D
    H -->|Yes| I["State verdict and remaining risks"]
```

## Display

Start with `> 🔥 **GRILL** · <target>`. Repeat this compact badge on every grill turn.

Show `Recommendation`, then `Question`. At completion, show `Verdict` and any remaining risks.
