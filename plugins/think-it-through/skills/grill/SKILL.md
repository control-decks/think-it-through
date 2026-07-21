---
name: grill
description: Stress-test a proposal, assumption, decision, design, or plan through a relentless multi-turn grill that follows its decision tree one question and recommendation at a time. Use only when the user invokes grill or asks for a demanding challenge; never begin silently.
disable-model-invocation: true
---

# 🔥 Think Grill

**ID:** `think-it-through/grill`\
**HACP:** `0.4`\
**Kind:** `operation`\
**Mode:** `transform`\
**Traits:** `read-only`, `semantic`, `multi-exchange`\
**Default Binding:** Current proposal, assumption, decision, design, or plan\
**Accepts:** `hacp/content`, `hacp/result`\
**Requires:** `hacp/testable-object`\
**Produces:** `think-it-through/verdict`\
**Duration:** `until-complete`

**Effect:** Walk the bound object's decision tree, resolve discoverable facts,
then test one unresolved branch at a time with a recommendation and demanding
question.

**Limits:** Keep the selected Binding until verdict, stop, or redirection.
Separate fact, inference, and unresolved claim. Do not decide for the human or
ask for information available from sources you can inspect.

## Flow

```mermaid
flowchart TD
    A["Selected Binding"] --> B["Map decisions and dependencies"]
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

At launch, show the full trace: `> 🎯 **<binding>** → 🔥 **GRILL**`. On later turns, show `> 🔥 **GRILL** · <binding>`.

Show `Recommendation`, then `Question`. At completion, show `Verdict` and any remaining risks.
