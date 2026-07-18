---
name: think-with-diagrams
description: Add the smallest useful diagram to a result from the same combo or the latest useful result while preserving its substance. Use only when the user invokes think-with-diagrams or asks for a diagrammatic representation; never add decorative visuals silently.
---

# 📊 Think With Diagrams

**Use when:** Existing relationships would be easier to understand as a visual structure.
**Works on by default:** The final result from the same combo, otherwise the latest substantive result or focus.
**Effect:** Identify the relationship worth compressing, choose the smallest useful form, and represent it without changing the substance.
**Result:** A flow, tree, timeline, matrix, table, or Mermaid diagram tied to the existing content.
**Duration:** One final representation. It does not affect later responses.
**Limits:** Do not decorate, duplicate prose, remove qualifications, or add conclusions, decisions, or certainty. Say briefly when a diagram would not help.
**Combines with:** Apply to the final substantive result or artifact. Multiple modifiers read that same result; they do not transform one another.

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

Append `+ 📊 **DIAGRAMS**` to the complete combo trace. Used alone, begin with `> 🎯 **<focus>** + 📊 **DIAGRAMS**`.

Place each diagram beside the content it clarifies.
