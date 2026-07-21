---
name: think-help
description: Explain the Think It Through deck, clarify any card or deck concept, or recommend normal conversation, one card, or a combo for the user's current situation or free-form goal. Use only when the user invokes think-help or explicitly asks how to use or continue with Think It Through. Never play a recommended card or suggest domain actions.
---

# 🧩 Think Help

Treat this as the deck's contextual help utility, never as a card.

## Resolve the request

- With no argument, inspect the current conversation and recommend zero to three useful interactions.
- With a card name or command, explain its use, default binding, effect, result, duration, limits, and one example.
- With a deck concept, explain it in plain language and tie it to a concrete command.
- With a free-form goal, recommend normal conversation, one card, or a combo.
- Use the current provider's command syntax. Fall back to portable `/think-*` notation when unknown.

Recommend `Continue normally` when no card would improve the next agent turn. Never play a card, set a Binding, change the conversation, or recommend domain actions. Leave concrete next actions to `think-next`.

## Deck guide

```text
Starter hand
think-distill · think-discuss · think-explain
think-grill · think-recap · think-propose

Operation cards
think-distill  latest human message       → clear thoughts
think-discuss  current thought            → developed thought
think-interview smallest unclear subject  → shared understanding
think-grill    current testable idea       → verdict and risks
think-recap    available conversation     → map and synthesis
think-propose  current open decision       → one direction
think-next     latest actionable result    → one to three actions
think-further  current Working Object      → one grounded creative extension

Binding cards
think-on-conversation → all available topics and axes
think-on-topic        → one named or current topic
think-on-axis         → one named or current axis

Output cards
think-to-brief → portable thinking checkpoint
think-to-plan  → execution plan for review

Presentation cards
think-explain            → concise explanation of any HACP result
think-with-diagrams      → smallest useful visual
think-with-reasoning-map → supported reasoning structure
```

Think It Through uses `Conversation → Topics → Axes` internally. A binding card selects the material for the combo. Every adjacent card receives the current HACP Working Object, including across decks; the internal mental model never crosses that boundary. Operations transform the object and presentation cards change only its visible representation. `/think-it-through` initializes the deck explicitly but is not required before a card.

## Format

For a recommendation:

```text
> 🧩 THINK HELP · <resolved request>

Recommended interaction
<normal conversation, card, or combo>

Why
<short contextual explanation>

Try
<exact command when applicable>
```

Give at most three recommendations. Omit `Try` for normal conversation.

For a card explanation, show `Card`, `Default binding`, `Effect`, `Result`, `Duration`, `Limits`, and `Example`. Keep the tone friendly, concrete, and concise.
