# Skills

Reusable agent skills by Derek Urban.

## Wayfind

[Wayfind](skills/wayfind/SKILL.md) helps turn an unclear idea into a grounded direction and a useful next step. Use it when you are still discovering what you want, which approach fits, or what to try next.

The workflow is simple: **Understand → Try → Learn → Choose.** It uses investigation, examples, and experience to clarify a direction, then moves into action when there is enough evidence for the next decision.

### Install

In Codex, ask the skill installer:

```text
$skill-installer install the skill at https://github.com/derekurban/skills/tree/main/skills/wayfind
```

The skill folder contains a compact `SKILL.md`, optional references for a [worked example](skills/wayfind/references/worked-example.md) and [Designing Trials](skills/wayfind/references/designing-trials.md), and Codex metadata in `agents/openai.yaml`.

### Use

```text
Use $wayfind to help me clarify what I want and take the next useful step.
```

Wayfind supports automatic selection in Codex when the task matches its description. It has no required external service or model dependency.

### Status

Version **0.3.2**. Package structure, metadata, and document links have been checked. Earlier drafts underwent limited agent smoke tests; the current simplified wording has not yet been behaviorally retested. Feedback from real use will guide further revisions.

## Find the vibe

[Find the vibe](skills/find-the-vibe/SKILL.md) is a collaborative working session for discovering how a product should feel to use. It treats the interface as the means to an experience rather than the goal, and finds the right experience by showing you concrete artifacts and reading your reactions instead of applying a style guide or a checklist.

The division of labour is the point: you report **where** something felt wrong and **what you were trying to do**; the agent builds things worth reacting to, works out the cause by looking at the rendered moment, changes one thing, and shows it again. The shape is **name the job → state a belief → show the cheapest artifact that tests it → ask for feeling and location → translate into a cause → change one thing → repeat until the belief holds.**

### Install

In Codex, ask the skill installer:

```text
$skill-installer install the skill at https://github.com/derekurban/skills/tree/main/skills/find-the-vibe
```

In Claude Code, copy `skills/find-the-vibe` into `~/.claude/skills/`.

### Use

It is invoked only when you say the phrase **"find the vibe"**, anywhere in a message. It never triggers on inference.

```text
Let's find the vibe on the checkout.
Find the vibe: the settings page feels clunky and I can't say why.
```

### Status

Version **0.4.0**. Derived from a study of how experience decisions were actually reached across a year of agent-assisted interface work, cross-checked against published design skills and the usability literature. Not yet behaviourally tested as a packaged skill; feedback from real sessions will guide revisions.
