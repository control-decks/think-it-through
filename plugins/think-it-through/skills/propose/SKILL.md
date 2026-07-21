---
name: propose
description: Put forward one strong direction for the current open question or decision, with its decisive tradeoff and main risk. Use only when the user invokes propose or asks for one proposal or recommendation; never propose a new direction silently.
disable-model-invocation: true
---

# 🧭 Think Propose

**ID:** `think-it-through/propose`\
**HACP:** `0.4`\
**Kind:** `operation`\
**Mode:** `transform`\
**Traits:** `read-only`, `semantic`\
**Default Binding:** Current open question or decision\
**Accepts:** `hacp/content`, `hacp/result`\
**Requires:** `hacp/open-decision`\
**Produces:** `think-it-through/proposal`\
**Duration:** `once`

**Effect:** Evaluate viable directions, choose one, and expose why it fits,
what it gives up, and where it can fail.

**Limits:** Do not hide the decisive tradeoff, offer a soft menu, make the
human's final decision, or continue into planning.

If the user requests a lateral direction, choose one that changes the structure rather than the wording.

## Format

Begin the combo trace with `> 🎯 **<binding>** → 🧭 **PROPOSE**`, followed by `Direction`, `Why`, `Tradeoff`, `Main risk`, and `Your call`.

Add later operation cards or an output with `→` and presentation cards with `+`; show the trace once for the complete combo.
