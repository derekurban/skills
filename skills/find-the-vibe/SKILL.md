---
name: find-the-vibe
description: >-
  Invoke ONLY when the user literally says "find the vibe". Never on
  inference, and never on "vibe", "vibe check" or other similar variations alone. It runs a
  collaborative session that discovers how a product should feel by showing
  the user concrete artifacts and reading their reactions.
metadata:
  version: "0.4.0"
---

# Find the vibe

## Why a session, not a spec

An interface is the *how* of an experience: the means by which someone gets something done and comes away feeling a certain way. The experience is the target; the interface is adjustable. Nobody can fully specify that target in advance, including the person asking. It shows itself when they see or use something concrete and notice how it feels.

So the session runs on a division of labour. People are reliable about **where** something felt wrong and **what they were trying to do** at that moment; they are unreliable about **why**, and so is the agent until it has looked. The user reports feeling and location. The agent builds things worth reacting to, turns the feeling into a cause by looking at the rendered moment, changes one thing, and shows it again.

A precise request with no open experiential question does not need any of this: make the change, verify it, stop. Enter the loop only where the right experience is actually unknown.

The shape: **name the job → state a belief → show the cheapest artifact that tests it → ask for feeling and location → translate into a cause → change one thing → repeat until the belief holds.**

## Setting up

### 1. Name the job

Open with one or two lines, in the user's own vocabulary, on what this screen or flow is hired to do: the functional outcome, the emotional one (calm, confident, in control, unbothered), and the moment it happens in (first run, mid-task, under time pressure, returning after a week). State it as a playback the user can correct, not a question awaiting approval. Ask only when the job or the intended outcome is genuinely missing and nothing sensible can be assumed. If the project keeps notes on earlier design decisions, read them first so settled questions stay settled.

### 2. State a belief and pick the cheapest test

Write one sentence: *we believe …, and we'll know it's right when …*. It says what the next artifact is for and gives the session a stop condition.

Then choose the lowest fidelity that can test it. Fidelity has three independent axes, interactivity, visual finish, and real content; raise only the one the belief depends on. A flow question wants a clickable wireframe with real content and no styling; a motion question wants real timing and no colour decisions. A polished page shown to test a structural belief invites feedback about the polish.

When the direction itself is open, offer a few options that differ on one named axis (layout, density, sequence, interaction model, tone) with identical content and data, so a preference is attributable. Options that differ only in surface treatment waste a round. If the user likes parts of several, combine them into a new artifact before going on.

Keep exploration disposable and away from real data and real state. Promote it into the product only when the user says so.

## The loop

### 3. Show it where it will be used

Reactions are only as good as their context. Show the artifact at real size, on the real device where possible, in the states the job passes through: first use, loading, empty, error, mid-transition, done, and both themes if the product has them. Judge motion on frames and loops, not the end state. Narrow the target: one screen or one moment looked at closely beats a whole flow glanced at. Confirm the user is seeing the current build; a stale cache or an unrefreshed page makes careful work look like ignored feedback.

### 4. Ask for feeling and location, not diagnosis

Invite the reaction in experience terms: what were you trying to do, where did it stop feeling right, what did you expect to happen. Take the words they use ("busy", "clunky", "nothing happens", "I don't trust it") as accurate reports of experience. Do not ask what is wrong with the design; that question moves them into a role where their answers get less reliable.

Pin the referent before interpreting: which element, which moment, which state. A marked-up screenshot or a pointed-at element is the most precise feedback there is; describe what you see in it before acting on it.

Keep observation and interpretation apart. "User paused at the save step and said it felt risky" is an observation; "destructive action lacks confirmation and undo" is an interpretation. Keep both, labelled.

### 5. Translate the feeling into a cause

Work from the feeling down to a mechanism, then confirm by looking at the rendered moment rather than trusting anyone's explanation. In order:

1. **Which gulf?** They did not know what to do next (unclear affordance, hidden control, too many choices, wrong sequence), or they did not know what had happened (no feedback, ambiguous state, delayed response, nothing visibly changed).
2. **Which mechanism?** Name it in plain usability language: status not visible; mismatch with how the user thinks about the task; no way back; inconsistent with the rest of the product; error not prevented; recall where recognition would do; clutter hiding the essentials; a response slower than the moment allows. This is vocabulary for naming causes, not a checklist for finding them.
3. **Which level?** A single property (too bright, too fast); a symptom with unknown cause (feels off, jumpy); the structure (crowded, can't find it, the action sits far from what it acts on); the underlying model (two settings that claim the same thing, a label promising more than the screen does, a "medium" option that looks heavier than "high", words the user wouldn't use); or the whole framing (nothing like what I meant, let's step back). Fix at the level the reaction points to; a property-level fix for a model-level complaint brings the same complaint back next round.
4. **Where in the arc?** A feeling about a whole flow usually comes from its worst moment or its ending. Find that moment before changing anything else.

Change one bounded thing per round when the cause is uncertain; batch several small, certain changes into one pass. Lock everything the user did not mention. If the same reaction returns after two rounds at one level, move up a level: loops that fail to converge are almost always adjusting properties when the problem is structure or model.

When the user proposes a solution after seeing yours, implement their semantics exactly first. Their nouns and rules carry information about the job that no artifact gave you.

### 6. Read the response from behaviour, not praise

Positive words mark direction, not completion. The reliable signals are what they do next: a specific follow-up request means the direction is accepted and the question has narrowed; "try something else here" means the belief is still open; a step back, a reset, or a change of subject means the framing was wrong, and the session returns to step 1. Whenever the framing changes, summarise what has been accepted so far so the next artifact builds on it instead of reopening it.

Every correction is evidence about the job. The fastest recovery from a miss is a plain acknowledgement and a changed approach; re-presenting the same change erodes trust. When asked to look or assess, report before fixing.

## Finishing

### 7. Verify what you claim

A claim needs evidence from the channel that can carry it: running state for behaviour, a screenshot at the right viewport, theme and state for appearance, the user's own device or data for anything that depends on them. Build and test success say nothing about feel. The agent's own review yields candidate problems; the user's observed reaction yields real ones, so their use outranks any self-audit. Say which states, devices and conditions were checked and which were not. When the user catches something missed, change the inspection method, not just the pixel.

### 8. Close

Stop when the belief from step 2 holds in the user's reaction, not when nothing is left to improve. Remove the disposable artifacts. Record the decision and the alternative it beat wherever the project keeps such notes; if it keeps none, a sentence in the commit message is enough, so that a later session with no memory of this one does not reopen it.
