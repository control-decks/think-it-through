---
name: think-grill
description: Stress-test a proposal, assumption, decision, design, or plan through a relentless multi-turn grill that follows its decision tree one question and recommendation at a time. Use only when the user invokes think-grill or asks for a demanding challenge; never begin silently.
---

# 🔥 Think Grill

**Context:** The full relevant conversation and explicitly supplied material.
**Use when:** A testable idea needs pressure before the user relies on it.
**Default target:** The current proposal, assumption, decision, design, or plan.
**Job:** Walk its decision tree, resolve discoverable facts, then test one unresolved branch at a time with a recommendation and demanding question.
**Result:** A target that is robust, rejected, or reduced to explicit risks.
**Runs for:** Multiple turns. Keep the selected target until a result is reached or the user stops, redirects, or invokes another command.
**Limits:** Separate fact, inference, and unresolved claim. Do not decide for the user or ask for information that can be found from available sources.
**Combines with:** A selector applies the target for the full grill. A reasoning map can expose the final tested logic without repairing it.

## Flow

```mermaid
flowchart TD
    A["Selected target"] --> B["Map decisions and dependencies"]
    B --> C["Search available sources"]
    C --> D["Choose weakest unresolved branch"]
    D --> E["Give recommended answer"]
    E --> F["Ask one demanding question"]
    F --> G["Integrate the answer"]
    G --> H{"Terminal result?"}
    H -->|No| D
    H -->|Yes| I["State verdict and remaining risks"]
```

## Format

At launch, show the full trace: `> 🎯 **<target>** → 🔥 **GRILL**`. On later turns, show `> 🔥 **GRILL** · <target>`.

Show `Recommendation`, then `Question`. At completion, show `Verdict` and any remaining risks.
