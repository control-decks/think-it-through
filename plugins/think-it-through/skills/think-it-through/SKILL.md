---
name: think-it-through
description: Supply the shared Think It Through deck rules and mental model whenever the user invokes think-it-through, plays any Think It Through card, combines its cards, or explicitly asks to use the deck. Stay silent when resolving cards; when invoked alone, initialize the deck on the available conversation.
---

# 🧩 Think It Through Deck

Treat this as the deck's shared skill, not as a card. It embeds the Human-Agent Card Protocol rules needed to resolve the deck without a remote dependency.

## Deck model

- **Context:** Use the full relevant conversation and supplied material, including briefs or other checkpoints.
- **Focus:** Resolve what the combo works on while retaining relevant context outside it.
- **Map:** Maintain `Conversation → Topics → Axes` silently as the available context allows. Reconstruct it when needed. Use short human labels; axes may be active, paused, resolved, or replaced.
- **Method:** Follow explicit user instructions first. Let domain methods, skills, project conventions, and templates govern substance, criteria, and document structure.
- **State:** Do not claim unavailable history, hidden state, synchronization, or cross-session memory.

## HACP resolution

Use these terms consistently:

```text
human turn → user message with zero or more played cards
agent turn → one response that resolves their effects
exchange   → one human turn and its agent turn
command    → slash syntax used to play a card
card       → explicit contract with one effect
deck       → this shared skill and its 14 cards
combo      → cards resolved together
effect     → transformation or control a card applies
clear      → stop applying an effect to later turns
```

Resolve a combo in semantic order:

```text
FOCUS? → MOVE* → OUTPUT? → MODIFIER*
```

- Let one focus card choose the focus for the whole combo, then clear it.
- Run move cards from left to right and pass each result to the next.
- Let at most one output create an artifact from the final result or its own default.
- Apply all modifiers to that same final result. Change its representation without changing its substance.
- Resolve omitted information from card defaults. Defaults do not play hidden cards.
- Before applying any effect, ask one clarification when focus cards or outputs conflict.

## Duration and display

- A one-shot move lasts one agent turn.
- Interview and grill remain in play across exchanges until complete or interrupted.
- A focus card lasts one combo, including any multi-exchange loop it starts.
- An output lasts through its creation and confirmation flow.
- A modifier lasts for one final representation.
- Clearing an effect stops its behavior; it does not remove available instructions or context.
- Without a played card, respond normally. Never play a move silently.
- Show one complete trace when a combo starts. During an interview or grill, use the card's compact continuation badge on later turns. Keep natural conversation silent.
- Treat traces and HACP vocabulary as control metadata. Keep them outside artifact bodies unless Think It Through or HACP is the subject, or the user asks for them.
- When loaded with cards, add no trace or response of your own.

## Resolution flow

```mermaid
flowchart LR
    A["Deck or card invoked"] --> B["Recover context and map"]
    B --> C{"Card played?"}
    C -->|Yes| D["Resolve focus and effects"]
    C -->|No| E["Initialize deck"]
    D --> F["Return one trace and result"]
```

## Initialization format

When invoked alone, respond only:

`> 🧩 **THINK IT THROUGH** · Deck initialized · Context: available conversation · Focus: <resolved focus>`

Use `multiple active axes` for several branches of one topic and `multiple active topics` for several major subjects. Do not ask the user to choose an artificial single focus.
