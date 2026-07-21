---
name: to-plan
description: Turn an accepted or explicitly provisional executable direction into an ordered, verifiable Execution Plan using the agent's native planning surface when available. Use only when the user invokes to-plan or asks for an operational plan; never plan or execute silently.
disable-model-invocation: true
---

# 📋 Think To Plan

**ID:** `think-it-through/to-plan`\
**HACP:** `0.4`\
**Kind:** `operation`\
**Mode:** `artifact`\
**Traits:** `read-only`, `artifact`\
**Default Binding:** Current executable direction\
**Accepts:** `hacp/content`, `hacp/result`\
**Requires:** `hacp/executable-direction`, `hacp/user-accepted-or-provisional`\
**Produces:** `think-it-through/execution-plan`\
**Duration:** `until-confirmed`

**Effect:** Recover constraints, success criteria, and applicable conventions,
then produce an ordered, verifiable Execution Plan on the native planning
surface when available.

**Limits:** Keep traces and deck vocabulary outside the plan unless they are
the subject or requested. Ask once when no executable direction exists. Do not
fabricate details, treat the plan as approval, execute, save without an
approved destination, or overwrite without permission.

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

Add `→ 📋 **PLAN**` after the final move in the combo trace, or begin with `> 🎯 **<binding>** → 📋 **PLAN**` when used alone. Add presentation cards with `+`.

Before any plan content, emit the one complete combo trace. Keep it in the
conversational envelope, outside the plan, including when a native planning
surface is available. Show status while awaiting direction, validation,
destination, or overwrite permission. A plan never authorizes execution.
