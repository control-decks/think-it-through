---
name: think-recap
description: Recover the full shape of the available conversation as a structured map with reusable topic and axis labels, followed by an overall synthesis. Use only when the user invokes think-recap or asks for a recap or synthesis; never insert an unsolicited checkpoint.
---

# 🗺️ Think Recap

**Use when:** The discussion has lost its overall shape or needs a checkpoint.
**Default focus:** The full available conversation, the same focus as `/think-on-conversation`.
**Effect:** Reconstruct topics and axes with concise human labels, reuse supported labels, classify their contents and states, then synthesize relationships across them.
**Result:** A navigable map whose topic and axis labels can be reused by focus cards, followed by a coherent account of where the thinking stands.
**Duration:** One agent turn. Play it again at useful checkpoints.
**Limits:** Preserve uncertainty and disagreement. Do not suggest another command, choose a direction, decide, plan, create technical identifiers, persist state, or create a file.

## Flow

```mermaid
flowchart LR
    A["Selected conversation context"] --> B["Recover topics and axes"]
    B --> C["Name or reuse human labels"]
    C --> D["Classify content and states"]
    D --> E["Surface tensions and dependencies"]
    E --> F["Build navigable map"]
    F --> G["Write overall synthesis"]
```

## Format

Begin the combo trace with `> 🎯 **<focus>** → 🗺️ **RECAP**`, followed by `Map` and `Digest`. Show the `Conversation → Topics → Axes` tree and the state of each axis. Give every topic and axis a concise label the user can repeat with `think-on-topic` or `think-on-axis`.

Add an output with `→` and modifiers with `+`. Do not append suggested commands.
