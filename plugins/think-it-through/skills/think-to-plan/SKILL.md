---
name: think-to-plan
description: Turn an accepted or explicitly provisional executable direction into an ordered, verifiable Execution Plan using the agent's native planning surface when available. Use only when the user invokes think-to-plan or asks for an operational plan; never plan or execute silently.
---

# 📋 Think To Plan

**Use when:** An accepted or explicitly provisional direction needs operational structure.
**Works on by default:** The accepted or explicitly provisional executable direction.
**Effect:** Use the canonical map and source direction to recover constraints, success criteria, and applicable conventions, then produce an ordered, verifiable Execution Plan on the agent's native planning surface when available.
**Result:** A proposed plan with objective, ordered work, dependencies, risks, verification, and completion criteria.
**Duration:** One output flow, including user validation.
**Limits:** Keep the trace, HACP, cards, combos, and deck vocabulary outside the artifact body unless they are the subject or the user requests them. Ask once when no executable direction exists. Do not fabricate details, treat the plan as approval, execute it, save it without an approved destination, or overwrite without permission.
**Combines with:** Consume the final move result or an accepted selected direction. Modifiers apply to the resulting plan. Ask one clarification if another output appears in the combo.

## Flow

```mermaid
flowchart TD
    A["Accepted or provisional direction"] --> B{"Executable?"}
    B -->|No| C["Ask one focused question"]
    B -->|Yes| D["Recover constraints, criteria, and conventions"]
    D --> E["Use native plan surface or inline plan"]
    E --> F["Build ordered, verifiable plan"]
    F --> G["Wait for user validation"]
    G --> H{"Approved destination?"}
    H -->|No| I["Keep plan unsaved"]
    H -->|Yes| J["Save without executing"]
```

State whether the source direction is accepted or provisional.

## Format

Add `→ 📋 **PLAN**` after the final move in the combo trace, or begin with `> 🎯 **<focus>** → 📋 **PLAN**` when used alone. Add modifiers with `+`.

Keep that trace in the conversational envelope, outside the plan. Show status while awaiting direction, validation, destination, or overwrite permission. A plan never authorizes execution.
