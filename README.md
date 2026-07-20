# Think It Through

**Stop rewriting the same instructions while thinking with AI. Play a card.**

Think It Through is an open-source deck of conversation cards for working
through ideas with an agent. Keep writing as usual, then play a card when you
want the next response to clarify, explore, question, challenge, recover, or
direct your thinking.

![Two collaborators prepare to play the Distill card against a hydra of tangled instructions](assets/think-it-through-hero.jpg)

## The interruption

I use AI before an idea is ready. My messages often end up doing two jobs at
once:

```text
The product may be a method, an interface, and a protocol. Some of those ideas
overlap, but perhaps I am forcing them together.

Separate the ideas. Clarify each one without merging them. Preserve useful
connections, and do not choose a direction yet.
```

The first paragraph carries the thought. The second tells the agent how to
respond. I kept rewriting that second paragraph as the subject changed.

`DISTILL` turns it into a card:

```text
The product may be a method, an interface, and a protocol. Some of those ideas
overlap, but perhaps I am forcing them together.

/think-distill
```

![Two collaborators face a hydra made of tangled instructions](assets/think-it-through-card-loop.gif)

The command carries the full response contract: separate the claims, clarify
them, preserve supported relationships, and return useful material for the
next exchange. Without a card, the agent gives its usual response.

## See `DISTILL` play

**Human**

```text
The product may be a method, an interface, and a protocol. Some of those ideas
overlap, but perhaps I am forcing them together.

/think-distill
```

**Agent**

> 🎯 **Latest message** → 🧪 **DISTILL**

**Distilled**

- A method is a repeatable way of working.
- An interface is how a person directs and observes the work.
- A protocol supplies rules that different implementations can follow.

**Connections**

The three ideas may describe layers of one system. The thought does not
establish that they must share one product boundary. A method can prescribe a
way of working while a protocol stays neutral about the method.

**Response**

Choose which layer people adopt first. Let the other two support it without
forcing them into the same product.

`DISTILL` separated the claims and preserved the unresolved product boundary.
The next message can continue from clearer material.

## Install and play

### Codex

```bash
codex plugin marketplace add thevzion/think-it-through
codex plugin add think-it-through@think-it-through
```

Use `$think-it-through:think-help` or play
`$think-it-through:think-distill`.

### Claude Code

```bash
claude plugin marketplace add thevzion/think-it-through --scope user
claude plugin install think-it-through@think-it-through --scope user
```

Use `/think-it-through:think-help` or play
`/think-it-through:think-distill`.

The examples below use the portable shorthand `/think-*`.

## Start with six cards

I kept reaching for the same six moves while developing ideas. Each card
captures one of them.

| When your thinking needs... | Play | The agent will... |
| --- | --- | --- |
| structure | [🧪 `DISTILL`](plugins/think-it-through/skills/think-distill/SKILL.md) | separate and clarify the thought |
| room to develop | [💬 `DISCUSS`](plugins/think-it-through/skills/think-discuss/SKILL.md) | explore without forcing a conclusion |
| missing information | [🔎 `INTERVIEW`](plugins/think-it-through/skills/think-interview/SKILL.md) | ask one focused question at a time |
| pressure | [🔥 `GRILL`](plugins/think-it-through/skills/think-grill/SKILL.md) | test one weak branch per exchange |
| orientation | [🗺️ `RECAP`](plugins/think-it-through/skills/think-recap/SKILL.md) | recover a map and synthesis |
| a direction | [🧭 `PROPOSE`](plugins/think-it-through/skills/think-propose/SKILL.md) | offer one choice with its tradeoff and risk |

Repeat a card, switch cards, or return to normal conversation as the thought
changes.

## Combine two cards

Cards pass their results from left to right:

```text
The product may be a method, an interface, and a protocol.

/think-distill
+ /think-propose
```

```text
🎯 Latest message → 🧪 DISTILL → 🧭 PROPOSE
```

The agent applies `DISTILL` first. `PROPOSE` receives the clarified result and
selects one direction, with its decisive tradeoff and main risk. You can stop
after clarification or ask for a direction in the same turn.

## Stay with a hard question

Some cards need more than one exchange:

```text
I think the interface should be the first product.

/think-grill
```

```text
🎯 Current testable idea → 🔥 GRILL

Recommendation
Treat the interface as the adoption surface, but keep the method optional.

Question
If the protocol vanished tomorrow, what value would the interface still
deliver on its own?
```

`GRILL` stays active while you answer each question. It ends with a verdict, or
when you stop or redirect it. `INTERVIEW` uses the same multi-exchange shape to
build shared understanding.

## The rules are short

- Keep writing as usual when you do not need a card.
- You play each card. The agent does not choose a move for you.
- Resolve combos from left to right against one focus.
- Clear most cards after one agent response.
- Keep `INTERVIEW` and `GRILL` active until they finish or you stop them.
- Create briefs and plans when you play their cards.

## Add control when you need it

The six core cards cover the main thinking loop. Eight more cards let you choose
the focus, recommend actions, create an artifact, or change its presentation.

`/think-help` explains the deck and gives exact commands without playing a
card:

```text
/think-help
/think-help distill
/think-help "I need to choose a direction"
```

Focus cards target a conversation, topic, or axis. Output cards create a brief
or plan. Modifiers can add a diagram or reasoning map to the same result. For
example:

```text
/think-recap + /think-with-diagrams
```

```text
🎯 Conversation → 🗺️ RECAP + 📊 DIAGRAMS
```

`/think-to-plan` turns an accepted or provisional direction into a plan for
review. It does not authorize execution.

## Under the deck

Think It Through controls the requested shape of an agent response. Your
methods, project rules, and tools still govern the substance and the available
actions.

The
[Human-Agent Card Protocol](https://github.com/thevzion/human-agent-card-protocol)
defines the shared rules beneath the deck: focus, composition, duration,
clearing, and visible resolution.

| Layer | Owns |
| --- | --- |
| Think It Through | purpose, mental model, cards, and defaults |
| HACP | card types, order, duration, and clearing |
| Methods and project rules | reasoning and quality constraints |
| Providers and tools | instruction loading, context, and actions |

<details>
<summary><strong>Complete card reference</strong></summary>

`/think-it-through` initializes the shared deck model. `/think-help` explains
the deck. Neither is a card.

### Move cards

| Card | Play when | Default focus | Result | Duration |
| --- | --- | --- | --- | --- |
| [🧪 Distill](plugins/think-it-through/skills/think-distill/SKILL.md) | Thoughts need structure | Latest human message | Clear thoughts | One agent turn |
| [💬 Discuss](plugins/think-it-through/skills/think-discuss/SKILL.md) | Exploration should stay open | Current thought | Developed thought | One agent turn |
| [🔎 Interview](plugins/think-it-through/skills/think-interview/SKILL.md) | Understanding is missing | Smallest unclear subject | Shared understanding | Multiple exchanges |
| [🔥 Grill](plugins/think-it-through/skills/think-grill/SKILL.md) | An idea needs pressure | Current testable idea | Verdict and risks | Multiple exchanges |
| [🗺️ Recap](plugins/think-it-through/skills/think-recap/SKILL.md) | Orientation is lost | Available conversation | Map and synthesis | One agent turn |
| [🧭 Propose](plugins/think-it-through/skills/think-propose/SKILL.md) | An open question needs direction | Current open decision | One proposal | One agent turn |
| [⚡ Next](plugins/think-it-through/skills/think-next/SKILL.md) | Action should follow | Latest actionable result | One to three actions | One agent turn |

### Focus cards

| Card | Chooses | Duration |
| --- | --- | --- |
| [🎯 Conversation](plugins/think-it-through/skills/think-on-conversation/SKILL.md) | All available topics and axes | One combo |
| [🎯 Topic](plugins/think-it-through/skills/think-on-topic/SKILL.md) | One topic | One combo |
| [🎯 Axis](plugins/think-it-through/skills/think-on-axis/SKILL.md) | One axis | One combo |

### Output cards

| Card | Creates | Default focus |
| --- | --- | --- |
| [📄 Brief](plugins/think-it-through/skills/think-to-brief/SKILL.md) | Portable thinking checkpoint | Available conversation |
| [📋 Plan](plugins/think-it-through/skills/think-to-plan/SKILL.md) | Execution plan for review | Accepted or provisional direction |

### Modifier cards

| Card | Adds | Default focus |
| --- | --- | --- |
| [📊 Diagrams](plugins/think-it-through/skills/think-with-diagrams/SKILL.md) | Smallest useful visual | Final or latest useful result |
| [🧠 Reasoning map](plugins/think-it-through/skills/think-with-reasoning-map/SKILL.md) | Supported reasoning structure | Final reasoning or current decision |

</details>

## Build your own card

Start with an instruction you repeat:

```text
repeated instruction
→ define one effect and default focus
→ define result, duration, and limits
→ test across subjects
→ keep, revise, merge, or remove
```

A card contract records:

```text
Use when → Default focus → Effect → Result
→ Duration → Limits → Flow → Format
```

A different deck can use the same interaction rules for another purpose and
mental model. Share an instruction you repeat in a
[GitHub issue](https://github.com/thevzion/think-it-through/issues).

## Origin and license

Grill Me was the seed: one short command for one reusable conversation
contract. Think It Through extracted more repeated instructions into cards. I
derived the HACP draft from this first implementation; one deck cannot prove a
universal standard.

Think It Through is available under the [MIT License](LICENSE).
