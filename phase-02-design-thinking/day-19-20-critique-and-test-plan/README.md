# Generative UI Critique and Test Plan

**Days 19–20 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. The on-screen proposal is a draft note with citations, sitting beside read-only claim facts from Lumen. Harbor does not decide coverage, set reserves, or message the claimant.

## Concept

Generative interfaces fail in ways ordinary forms do not. The text looks finished. The citation looks like proof even when it is the wrong paragraph. The handler can become the editor of a document they did not start, which changes where errors hide. A critique rubric for this kind of interface asks whether a skilled worker can tell what is known, what is proposed, what they can change, and how they get back to a state they trust.

This project writes that rubric, applies it to your own wizard-of-oz screen, and turns the gaps into a five-task usability plan you could run in the Columbus office without a model in the loop.

## Approach

Use six critique lenses, each scored with evidence from the screen description rather than with a vibe:

1. **Authorship.** Can the handler see that the committed note will carry their name, and what "commit" writes to Lumen?
2. **Provenance.** Can they see the document, edition, and bulletin date for each paragraph, and notice a missing one?
3. **Uncertainty.** Does the interface have a designed state for "no published source," or does empty space look like a loading spinner?
4. **Editability.** Can they change one paragraph without regenerating the rest and losing their edits?
5. **Reversibility.** Can they discard the entire draft and return to an empty note they type themselves, in one action?
6. **Pace.** Does the latency floor and the disabled-commit rule respect a 26-minute handle time, or do they stack friction that handlers will route around?

Write the usability plan around tasks, not around screens. Each task has a setup, a success condition a facilitator can observe, and a failure that would change the design. Include one task where the correct behavior is to reject the draft.

## Components

- **Rubric.** The six lenses, each with a pass question and a fail example drawn from Harbor.
- **Self-critique.** Your wizard screen scored on each lens, with the sentence in the screen description that justified the score.
- **Test plan.** Five tasks, facilitator script, what you record, and what you will not ask ("did you like it?").
- **Recruiting note.** Who in a forty-person office you want: tenure mix, including one person in their first year, and why you will not recruit only volunteers who like new tools.
- **Stop rules.** Conditions under which you halt a session, for example if a participant tries to put coverage language into the note because the draft invited it.

## Flow

1. Write the pass question for each lens before you look at your screen description, so the rubric is not a retroactive defense.
2. Score your screen. Quote yourself. Any lens you cannot score because the screen never mentioned it is an automatic gap.
3. Turn the two weakest lenses into tasks. Then add a clean success task, a bulletin-conflict task, and a reject-the-draft task, for five total.
4. Write the recruiting note and the stop rules.
5. On day 20, dry-run the facilitator script with a timer. Cut any task that needs more than eight minutes. A plan that takes an hour per handler will not survive a claims floor.

## Tools and stack

Markdown. The screen description and observation sheet from days 17–18. A stopwatch for the dry run. No usability-lab software. If you later run sessions, a shared notes doc and a clock are sufficient.

## Setup

1. Create `harbor-portfolio/19-test-plan/critique.md` and `test-plan.md`.
2. Keep the wizard screen description open while you score.
3. Day 19 is the rubric and the self-critique. Day 20 is the five tasks, recruiting, stop rules, and the timed dry run.

## Deliverables

- Critique rubric with pass questions and Harbor-specific fail examples.
- Self-critique with quotes from your own screen description.
- Five-task test plan, recruiting note, and stop rules.

## What done looks like

A researcher who has never attended your workshop can facilitate task three tomorrow. Every task has an observable success condition. The plan includes a task whose success is rejecting the draft. The rubric caught at least one gap you then wrote into the plan, so the critique changed the work.

## Think a step ahead

A five-person test on a wizard will not tell you how the interface behaves when the draft is usually right and occasionally, quietly wrong. Add a follow-on study design, one page, for a later week when a real model is in the loop: how you will salt known-bad citations at a low rate, how you will tell participants that salting happened after the session, and what consent that requires. Salting without consent is a different, unacceptable study. Write the consent sentence now.

## Interview angle

Show one lens you failed and the task you added because of it. Critique that does not change the plan is taste.
