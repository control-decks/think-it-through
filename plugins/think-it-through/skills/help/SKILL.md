---
name: help
description: Explain the Think It Through deck, clarify any card or deck concept, or recommend normal conversation, one card, or a combo for the user's current situation or free-form goal. Use only when the user invokes help or explicitly asks how to use or continue with Think It Through. Never play a recommended card or suggest domain actions.
disable-model-invocation: true
---

# 🧩 Think Help

Treat this as the deck's contextual help utility, never as a card.

## Resolve the request

- With no argument, inspect the current conversation and recommend zero to three useful interactions.
- With a card name or command, explain its use, default binding, effect, result, duration, limits, and one example.
- With a deck concept, explain it in plain language and tie it to a concrete command.
- With a free-form goal, recommend normal conversation, one card, or a combo.
- Use the current provider's command syntax. Fall back to the portable card name when unknown.

Recommend `Continue normally` when no card would improve the next agent turn. Never play a card, set a Binding, change the conversation, or recommend domain actions. Leave concrete next actions to `next`.

## Deck guide

```text
Starter hand
distill · discuss · further
grill · recap · propose

Operation cards
distill  latest human message       → clear thoughts
discuss  current thought            → developed thought
interview smallest unclear subject  → shared understanding
grill    current testable idea       → verdict and risks
recap    available conversation     → map and synthesis
propose  current open decision       → one direction
next     latest actionable result    → one to three actions
further  current Working Object      → one grounded creative extension

Binding cards
on-conversation → all available topics and axes
on-topic        → one named or current topic
on-axis         → one named or current axis

Output cards
to-brief → portable thinking checkpoint
to-plan  → execution plan for review

Presentation cards
explain            → concise explanation of any HACP result
with-diagrams      → smallest useful visual
with-reasoning-map → supported reasoning structure
```

Think It Through uses `Conversation → Topics → Axes` only in the cards that
need that model. A binding card selects material for the combo. Adjacent cards
receive the current HACP Working Object, including across decks; the mental
model never crosses that boundary. Operations transform the object and
presentation cards render it without advancing it. A compatible HACP session
adapter must already be active; there is no deck initializer.

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
