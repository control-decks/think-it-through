---
name: recap
description: Recover the full shape of the available conversation as a structured map with reusable topic and axis labels, followed by an overall synthesis. Use only when the user invokes recap or asks for a recap or synthesis; never insert an unsolicited checkpoint.
disable-model-invocation: true
---

# 🗺️ Think Recap

**ID:** `think-it-through/recap`\
**HACP:** `0.4`\
**Kind:** `operation`\
**Mode:** `transform`\
**Traits:** `read-only`, `semantic`\
**Default Binding:** Full available conversation\
**Accepts:** `hacp/content`, `hacp/result`\
**Produces:** `think-it-through/conversation-map`\
**Duration:** `once`

**Effect:** Reconstruct `Conversation → Topics → Axes` with concise reusable
human labels, classify their contents and states, then synthesize relationships
across them.

**Limits:** Preserve uncertainty and disagreement. Do not suggest another
command, choose, decide, plan, create technical identifiers, persist state, or
create a file.

## Format

Begin the combo trace with `> 🎯 **<binding>** → 🗺️ **RECAP**`, followed by `Map` and `Digest`. Show the `Conversation → Topics → Axes` tree and the state of each axis. Give every topic and axis a concise label the user can repeat with `on-topic` or `on-axis`.

Add an output with `→` and presentation cards with `+`. Do not append suggested commands.
