---
name: think-to-brief
description: Turn the full available conversation or a result from the same combo into a neutral, reusable Thinking Brief. Use only when the user invokes think-to-brief or asks to preserve the thinking; never create or overwrite a durable artifact silently.
---

# 📄 Think To Brief

**Use when:** The user wants to preserve thinking for reuse in this session, another session, or another tool.
**Works on by default:** The full available conversation, the same focus as `/think-on-conversation` when used alone. A result supplied by a combo takes priority.
**Effect:** Use the canonical map or supplied result to verify coverage, infer a useful document form and audience, then use the subject's vocabulary and the audience's expected structure.
**Result:** A portable Markdown checkpoint that covers the relevant material, with purpose, overall synthesis, decisions, tensions, open questions, and where to resume when useful.
**Duration:** One output flow, including any required confirmation.
**Limits:** Keep the trace, HACP, cards, combos, and deck vocabulary outside the artifact body unless they are the subject or the user requests them. Do not run an implicit recap, invent conclusions, claim cross-session memory, synchronize later, or overwrite without permission.
**Combines with:** Use the final move result or the default focus. Modifiers apply to the resulting brief. Ask one clarification if another output appears in the combo. The default resolves directly; it does not play a hidden focus card.

## Flow

```mermaid
flowchart TD
    A["Final result or default focus"] --> B["Verify coverage and choose document form"]
    B --> C{"Destination?"}
    C -->|None| D["Return Markdown inline"]
    C -->|Inferred| E["Show creation preview"]
    E --> F["Wait for confirmation"]
    C -->|Explicit| G{"Already exists?"}
    G -->|No| H["Create artifact"]
    G -->|Yes| I{"Overwrite approved?"}
    I -->|Yes| H
    I -->|No| J["Wait for permission"]
```

Follow an applicable method or project convention; otherwise use portable Markdown. A creation preview states the overview, outline, inclusions, exclusions, and proposed path.

## Format

Add `→ 📄 **BRIEF**` after the final move in the combo trace, or begin with `> 🎯 **<focus>** → 📄 **BRIEF**` when used alone. Add modifiers with `+`.

Keep that trace in the conversational envelope, outside the brief. Show status only while awaiting confirmation or overwrite permission. A later session resumes only when the user supplies the brief or its content.
