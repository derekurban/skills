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
