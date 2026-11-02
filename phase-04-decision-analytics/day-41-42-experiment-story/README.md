# Experiment Story Memo

**Days 41–42 · Phase 4, Decision Analytics · Intermediate**

**Case.** Northline ran a four-week pilot comparison inside the Columbus office. Handlers were split by pre-assigned rotation, not by who volunteered. The treatment group used Harbor. The control group used Lumen and the shared drive, as before. You are not designing the study and you are not computing a sample size. You have been handed a result table, and your job is the decision narrative: what the company may claim, what it must not claim, and what it will do next.

## Concept

An experiment story memo translates a result table into a claim with a strength that matches the evidence, written for people who will repeat a simpler version of your sentence in a room you are not in. The risk is a true number turned into a false sentence. "Handle time fell by 3.2 minutes" can be a measured difference and still be the wrong sentence, if the citation defect moved the wrong way, if the groups were small, or if the people in the room will hear "Harbor makes claims faster" and take it to another line of business.

## Approach

Use this result table as given. Do not "fix" it. The story has to live with the awkward cells.

| Measure | Harbor (n=19 handlers) | Control (n=18 handlers) | Notes |
| --- | --- | --- | --- |
| Median handle time, new Ohio auto notice | 22.1 min | 25.4 min | Means were 24.0 and 25.6. Two Harbor handlers had medians under 12 min. |
| Citation defect in audited notes | 4 of 41 notes (9.8%) | 3 of 38 notes (7.9%) | Audit continued at the usual sample. Baseline before the pilot was 3.1% in a much larger quarter. |
| Supervisor bounce-back within 2 days | 11% of notes | 9% of notes | Bounce reasons were not coded. |
| Draft committed with a citation opened | 61% of Harbor notices | — | Control had no drafts. |
| Handler voluntary opt-out | 1 handler, week 2 | 0 | The opt-out said the draft "got in the way on glass-only claims." |

Write the memo in five parts:

1. **What we did,** in one paragraph, including who was in and the episode fence (Ohio personal auto, Columbus).
2. **What moved,** stating direction and size, with the n next to every percentage.
3. **What we will say in the staff meeting,** a single sentence you are willing to have repeated.
4. **What we will not say,** at least four sentences people will want, rewritten as refusals. Include a refusal to claim the 3.1% baseline was beaten, a refusal to claim statistical proof you were not given, and a refusal to generalize past glass-only or past Ohio.
5. **What we will do next,** one bet. The bet has to follow from the awkward cells, not from the flattering median. The higher citation defect and the glass-only opt-out are the point of the table.

You may describe the median difference as a measured difference in this pilot. You may not call it a proven causal effect, because no inferential statistic was handed to you. If a partner brings you a p-value later, the story structure stays; the claim strength can be revisited. This memo is about claim hygiene under a fixed table.

## Components

- **Result appendix.** The table, unchanged, with the date you received it ("given with the project").
- **Staff sentence.** One sentence.
- **Refusal list.** Four or more forbidden sentences, each with the cell that makes it forbidden.
- **Next bet.** One change to the pilot, with the metric that would tell you the bet worked, using a definition you already have.
- **Audience note.** What the VP version omits, and what the handler-training version adds. The numbers do not change between audiences. The advice does.

## Flow

1. Copy the table into the memo. Read it twice before you write a sentence of interpretation.
2. Draft the staff sentence. Then try to make it more exciting, and reject your own revision if the excitement is not in the table.
3. Write the refusals by imagining a launch announcement. Every adjective in that announcement is a candidate for the refusal list.
4. Choose the next bet from the defect rate or the glass-only comment, and name the metric.
5. On day 42, have someone else repeat the staff sentence from memory after one reading. If they remember a claim that is on your refusal list, the sentence is too easy to over-read and you rewrite it.

## Tools and stack

Markdown. A calculator only if you want to restate a percentage; the table already has the rates. No experimentation platform. The skill is the narrative and the refusals.

## Setup

1. Create `harbor-portfolio/41-experiment-story/memo.md`.
2. Paste the table exactly.
3. Day 41 is the five parts. Day 42 is the memory test and the rewrite.

## Deliverables

- An experiment story memo with the table, the staff sentence, the refusals, and one next bet.
- A one-paragraph note on what the memory test did to the sentence.

## What done looks like

The staff sentence can be repeated without smuggling in a proof you do not have. Every refusal points at a cell. The next bet responds to the citation defect or the glass-only opt-out, not only to the faster median. Sample sizes appear next to the claims that need them.

## Think a step ahead

The opt-out names a slice, glass-only, where the draft may be a tax. The table does not break handle time or defects out by claim subtype. Specify the next readout you would require before acting on that comment: the same measures, split by glass-only versus repairable collision, with a minimum cell size below which you will report "not split" rather than a rate. Write that minimum as a reporting rule. This is how a story memo becomes a request for the next cut, instead of a license to invent the cut from one comment.

## Interview angle

Read the staff sentence and one refusal. Offer the next bet only if they ask what you would do. The restraint is the signal.
