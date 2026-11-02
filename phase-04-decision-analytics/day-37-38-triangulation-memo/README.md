# Qual and Quant Triangulation Memo

**Days 37–38 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor's Columbus pilot has a metric tree, a tracking plan, and a week of fixture events. You also have the two practice transcripts from days 3–4, which describe the work before Harbor existed, and you may use one additional fictional observation from the wizard test: a handler committed a draft without opening the citation because the queue on their desk was "already behind." Treat that observation as a single usability note, not as a rate.

## Concept

A triangulation memo answers one product question with two kinds of evidence, and it says where the kinds disagree. Numbers tell you how often a pattern appears in the logged population. Quotes and sessions tell you what the pattern meant to a person. Either one alone will support a confident, incomplete story. The memo is the place those stories have to sit in the same paragraph.

The question for this project: are handlers treating Harbor as a source they check, or as a text generator they paste?

## Approach

Use only evidence you can point at:

- Counts and ids from the activation fixture.
- Quotes from the transcripts (Priya's fear of a sentence that sounds like a denial; Andre's wish that the tool "just does the note" because he is measured on closures).
- The single wizard observation, labeled as one session.

Structure the memo as three claims. Each claim has a quantitative clause, a qualitative clause, and a confidence line: supported, suggested, or contradicted. A claim can be suggested by a quote and unsupported by the fixture. That is a useful result. Write it that way, and name the next evidence that would promote it.

Include one disagreement on purpose. Andre's transcript predicts paste-without-reading from handlers under a closure metric. Your fixture either contains a handler who committed `used_draft=true` with `edit_size=none` and no `citation_opened`, or it does not. Look it up. Do not write the disagreement from memory. If the fixture and Andre agree, the disagreement you write should be a different one, for example a transcript pain the events cannot see (bulletin freshness), because no event records the bulletin date the handler needed.

Close with a decision the memo can support this week, and a decision it cannot. Expanding to a second office is a decision it cannot support. Changing the commit rule, or refusing to, might be a decision it can inform, if you state the evidence limit.

## Components

- **Question.** One sentence.
- **Evidence inventory.** What you used, with paths, and what you refused to use.
- **Three claims.** Quant clause, qual clause, confidence, next evidence.
- **Disagreement paragraph.** The specific mismatch and the likely reason (different population, missing event, or a quote that was an opinion).
- **Decision box.** One action you would take in the pilot this month, and one action you would block, each tied to a claim.

## Flow

1. Write the question at the top and do not change it after you see which answer is easier.
2. Pull the ids and counts you need from the fixture. Quote Andre and Priya with transcript ids.
3. Draft claims. Force each one through the confidence line. If both clauses are thin, the confidence is "suggested" at best.
4. Write the disagreement before the decision box, so the action has already survived the mismatch.
5. On day 38, cut the memo to two pages. Anything that does not serve the question moves to an appendix or disappears.

## Tools and stack

Markdown. The fixture CSV, the transcripts, and your wizard observation note. No text-mining stack. With this much evidence, mining would be a way to avoid reading.

## Setup

1. Create `harbor-portfolio/37-triangulation/memo.md`.
2. Open the fixture and the transcripts side by side.
3. Day 37 is inventory and claims. Day 38 is the disagreement, the decision box, and the cut.

## Deliverables

- A two-page triangulation memo answering the question.
- An evidence inventory.
- A decision box with one move and one blocked move.

## What done looks like

A reader can see which claims the fixture supports and which rest on a single quote. The disagreement names a concrete row pattern or a missing event. The blocked decision is one a stakeholder might actually push, and the memo says why this evidence is the wrong size for it.

## Think a step ahead

Week-two interviews can contaminate the numbers if handlers change behavior because you sat with them. Add a short "evidence hygiene" note: interviews during the measurement window get logged against the handler id in a research log that is separate from the analytics stream, and any week that includes a facilitated session is marked before you read the funnel. This is the same facilitated-use problem as the activation follow-on, now applied to mixed-method work.

## Interview angle

Walk a hiring manager through one claim's two clauses and the decision you blocked. The block is the judgment.
