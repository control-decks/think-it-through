---
name: with-reasoning-map
description: Expose the reasoning structure in a result from the same combo or the current proposal or decision without inventing missing logic. Use only when the user invokes with-reasoning-map or asks for an argument or reasoning map; never expose one silently.
disable-model-invocation: true
---

# 🧠 Think With Reasoning Map

**ID:** `think-it-through/with-reasoning-map`\
**HACP:** `0.4`\
**Kind:** `presentation`\
**Mode:** `render`\
**Traits:** `read-only`, `semantic`\
**Default Binding:** Current Working Object, then current proposal or decision\
**Accepts:** `hacp/result`\
**Produces:** `hacp/presentation`\
**Duration:** `once`

**Effect:** Extract stated claims, evidence, premises, assumptions, inferences,
implications, and objections, then render only their supported links without
advancing the semantic object.

**Limits:** Mark inferred links and uncertainty. Do not add or repair evidence,
causality, confidence, or reasoning. Do not challenge or decide.

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

Append `+ 🧠 **REASONING MAP**` to the complete combo trace. Used alone, begin with `> 🎯 **<binding>** + 🧠 **REASONING MAP**`.

Use labels that distinguish claims, evidence, assumptions, inferences, and objections.
