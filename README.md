# Think It Through

**Think freely. The agent keeps the map.**

Think It Through is a lightweight conversation kit for human-led thinking with AI, designed to fit the way you already work.

Each exchange gives you new material to think with. Think It Through keeps that loop coherent and under your control.

It started with Grill Me: one short command for one precise, reusable conversation contract. Think It Through extends that principle across the whole conversation.

Start by talking. Learn the controls only when you need them.

## Why it exists

**Write the thought—not the instructions for how to discuss it.**

Complex thoughts rarely arrive in order. You branch, revise, contradict yourself, and discover late that an earlier idea mattered.

AI can respond well to each turn while losing the shape of the discussion across time. You compensate by repeating context and writing instructions about how the conversation should continue.

You keep using your product process, research method, creative practice, or personal system. Think It Through removes the need to steer the agent in prose. You use its controls to tell the agent when to clarify, connect, challenge, recover, or preserve your thinking.

The agent also returns connections and questions that can change what you think next. You keep or reshape what helps. Each response gives the agent richer working context and gives you a clearer mental model.

## Learn it in 30 seconds

### 1. Talk normally

~~~text
I think the product is really a kit, not a methodology. The commands remove
all the meta-conversation, but I also want the agent to recover ideas from much
earlier. Maybe those are two different promises?
~~~

### 2. Invoke a move when you need one

~~~text
/think-discuss
/think-recap
/think-grill
/think-propose
~~~

Natural language works too: “recap the whole conversation” or “grill this assumption.”

### 3. Add control only when useful

~~~text
/think-on-axis Positioning + /think-grill
/think-recap + /think-with-diagrams
/think-propose + /think-with-reasoning-map
/think-to-brief
~~~

The defaults cover ordinary use. `think-on-*`, `think-with-*`, and `think-to-*` are progressive controls for the moments when you want precision, representation, or a reusable artifact.

## How it works

**Your creativity leads. The agent helps you take it further.**

Your practice defines the work and its standards. Think It Through shapes how you and the agent work through it.

| Human | Kit | Agent |
| --- | --- | --- |
| Curiosity, intuition, taste, lived context | A living map and explicit controls | Working memory, structure, comparison, compression |
| Expresses, reacts, revises, and combines | Shared interaction contracts | Connections, questions, and possibilities |
| Meaning, judgment, and ownership | No hidden workflow | Support without silent direction |

~~~mermaid
flowchart LR
    P["Your practice<br/>methods · criteria · outputs"]
    H["Human<br/>expresses · reacts · chooses"]
    C["Shared conversation<br/>topics · axes · open threads"]
    A["Agent<br/>reflects · connects · questions"]
    K["Think It Through<br/>map · moves · checkpoints"]
    P -->|"defines the work"| C
    H -->|"thought"| C
    C -->|"working context"| A
    A -->|"new material"| H
    H -->|"response enriches context"| C
    H -->|"explicit steering"| K
    K -. "keeps the map coherent" .-> C
~~~

You supply the interest, the lived context, and the judgment. The agent returns material you can use: a connection between distant ideas, a sharper question, or a possibility you had not considered.

As you react, your own model becomes clearer and the agent receives richer working context for its next response. The kit preserves the accumulated shape so a new idea can build on an earlier one instead of replacing it.

This feedback loop uses only the conversation and material still available. The agent does not train on the exchange or gain memory across separate conversations.

### Activate late, keep the living map

You do not need to start a conversation with Think It Through. Invoke `/think-it-through` after the conversation becomes worth preserving:

~~~text
/think-it-through
~~~

~~~text
Think It Through active · Adopted: available conversation · Current: product positioning
~~~

The agent adopts the conversation still available, reconstructs its topics and axes, and continues from the current focus. After activation, it maintains a best-effort map during natural exchanges.

Every explicit control also reconstructs its own relevant context. It does not depend on prior activation or the latest messages alone.

~~~text
Conversation
└── Topics
    └── Axes
        ├── ideas and assumptions
        ├── proposals and decisions
        ├── tensions and contradictions
        └── open questions
~~~

- A **conversation** is the current chat plus material explicitly supplied to it.
- A **topic** is a broad subject identifiable in that conversation.
- An **axis** is a stable, human-readable branch of a topic.
- Axes may be active, paused, resolved, or superseded.

Think It Through cannot recover unavailable context or remember across separate conversations. A Thinking Brief is the portable handoff when the thinking needs to outlive the chat.

## Install and invoke

This README uses portable `/think-*` notation. The clients expose the same shared `SKILL.md` files with different prefixes:

| Portable notation | Codex | Claude Code |
| --- | --- | --- |
| `/think-recap` | `$think-it-through:think-recap` | `/think-it-through:think-recap` |

### Codex

~~~bash
codex plugin marketplace add thevzion/think-it-through
codex plugin add think-it-through@think-it-through
~~~

Example: `$think-it-through:think-recap Recover the full shape of this conversation.`

### Claude Code

~~~bash
claude plugin marketplace add thevzion/think-it-through --scope user
claude plugin install think-it-through@think-it-through --scope user
~~~

Example: `/think-it-through:think-recap Recover the full shape of this conversation.`

Explicit natural-language requests work too. The names are concise handles and shared vocabulary, not syntax you must use.

## The kit

Each family answers a different question:

| Family | Question | Examples |
| --- | --- | --- |
| `/think-*` | What conversational move should happen? | `/think-discuss`, `/think-recap` |
| `/think-on-*` | What should the control target? | `/think-on-topic`, `/think-on-axis` |
| `/think-with-*` | What representation should accompany the result? | `/think-with-diagrams`, `/think-with-reasoning-map` |
| `/think-to-*` | What reusable artifact should the thinking become? | `/think-to-brief`, `/think-to-plan` |

The composition model is:

~~~text
optional target + move or projection + optional modifier
~~~

The agent makes explicit controls visible:

~~~text
On: <target> · Move: <operation>
On: <target> · Move: <operation> · With: diagrams
On: <target> · To: brief|plan · With: reasoning-map|diagrams
~~~

Ordinary conversation remains silent. A selector invoked alone only replies `Scope set: …` and applies to the next explicit control, then expires.

### Context is not target

Every skill uses:

~~~text
Context: the full relevant conversation and explicitly supplied material.
Default target: the part the result should center on.
~~~

A selector changes the target once. It never removes evidence, history, or dependencies needed for correct reasoning.

### Session and moves

| Skill | Effect | Default target |
| --- | --- | --- |
| `/think-it-through` | Activate the protocol, adopt available history, and maintain the living map. | Current focus or supplied subject; adoption stays conversation-wide |
| `/think-distill` | Clarify the latest message, then respond or pass it to a co-invoked control. | Latest human message in context |
| `/think-discuss` | Explore and connect without forcing closure. | Thought currently being expressed |
| `/think-interview` | Run a neutral multi-turn interview, one focused question at a time, until shared understanding. | Smallest current subject with a material understanding gap |
| `/think-grill` | Walk a decision tree relentlessly, one question and recommendation at a time. | Current testable proposal, assumption, decision, design, or plan |
| `/think-recap` | Recover the map, then give a transversal digest. | Full available conversation |
| `/think-propose` | Put forward one strong direction without deciding for the human. | Current open question or decision |
| `/think-next` | Recommend the next one to three highest-leverage actions. | Latest actionable result, otherwise current focus |

`/think-interview` and `/think-grill` continue across the user's answers without reinvocation. They ask one question at a time and retain their resolved target until they finish, the user stops or redirects, or another control begins. The pipeline line appears only when the loop starts.

`/think-interview` seeks understanding without recommending a direction. `/think-grill` tests the target and provides a recommended answer with every question. Both investigate discoverable facts before asking the user.

### Target selectors

| Skill | One-shot target |
| --- | --- |
| `/think-on-conversation` | Full available conversation |
| `/think-on-topic <name>` | Named topic, otherwise clearly current topic |
| `/think-on-axis <name>` | Named axis, otherwise clearly current axis |

Selectors work in the same request or before the next explicit move, modifier, or projection. They expire after one use and never narrow the adopted history.

### Representation modifiers

| Skill | Effect | Default target |
| --- | --- | --- |
| `/think-with-diagrams` | Add the smallest useful flow, tree, timeline, matrix, table, or Mermaid diagram without changing substance. | Co-invoked result, otherwise latest substantive result or focus |
| `/think-with-reasoning-map` | Expose claims, evidence, premises, assumptions, inferences, implications, and objections without inventing logic. | Co-invoked reasoning, otherwise current proposal or decision |

Modifiers apply immediately to the co-invoked or current result. They do not create a persistent mode.

`think-with-reasoning-map` uses an argument map for argumentative claims and a broader reasoning map for decisions or systems. If there is no identifiable reasoning, it asks one focused question instead of fabricating a chain.

### Artifact projections

| Skill | Effect | Default target |
| --- | --- | --- |
| `/think-to-brief` | Project selected thinking into a neutral, reusable Thinking Brief. | Full conversation, unless an explicit co-invoked result is selected |
| `/think-to-plan` | Project an accepted or explicitly provisional direction into an Execution Plan. | Accepted or explicitly provisional executable direction |

## Composition cookbook

Use the kit at the moment a human need appears. These are recipes, not a required sequence.

| Human moment | Use | What it gives you |
| --- | --- | --- |
| This conversation became important | `/think-it-through` | Adopts available history and starts the quiet living map |
| I know what I mean, but cannot phrase it | `/think-distill` | A faithful clarification followed by a response |
| I want to keep exploring without being pushed | `/think-discuss` | Active, neutral development of the current thought |
| I lost the overall shape | `/think-recap` | Conversation-wide map, then coherent digest |
| I need to see how the parts connect | `/think-recap + /think-with-diagrams` | The same recap with the smallest useful diagram |
| The agent still does not understand enough | `/think-interview` | A neutral interview that continues one question at a time |
| This branch may be fragile | `/think-on-axis <name> + /think-grill` | A decision-tree grill with one recommendation per question |
| I need a concrete direction | `/think-propose` | One strong proposal and its decisive tradeoff |
| I need to inspect the logic | `/think-propose + /think-with-reasoning-map` | Claims, assumptions, inferences, evidence, and objections |
| I want to preserve the thinking | `/think-to-brief` | A neutral, reusable Thinking Brief |
| We made a decision; now make it executable | `/think-to-plan` | A validated Execution Plan, not implementation |

One possible map of the moments is:

~~~text
Unload → Explore → Orient → Challenge → Choose → Preserve
                                             └────→ Act
~~~

This is a map, not a workflow. Start anywhere, skip anything, loop backward, or continue talking without controls.

More useful compositions:

~~~text
/think-distill + /think-propose
/think-on-topic Product + /think-recap + /think-with-diagrams
/think-on-conversation + /think-to-brief
/think-recap + /think-to-brief
/think-grill + /think-with-reasoning-map
/think-recap + /think-with-reasoning-map
/think-on-topic v0.5 + /think-to-plan + /think-with-diagrams
~~~

## From conversation to artifact

Recap, Thinking Brief, and Execution Plan solve different problems:

| Result | Purpose | Persistence | Direction |
| --- | --- | --- | --- |
| `/think-recap` | Conversational checkpoint: `map → digest` | None | Reflects; does not add one |
| `/think-to-brief` | Neutral snapshot for reuse | Explicit artifact or inline Markdown | Preserves understanding |
| `/think-to-plan` | Operational projection of an executable direction | Native plan, inline, or approved durable destination | Organizes execution |

`/think-recap` defaults to the full conversation. Use `/think-on-topic` or `/think-on-axis` only when you intentionally want a smaller result.

`/think-to-brief` reads the selected living map directly; it does not run an invisible recap. `/think-recap + /think-to-brief` explicitly materializes that checkpoint.

A Thinking Brief follows `Conversation → Topics → Axes`, then adds purpose, audience, transversal synthesis, decisions, tensions, open questions, and a resumption point. A product spec, design document, research brief, or decision note is a contextual form of the same artifact.

Brief destination behavior follows four rules:

| Destination state | Behavior |
| --- | --- |
| No destination | Return complete portable Markdown inline immediately |
| Destination inferred | Show a materialization brief, then wait for confirmation |
| Destination explicit and direct creation requested | Create directly |
| Destination already exists | Require explicit overwrite permission |

A materialization brief shows the overview, outline, inclusions, exclusions, format, and proposed destination. Audience and contextual form are inferred unless ambiguity would materially change the result.

`/think-to-plan` uses the agent's native planning surface when available. Without an identifiable executable direction, it asks one question instead of inventing one. It preserves whether the direction is accepted or provisional, waits for validation before implementation, and persists only after approval when an explicit durable destination exists.

**A plan is never permission to execute.**

Both artifacts may include the smallest useful diagrams. Adding `/think-with-diagrams` makes the artifact diagram-led. Adding `/think-with-reasoning-map` makes its logic explicit.

## Built with itself: the conversation that designed the kit

This shortened and generalized example is adapted from the real conversation that produced Think It Through.

### Raw thought, then late activation

**Human**

> I keep feeling that generic levers could push a subject in precise directions, instead of making me rewrite what I want in prose every time. Maybe it is a method? A kit? Also, if I jump around, the agent should not forget an idea from four axes ago.

After several more messages:

~~~text
/think-it-through
~~~

**Agent**

~~~text
Think It Through active · Adopted: available conversation · Current: product model and vocabulary
~~~

Nothing had to be restarted. The earlier discussion became the adopted workspace.

### Distill and continue exploring

~~~text
/think-distill + /think-discuss
~~~

**Agent**

~~~text
On: latest human message · Move: think-distill → think-discuss

Distilled: You want the human to remain divergent while a small set of named
controls lets the agent provide convergence on demand. The product may therefore
be a conversation kit rather than a workflow or a prompt collection.

That distinction separates the product from the mechanism: the skills are tiny,
but together they establish a reusable interaction vocabulary...
~~~

**Human**

> That makes me think the map is more than memory. An agent response can trigger
> another idea, and my reaction gives the next response better context. The kit
> could make that loop steerable.

The human turned material from the agent's response into a new product direction.

### Recover the whole shape

~~~text
/think-recap + /think-with-diagrams
~~~

**Agent**

~~~text
On: conversation · Move: think-recap · With: diagrams
~~~

~~~mermaid
flowchart LR
    P["Positioning<br/>method → conversation kit"]
    M["Mental model<br/>Conversation → Topics → Axes"]
    I["Interface<br/>moves + optional controls"]
    A["Artifacts<br/>brief or execution plan"]
    P --> M
    M --> I
    I --> A
    A -. "portable context" .-> M
~~~

The recap maps every material axis first, then gives a transversal digest. Its default target is the full available conversation rather than the latest topic.

### Challenge one branch

~~~text
/think-on-axis Zero-config promise + /think-grill
~~~

**Agent**

~~~text
On: axis “Zero-config promise” · Move: think-grill

Recommendation: teach four core moves before exposing the complete palette.

Question: what can a new user accomplish before learning any family beyond the
four core moves?
~~~

**Human**

> They can discuss, recap, grill, and ask for a proposal. The other controls only
> need to appear when the reader wants more precision.

**Agent**

~~~text
Recommendation: make those four moves the first visible toolkit and introduce
targets, modifiers, and artifacts through the cookbook.

Question: does the 30-second example show a useful result from those four moves,
or does it only list their names?
~~~

The grill continues without another invocation. Its target stays narrow while evidence and dependencies from the rest of the conversation remain available.

### Choose a direction and expose its logic

~~~text
/think-propose + /think-with-reasoning-map
~~~

**Agent**

~~~text
On: open product decision · Move: think-propose · With: reasoning-map

Proposal: present Think It Through as a zero-config conversation kit, teach only
“talk, invoke a move, add optional control” before introducing the taxonomy, then
use the full example as proof after the reference.

Human thought is nonlinear
    ├── therefore activation must work late
    └── therefore recap defaults to the conversation
Named controls remove steering prose
    └── but a large palette creates learning cost
        └── therefore teach defaults first and families progressively
~~~

The proposal is strong, but the decision remains human.

### Preserve or act

~~~text
/think-to-brief
~~~

With no destination, the result is a complete portable Markdown brief inline. It preserves the conversation as reusable understanding.

~~~text
/think-to-plan
~~~

An Execution Plan needs an accepted direction or one marked provisional. Planning remains optional and never authorizes implementation.

The complete shape is:

~~~text
raw thoughts
→ late activation
→ distill and discuss
→ conversation-wide recap with diagrams
→ scoped grill
→ proposal with reasoning map
→ Thinking Brief
→ optional Execution Plan
~~~

### The same pattern in other work

**Technical architecture**

Unload competing constraints for an API and deployment model. Activate once the tradeoff becomes important. Use `/think-recap + /think-with-diagrams` to recover components and dependencies, `/think-on-axis Operations + /think-grill` to test the fragile branch, `/think-propose + /think-with-reasoning-map` to make the recommendation inspectable, then `/think-to-plan` after accepting it.

**Research or creative work**

Unload observations, fragments, counterarguments, and possible themes. Use `/think-distill` on a difficult thesis, `/think-discuss` while it is still forming, `/think-recap` to recover the cross-theme shape, and `/think-to-brief` to preserve a research brief or creative direction for the next session.

## Origin and philosophy

Grill Me supplied the seed: a short name for a precise, reusable conversation contract. It challenges one consequential branch at a time without a topic-specific mega-prompt.

Think It Through extends that idea across the life of complex thought. It adds small, composable controls to clarify, explore, understand, map, synthesize, propose, represent, preserve, and plan.

**Grill Me was the seed. Think It Through is the system around it.**

- **Human-led.** The user owns intent, direction, and final judgment.
- **Human creativity first.** The agent supplies connections and questions; the user decides what they mean and what to do with them.
- **Compounding conversation.** Each response can clarify the user's mental model and improve the working context for the next exchange.
- **Zero-config first.** Talk normally; learn controls only as needs appear.
- **Silent structure.** The map supports conversation instead of interrupting it.
- **Progressive control.** Defaults serve ordinary use; targets, modifiers, and artifacts serve precise use.
- **No hidden workflow.** A control may be suggested, but never applied silently.
- **Context-preserving.** Narrow targets do not erase relevant history or dependencies.
- **One control, one effect.** New skills earn their place through a distinct repeated outcome.
- **Stable grammar, adaptable practice.** Individuals and teams can use the kit inside their own methods and add controls without changing the compositional model.
- **Portable and lightweight.** Precise wording does the work; no runtime is required.

## Repository

~~~text
.agents/plugins/marketplace.json
.claude-plugin/marketplace.json
plugins/think-it-through/
├── .codex-plugin/plugin.json
├── .claude-plugin/plugin.json
└── skills/
    └── <control>/SKILL.md
~~~

There is one portable skill core for Codex and Claude Code. There are no per-skill metadata files, generated copies, scripts, assets, build steps, dependencies, hooks, MCP servers, or runtime.

The kit evolves through use: practice a control, tighten its contract, merge or remove overlap, and add nothing until repeated conversations reveal a distinct effect.

## License

MIT
