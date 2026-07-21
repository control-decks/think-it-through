---
name: with-diagrams
description: Add the smallest useful diagram to a result from the same combo or the latest useful result while preserving its substance. Use only when the user invokes with-diagrams or asks for a diagrammatic representation; never add decorative visuals silently.
disable-model-invocation: true
---

# 📊 Think With Diagrams

**ID:** `think-it-through/with-diagrams`\
**HACP:** `0.4`\
**Kind:** `presentation`\
**Mode:** `render`\
**Traits:** `read-only`, `semantic`\
**Default Binding:** Current Working Object, then latest substantive result or
Binding\
**Accepts:** `hacp/result`\
**Produces:** `hacp/presentation`\
**Duration:** `once`

**Effect:** Identify the relationship worth compressing, choose the smallest
useful form, and render it without advancing or changing the semantic object.

**Limits:** Do not decorate, duplicate prose, remove qualifications, or add
conclusions, decisions, or certainty. Say briefly when a diagram would not help.

## Flow

```mermaid
flowchart LR
    A["Final or latest useful result"] --> B["Find existing relationship"]
    B --> C{"Diagram compresses it?"}
    C -->|No| D["Keep representation minimal"]
    C -->|Yes| E["Choose smallest useful form"]
    E --> F["Render diagram"]
    F --> G["Verify substance is unchanged"]
```

## Format

Append `+ 📊 **DIAGRAMS**` to the complete combo trace. Used alone, begin with `> 🎯 **<binding>** + 📊 **DIAGRAMS**`.

Place each diagram beside the content it clarifies.
