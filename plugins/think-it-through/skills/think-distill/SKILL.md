---
name: think-distill
description: Separate and clarify one or more fragmented, implicit, or hard-to-word thoughts, expose only supported relationships, then respond or pass the result forward. Use only when the user invokes think-distill or asks for clarification before answering; never activate it silently.
---

# 🧪 Think Distill

**Use when:** Ideas arrive faster than the user can structure them.
**Default binding:** The latest human message, interpreted in its relevant context.
**Accepts:** A compatible HACP Working Object or the declared default material.
**Effect:** Separate every material thought, clarify each one, then expose only convergence, tension, or dependency supported by the context.
**Result:** Clear thoughts that preserve the user's meaning, ambiguity, and distinctions.
**Duration:** One agent turn. Play it again on successive messages when useful.
**Limits:** Do not merge distinct thoughts, invent connections, add advice,
choose a direction, or replace clarification with another effect.

## Flow

```mermaid
flowchart LR
    A["Latest message in context"] --> B["Separate material thoughts"]
    B --> C["Clarify each thought"]
    C --> D{"Relationship supported?"}
    D -->|Yes| E["Show connection or tension"]
    D -->|No| F["Keep thoughts distinct"]
    E --> G{"Reading still ambiguous?"}
    F --> G
    G -->|Yes| H["Show readings and ask once"]
    G -->|No| I["Respond or pass result"]
```

## Format

Begin the combo trace with `> 🎯 **<binding>** → 🧪 **DISTILL**`, then use:

1. `Distilled` with one formulation or a short list.
2. `Connections` only when the context supports them.
3. `Response` when used alone, stating the remaining question or asking one
   necessary clarification.

Keep advice and direction out of `Response`. Add later operation cards with
`→`; show the trace once for the complete combo.
