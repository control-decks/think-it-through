---
name: think-to-plan
description: Turn an accepted or explicitly provisional executable direction into an ordered, verifiable Execution Plan using the agent's native planning surface when available. Use only when the user invokes think-to-plan or asks for an operational plan; never plan or execute silently.
---

# 📋 Think To Plan

**Context:** The full relevant conversation and explicitly supplied material.
**Use when:** An accepted or explicitly provisional direction needs operational structure.
**Default target:** The accepted or explicitly provisional executable direction.
**Job:** Recover constraints and success criteria, then produce an ordered, verifiable Execution Plan on the agent's native planning surface when available.
**Result:** A proposed plan with objective, ordered work, dependencies, risks, verification, and completion criteria.
**Runs for:** One output followed by user validation.
**Limits:** Ask once when no executable direction exists. Do not fabricate details, treat the plan as approval, execute it, save it without an approved destination, or overwrite without permission.
**Combines with:** Consume the final job result or an accepted selected direction. Modifiers apply to the resulting plan. Ask one clarification if another output appears in the combo.

## Flow

```mermaid
flowchart TD
    A["Accepted or provisional direction"] --> B{"Executable?"}
    B -->|No| C["Ask one focused question"]
    B -->|Yes| D["Recover constraints and criteria"]
    D --> E["Use native plan surface or inline plan"]
    E --> F["Build ordered, verifiable plan"]
    F --> G["Wait for user validation"]
    G --> H{"Approved destination?"}
    H -->|No| I["Keep plan unsaved"]
    H -->|Yes| J["Save without executing"]
```

State whether the source direction is accepted or provisional.

## Format

Add `→ 📋 **PLAN**` after the final job in the combo trace, or begin with `> 🎯 **<target>** → 📋 **PLAN**` when used alone. Add modifiers with `+`.

Show status while awaiting direction, validation, destination, or overwrite permission. A plan never authorizes execution.
