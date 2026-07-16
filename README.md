# Think It Through

Small conversation moves for steering big thoughts with an AI.

Think It Through is a lightweight, agent-neutral set of reusable moves. Instead of repeatedly explaining how the conversation should proceed, name the move you want: explore, interview, challenge, synthesize, decide, plan, choose the next action, or make the reasoning visual.

The human keeps the wheel. Commands are fast shortcuts, not mandatory syntax and not autonomous modes.

## Quick start

Start a topic:

~~~text
$think-it-through Should this product be a library, a method, or both?
~~~

Use <code>/think-it-through:think-it-through</code> in Claude Code. You can also speak normally:

~~~text
Think this through with me: should the method stay agent-neutral?
~~~

Then steer the conversation as it develops:

~~~text
Interview me about the audience.
Give me one wildcard on distribution.
Tie it all together.
Map the chosen direction out and draw it.
~~~

## Install

### Codex

~~~bash
codex plugin marketplace add thevzion/think-it-through
codex plugin add think-it-through@think-it-through
~~~

Invoke moves with <code>$think-it-through</code>, <code>$grill-me</code>, <code>$draw-it</code>, and the other skill names.

### Claude Code

~~~bash
claude plugin marketplace add thevzion/think-it-through --scope user
claude plugin install think-it-through@think-it-through --scope user
~~~

Claude namespaces plugin skills. Invoke moves with <code>/think-it-through:think-it-through</code>, <code>/think-it-through:grill-me</code>, <code>/think-it-through:draw-it</code>, and the other skill names.

Both plugins expose the exact same skill files. The platform manifests are packaging, not separate implementations.

## The idea

A normal conversation mixes several jobs: discovering what matters, opening possibilities, testing claims, compressing context, deciding, and turning a decision into action. Asking an agent to do all of them at once usually produces a blurry average.

Think It Through treats each change of conversational direction as a small move:

~~~text
primary move + optional target + optional form
~~~

Examples:

~~~text
grill-me on the adoption assumption
tie-it-together around the business model
map-it-out the chosen direction + draw-it
~~~

Moves are composable without becoming a workflow engine. The conversation itself carries the state.

## Vocabulary

| Term | Meaning |
| --- | --- |
| Topic | The broad subject being explored. |
| Intent | What the human wants from the conversation. |
| Angle | The current slice or perspective within the topic. |
| Move | The transformation requested for the conversation. |
| Target | The topic, angle, claim, or decision the move acts on. |
| Form | An optional representation such as a diagram or table. |

## Moves

| Move | What it does | Example |
| --- | --- | --- |
| <code>think-it-through</code> | Opens a topic and clarifies the intent and current angle. | “Think through whether this should be open source.” |
| <code>talk-it-out</code> | Explores without rushing toward closure. | “Talk out the tradeoffs with me.” |
| <code>interview-me</code> | Builds understanding with one useful question at a time. | “Interview me about who this is for.” |
| <code>grill-me</code> | Stress-tests assumptions and weak branches. | “Grill me on the distribution plan.” |
| <code>wildcard</code> | Introduces one plausible, genuinely lateral direction. | “Give me a wildcard on the business model.” |
| <code>tie-it-together</code> | Synthesizes the topic by angles, decisions, tensions, and unknowns. | “Tie together everything we established.” |
| <code>make-the-call</code> | Chooses a direction and names the decisive tradeoff. | “Make the call between a plugin and a standalone repo.” |
| <code>map-it-out</code> | Turns an accepted direction into an actionable plan. | “Map out the first public release.” |
| <code>what-next</code> | Recommends the next one to three high-leverage actions. | “What should I do next?” |
| <code>draw-it</code> | Expresses the current result with the smallest useful visual. | “Draw the relationship between topics, angles, and moves.” |

## Activation contract

Think It Through is user-led and syntax-optional:

1. A named invocation is the fastest, most precise trigger.
2. A clear natural-language request should produce the same behavior.
3. The agent may suggest a move, but must not silently apply a directional move on its own.
4. No move creates a hidden mode or state machine.

This is a v1 hypothesis, not dogma. Real conversations should decide whether the trigger descriptions are too eager, too quiet, or just right.

## Useful flows

Explore a fuzzy subject:

~~~text
think-it-through → talk-it-out → interview-me → tie-it-together
~~~

Pressure-test and decide:

~~~text
grill-me → wildcard → make-the-call
~~~

Turn clarity into action:

~~~text
tie-it-together → map-it-out → what-next
                              ↘ draw-it
~~~

These are examples, not required sequences. Jump directly to any move.

## Design principles

- One move, one distinct conversational effect.
- Keep every skill short enough to inspect at a glance.
- Make every move useful on its own.
- Prefer a precise trigger and a few strong instructions over a long prompt.
- Keep provider-specific syntax out of the skill core.
- Merge or remove overlapping moves before adding new ones.
- Add a move only after real conversations reveal a repeated need.

## Repository structure

~~~text
.agents/plugins/marketplace.json
.claude-plugin/marketplace.json
plugins/think-it-through/
├── .codex-plugin/plugin.json
├── .claude-plugin/plugin.json
└── skills/
    └── <move>/SKILL.md
~~~

There is no build step, generated copy, dependency, hook, MCP server, or runtime. Edit a skill and both integrations receive the same source.

## Evolving the method

Use the moves in real conversations. When one feels vague, tighten its outcome or boundary. When two produce the same effect, merge them. When a repeated steering request cannot be expressed as a target or form of an existing move, consider adding one.

A useful move should answer three questions in very little space:

1. What change should happen now?
2. How should the agent behave while making it?
3. What should the agent deliberately avoid?

Issues and pull requests are welcome, especially when they include the conversation pattern that motivated the change.

## License

MIT
