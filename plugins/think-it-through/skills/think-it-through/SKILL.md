---
name: think-it-through
description: Supply the shared Think It Through deck rules and mental model whenever the user invokes think-it-through, plays or combines any Think It Through card, invokes think-help, or asks to use the deck. Stay silent while a card or help utility produces the response; when invoked alone, initialize the deck on the available conversation.
---

# 🧩 Think It Through Deck

Treat this as the deck's shared skill, not as a card. Embed the minimum HACP
Draft 0.3 resolver so the deck works without the optional HACP plugin.

## Deck model

- **Context:** Use the relevant conversation and supplied checkpoints.
- **Binding:** Resolve what the combo works on: conversation, topic, axis,
  current thought, or current result.
- **Map:** Maintain `Conversation → Topics → Axes` silently when useful. Use
  short human labels. Reconstruct the map from available context.
- **Working Object:** Pass each visible result to the next card, including a
  card from another HACP deck.
- **State:** Keep the Think mental model local. Share only the Working Object,
  Binding, and active HACP controls.

## Ordered resolution

Read prose and explicit cards as one ordered stream. Position carries meaning:
a leading card acts on following material or the available object; a card after
prose consumes that prose; a card between blocks transforms the object at that
point.

Before applying an effect:

1. resolve every played card and its position;
2. validate inputs, outputs, relations, and active controls;
3. reject the full stream without effects when it is invalid;
4. never reorder cards or play a hidden card.

Think cards map to HACP roles:

```text
think-on-*              → binding
thinking moves          → operation
think-to-brief / plan   → operation:artifact
think-explain / with-*  → presentation
```

Resolve operations in written order. Pass the Working Object across deck
boundaries automatically. Binding cards set the Binding at their position. Apply
presentation cards to the current final object without changing its substance.

## Outcomes and controls

- Pass `success` and compatible `blocked` results to later cards.
- Preserve `pending` while approval is missing.
- Defer cards that need the completed pending result, then resume them after
  approval.
- Apply active controls before tools or domain effects.
- Let blocking controls win over approval controls.
- Show persistent controls on every governed response.

The deck never grants authority to mutate, browse, persist, or contact anyone.
Those actions remain governed by the user request, higher instructions, tools,
and active controls.

`think-further` extends the current object by one grounded creative leap. It
must not silently become broad ideation, a proposal, or a list of next actions.

## Duration

One-shot cards clear after one agent turn. Interview and Grill stay active
until complete, stopped, or redirected. A Binding lasts for its combo,
including a multi-exchange loop. Outputs last through their confirmation flow.

Never repeat a cleared effect from cadence. Without a played card, respond
normally and show no HACP trace.

## Display

Show one complete trace when a combo starts. Show compact continuation badges
for later Interview or Grill turns. Keep traces and active-control lines outside
artifact bodies.

Return the minimum sufficient final result. Do not print intermediate results
or explain HACP unless HACP is the subject.

When loaded with a card or `think-help`, add no trace or response of your own.

## Help

Treat `think-help` as a utility. It may explain the deck or recommend normal
conversation, one card, or a combo. It never plays a card or recommends domain
actions.

## Initialization

When invoked alone, respond only:

`> 🧩 **THINK IT THROUGH** · Deck initialized · Binding: <resolved binding> · Working Object: <available result or human message>`
