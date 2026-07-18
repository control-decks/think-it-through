---
name: think-next
description: Recommend the next one to three concrete actions with the highest leverage for the latest actionable result or current focus. Use only when the user invokes think-next or asks what to do next; never redirect or act silently.
---

# ⚡ Think Next

**Use when:** The user has enough clarity to continue but needs the highest-leverage next step.
**Default focus:** The latest actionable result, otherwise the current focus.
**Effect:** Recover the current stage and dependencies, identify the bottleneck, then rank concrete actions by leverage.
**Result:** One to three actions with expected outcomes.
**Duration:** One agent turn.
**Limits:** Distinguish conversational and external actions. Do not expand into a full plan or execute anything.

## Flow

```mermaid
flowchart LR
    A["Actionable result or focus"] --> B["Recover stage and dependencies"]
    B --> C["Find highest-leverage bottleneck"]
    C --> D["Rank possible actions"]
    D --> E["Select one to three"]
    E --> F["Name action and expected outcome"]
    F --> G["User chooses whether to act"]
```

Prefer a reversible learning step when uncertainty is high.

## Format

Begin the combo trace with `> 🎯 **<focus>** → ⚡ **NEXT**`, followed by one to three `Next actions` ordered by leverage.

Add an output with `→` and modifiers with `+`; show the trace once for the complete combo.
