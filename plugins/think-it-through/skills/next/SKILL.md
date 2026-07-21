---
name: next
description: Recommend the next one to three concrete actions with the highest leverage for the latest actionable result or current Binding. Use only when the user invokes next or asks what to do next; never redirect or act silently.
disable-model-invocation: true
---

# ⚡ Think Next

**ID:** `think-it-through/next`\
**HACP:** `0.4`\
**Kind:** `operation`\
**Mode:** `transform`\
**Traits:** `read-only`, `semantic`\
**Default Binding:** Latest actionable result, otherwise current Binding\
**Accepts:** `hacp/content`, `hacp/result`\
**Requires:** `hacp/actionable-result`\
**Produces:** `think-it-through/next-actions`\
**Duration:** `once`

**Effect:** Recover the bound stage and dependencies, identify its bottleneck,
and rank one to three concrete actions by leverage with expected outcomes.

**Limits:** Distinguish conversational and external actions. Do not expand into
a full plan or execute anything.

## Flow

```mermaid
flowchart LR
    A["Actionable result or Binding"] --> B["Recover stage and dependencies"]
    B --> C["Find highest-leverage bottleneck"]
    C --> D["Rank possible actions"]
    D --> E["Select one to three"]
    E --> F["Name action and expected outcome"]
    F --> G["User chooses whether to act"]
```

Prefer a reversible learning step when uncertainty is high.

## Format

Begin the combo trace with `> 🎯 **<binding>** → ⚡ **NEXT**`, followed by one to three `Next actions` ordered by leverage.

Add an output with `→` and presentation cards with `+`; show the trace once for the complete combo.
