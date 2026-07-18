---
name: think-to-brief
description: Project the full available conversation or a co-invoked result into a neutral, reusable Thinking Brief. Use only when the user invokes think-to-brief or asks to materialize the thinking; never create or overwrite a durable artifact silently.
---

# 📄 Think To Brief

Context: the full relevant conversation and explicitly supplied material.

**When:** The user wants to preserve thinking for reuse in this session, another session, or another tool.
**On:** The full available conversation, unless a combo supplies a selected result.
**Move:** Read the selected map or result directly, infer a useful document form and audience, then project it into a neutral Thinking Brief.
**Result:** Portable Markdown organized by topics and axes, with purpose, synthesis, decisions, tensions, open questions, and a resumption point.
**Cadence:** Occasional artifact projection.
**Boundary:** Do not run an implicit recap, invent missing conclusions, update the snapshot later, or overwrite a destination without permission.
**Composition:** Materialize a co-invoked recap or move result. A modifier can make the artifact diagram-led or expose its reasoning.

## Flow

```mermaid
flowchart TD
    A["Selected map or result"] --> B["Build Thinking Brief"]
    B --> C{"Destination?"}
    C -->|None| D["Return Markdown inline"]
    C -->|Inferred| E["Show materialization brief"]
    E --> F["Wait for confirmation"]
    C -->|Explicit creation| G{"Destination exists?"}
    G -->|No| H["Create artifact"]
    G -->|Yes| I{"Overwrite authorized?"}
    I -->|Yes| H
    I -->|No| J["Wait for permission"]
```

Prefer an existing project convention, otherwise portable Markdown. An inferred destination requires an overview, outline, inclusions, exclusions, and proposed path before confirmation.

## Display

Begin with `> 🎯 **<target>** → 📄 **BRIEF**`. Append `+ 📊 **DIAGRAMS**` or `+ 🧠 **REASONING MAP**` when composed.

Show status only while awaiting confirmation or overwrite permission. A selector targets the whole combo, then expires; it never narrows evidence.
