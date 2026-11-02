# Problem-Solution Narrative

**Days 7–8 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. Baseline: 26 minutes average handle time on a new auto claim, about 9 minutes finding the form in force on the date of loss, 3.1% of audited notes citing a form that was not in force.

## Concept

A problem-solution narrative is the short story of a before, a change, and an after, written so a builder can see what "better" means for one episode. It is narrower than a full requirements document. It fixes the episode you intend to improve, the behavior that should be different at the end of that episode, and the behaviors you are leaving alone on purpose.

You will write the narrative for a single claim type: a new personal-auto physical-damage notice in Ohio, where the handler must cite the form in force on the date of loss and the latest bulletin that amends it. Coverage determination stays with the handler.

## Approach

Write the narrative in scenes, not in requirements identifiers. Scene one is the handler's current path, taken from the switch stories. Scene two is the same claim with Harbor in the loop, told as handler actions and system responses, still without screens. Scene three is the after: what the supervisor sees in the audit sample, and what the claimant experiences (a faster note, not a message from a model).

Hold the narrative to one episode so scope cannot leak. If a sentence would also apply to injury claims, commercial policies, or a claimant chatbot, move it to an explicit out-of-episode list.

Name the authorship rule inside the story. The note that lands in Lumen is the handler's note. Harbor may propose text. The moment of authorship is a human action with a name, such as "Add to note," and the story should say what is true of the file after that action.

## Components

- **Episode fence.** Claim type, state, what the handler is trying to produce, who signs it.
- **Before scene.** Five steps, with the failure from the case (wrong form or stale bulletin) placed where it actually happens.
- **After scene.** The same five steps, with Harbor's proposal, the citation the handler can see, and the human action that commits text.
- **Unchanged scene.** What the supervisor and the claimant still experience, so "better" is not allowed to mean "the model talks to the customer."
- **Success anecdote.** A paragraph you could read in a pilot retrospective, written in the past tense, with a number you would need to observe. Mark that number as a target, not a result.
- **Non-goals.** At least four, written as episodes you are not telling.

## Flow

1. Write the before scene from Priya's timeline. Keep the bulletin problem in the scene. A narrative that only solves PDF search has dropped half the job.
2. Write the after scene. Every system action is paired with a handler action. If the system acts twice in a row with no human, rewrite it.
3. Write the unchanged scene for the supervisor's audit and for the claimant's phone call.
4. Draft the success anecdote. Then strike any sentence you could not verify from a file, a clock, or an audit sample.
5. On day 8, read the narrative to someone who has not seen the case. Ask them what Harbor decided. If they say "coverage," the story leaked, and you revise.

## Tools and stack

Markdown. No wireframe yet. Days 17–18 are where the interaction becomes a script. Staying in prose forces you to get the responsibility right before you get the layout right.

## Setup

1. Have the switch stories or the transcripts within reach.
2. Create `harbor-portfolio/07-narrative/narrative.md` with the six component headings.
3. Day 1 of the project: before, after, unchanged. Day 2: anecdote, non-goals, and the read-aloud test.

## Deliverables

- A narrative of about 700 to 1,000 words covering one episode.
- A non-goal list of at least four neighboring episodes.
- A one-paragraph note on what the read-aloud test revealed, including what you changed.

## What done looks like

A designer and a claims supervisor can both retell the episode. The designer can see the human commit point. The supervisor can see that the audit sample still has a named author. The success anecdote contains a target and no pretended result.

## Think a step ahead

The narrative covers the happy claim, where the form and the bulletin agree once they are both on screen. The next episode is a conflict: the bulletin and the PDF disagree, and the handler has to choose. Add a six-line "conflict beat" that says what Harbor shows when two sources cannot both be cited as current, and who is allowed to resolve it. The corpus policy on days 67–68 turns that beat into a precedence rule.

## Interview angle

Walk a hiring manager through the before and after using one claim, and end on the commit point. Responsibility is the part most AI narratives skip.
