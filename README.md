# Think It Through

**Think freely. The agent keeps the map.**

Think It Through is a lightweight methodology for brainstorming and working through complex subjects with an AI. You can unload ideas as they come, jump between threads, and return to earlier thoughts. The agent quietly organizes the conversation, connects what belongs together, and gives you small slash commands to explore, challenge, synthesize, propose, and act.

The human remains the author and driver. The agent acts as a working memory and cartographer: it catches, sorts, connects, compresses, and resurfaces ideas without silently taking the conversation in a new direction.

## Why it exists

Human thought is divergent. We circle back, contradict ourselves, open side paths, and discover the importance of an earlier idea much later.

AI conversations can flatten that process into the latest few messages. Early assumptions disappear, related branches drift apart, and summaries follow chronology instead of meaning.

Think It Through gives the agent a simple job:

1. Let the human think nonlinearly.
2. Maintain a coherent map of the available conversation.
3. Apply one explicit conversational move at a time.
4. Return structure when the human asks for it.

It is useful for brainstorming, product and technical design, strategy, research, writing, personal projects, and any subject that is too connected or uncertain for a single prompt.

## The map

~~~text
Conversation
└── Topics
    └── Axes
        ├── ideas and assumptions
        ├── proposals and decisions
        ├── tensions and contradictions
        └── open questions
~~~

- A **conversation** is the current chat plus any context or checkpoints explicitly provided.
- A **topic** is a broad subject being explored.
- An **axis** is a stable, human-readable branch of a topic.
- A **move** changes what the agent does next.
- A **form** changes how the result is represented.

Axes may be active, paused, resolved, or superseded. The agent maintains this structure quietly, reuses stable labels, and reconnects later insights to earlier axes when they materially affect the discussion.

Think It Through does not promise memory across separate conversations. A recap can serve as a compact checkpoint when context needs to be carried elsewhere.

## In 30 seconds

Open a complex subject and think normally:

~~~text
/think-it-through Should I turn this research workflow into a product?
/think-discuss
~~~

Focus the next move without losing the rest of the map:

~~~text
/think-on-axis Audience
/think-interview
~~~

Make the structure visible, choose a direction, and act:

~~~text
/think-on-topic Product direction + /think-recap + /think-visual
/think-propose
/think-plan
/think-next
~~~

The grammar is deliberately small:

~~~text
optional scope + move + optional form
~~~

Selectors and forms are composable. There is no required sequence or hidden workflow.

## Moves

| Move | Effect | Default scope |
| --- | --- | --- |
| `/think-it-through` | Open or resume a topic, clarify the intent, and establish its first axes. | Supplied topic, otherwise current topic |
| `/think-discuss` | Explore, connect, and deepen without forcing closure. | Current axis |
| `/think-interview` | Build shared understanding with one focused question at a time. | Current axis |
| `/think-grill` | Stress-test assumptions, evidence, tradeoffs, and failure modes. | Current axis or specific current object |
| `/think-recap` | Show the map, then produce a coherent digest. | Current topic |
| `/think-propose` | Put forward one strong direction while leaving the final decision to the human. | Current axis |
| `/think-plan` | Turn an accepted or provisional direction into an executable plan. | Current proposal or axis |
| `/think-next` | Recommend the next one to three highest-leverage actions. | Current result or axis |
| `/think-visual` | Express a result with the smallest useful visual without changing its substance. | Co-invoked result, otherwise current axis |

`/think-interview` tries to understand. `/think-grill` tries to find what does not hold. `/think-propose` can be made lateral or unconventional through the request without needing a separate wildcard move.

## Scope

| Selector | Effect |
| --- | --- |
| `/think-on-conversation` | Apply one move to the whole available conversation. |
| `/think-on-topic` | Apply one move to a named or inferred topic. |
| `/think-on-axis` | Apply one move to a named or inferred axis. |

A selector applies to a move in the same request or, when used alone, to the next explicit move. It expires after that move.

Scope narrows the output, not the reasoning. If an idea outside the selected scope materially changes the result, the agent brings that dependency back into view.

## Recap as a checkpoint

`/think-recap` is not a chronological summary. It reconstructs the selected scope from all relevant available context, then returns:

1. **The map** — topics or axes, their state, decisions, tensions, and open questions.
2. **The digest** — the coherent overall shape of the thinking and the connections that matter.

At axis scope, it shows that axis and its evolution. At topic scope, it relates the topic's axes. At conversation scope, it relates the topics and surfaces cross-topic dependencies.

This makes recap a compression checkpoint: a way to preserve the beginning and middle of a long discussion before context becomes noisy or needs to move.

## Examples

### Product and technical design

~~~text
/think-it-through Should this API be a library or a managed service?
/think-grill
/think-recap + /think-visual
/think-propose
~~~

### Strategy or a personal project

~~~text
/think-it-through How should I turn this side project into a sustainable practice?
/think-on-axis Time and energy + /think-interview
/think-recap
/think-next
~~~

### Research or creative work

~~~text
/think-it-through What is the central argument of this essay?
/think-discuss
/think-on-conversation + /think-recap
/think-propose Give me a lateral framing
~~~

## Install and invoke

The README uses canonical `/think-*` notation so the method has one portable language. Clients expose that language differently:

| Canonical move | Codex | Claude Code |
| --- | --- | --- |
| `/think-recap` | `$think-it-through:think-recap` | `/think-it-through:think-recap` |

### Codex

~~~bash
codex plugin marketplace add thevzion/think-it-through
codex plugin add think-it-through@think-it-through
~~~

For example, invoke `$think-it-through:think-grill`.

### Claude Code

~~~bash
claude plugin marketplace add thevzion/think-it-through --scope user
claude plugin install think-it-through@think-it-through --scope user
~~~

For example, invoke `/think-it-through:think-grill`.

The same `SKILL.md` files power both integrations. Provider manifests are packaging, not separate implementations.

Explicit natural-language requests work too. The slash names are the short, memorable handles and the canonical notation used throughout this README.

## Philosophy

- **Human-led.** The agent may suggest a move but never applies a directional move silently.
- **Silent structure.** The map supports the conversation instead of interrupting it.
- **Syntax-optional.** Commands are handles, not a language the human must learn.
- **One move, one effect.** Overlapping moves are merged or removed.
- **Standalone.** Every move works without first invoking `/think-it-through`.
- **No hidden workflow.** The conversation carries the state; jump directly to any move.
- **Lightweight.** Precise wording does the work. Skills stay short enough to inspect at a glance.

## Repository

~~~text
.agents/plugins/marketplace.json
.claude-plugin/marketplace.json
plugins/think-it-through/
├── .codex-plugin/plugin.json
├── .claude-plugin/plugin.json
└── skills/
    └── <move>/SKILL.md
~~~

There is no build step, generated copy, dependency, hook, MCP server, or runtime.

The method should evolve from real conversations. Tighten vague moves, remove redundant ones, and add a move only when repeated use reveals a distinct conversational effect.

## License

MIT
