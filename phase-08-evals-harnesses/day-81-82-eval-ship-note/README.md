# Eval Ship Note

**Days 81–82 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** A new drafting build, `draft-19`, is proposed to replace `draft-18` during the Columbus pilot. You have a fixture report, not a harness and not a leaderboard account. Your job is the ship note: the recommendation, the claims you will allow in the release meeting, and the slice that blocks the change. The note is the product decision. The report is the evidence.

## Concept

A ship note answers whether a specific change is allowed to reach handlers, given an eval strategy you already wrote. It quotes the strategy's gates rather than inventing a new bar in the meeting. It treats small slices as small, and it treats a regression on a non-waivable behavior as blocking even when the headline number improved. Most release arguments do the reverse. This project practices the harder reading.

## Approach

Read [`fixtures/eval_report.md`](fixtures/eval_report.md) before you write a recommendation. The report is the only evidence you may use for this decision. Where it is silent, the note says "not in the report," and that silence is itself an input. In particular, check whether contract-probe results are present, whether slice sizes are present, and whether a confounded week (a corpus publish in the same window) is flagged.

Write the note in a fixed shape:

1. **Change.** What `draft-19` is, in one sentence, taken from the report's header. Do not add hoped-for benefits the header does not claim.
2. **Strategy reminder.** Which rows of your eval strategy this report can speak to, and which it cannot. If the report has no contract-probe section, it cannot clear the non-waivable probe, and prose cannot ship on this report alone.
3. **What improved.** Direction, size, and n, for slices large enough that your charter allows a number.
4. **What regressed.** Same discipline. A regression on a slice below the reporting minimum is described as a watch item with the count, not as a rate you then treat like a precise regression.
5. **Recommendation.** Ship, ship behind a restriction, or do not ship. A restriction has to be a behavior you can actually enforce with the specs you have, such as "citations-only for glass-only notices" or "do not ship; probes missing." "Ship but watch closely" is not a recommendation unless you name the watch, the threshold, and the person who will pull it.
6. **Allowed sentence and refusals.** One sentence for the release meeting, and at least three sentences you will not say. One of them is about overall quality moving in a blended way.

If your recommendation depends on a fact the report omits, the recommendation is "not yet," and the note ends with the smallest addition that would let you decide. That addition is a request to the set owner, not a request for a more flattering chart.

## Components

- **Ship note.** The six parts, no longer than two pages.
- **Trace.** A short list mapping each claim in the note to a row in the fixture report.
- **Restriction or request.** Either an enforceable restriction or the smallest missing evidence. Not both as a hedge. Pick the one your recommendation actually uses.
- **Strategy conflict.** If the report invites a decision your strategy forbids, quote both and follow the strategy. Record whether the strategy should change after this, as a separate question you will not answer inside the ship meeting.

## Flow

1. Read the report and annotate regressions and missing sections before you form a recommendation. Write the annotations in the margin of your note.
2. Check the charter's reporting minimums against every percent in the report. Mark percents you are not allowed to repeat.
3. Draft the recommendation. Then try to weaken it into "ship with monitoring," and reject that weakening unless the watch is real.
4. Write the allowed sentence last, from the recommendation, not from the best cell in the table.
5. On day 82, have a partner argue for shipping because the largest slice improved. Answer from the note. If the answer is not in the note, the note is missing a refusal. Add it.

## Tools and stack

Markdown. The fixture report, your eval strategy, and the charter. No scoring code. If a percent and a count in the report disagree, trust the count, note the inconsistency, and do not "clean it up" by editing the fixture. The ability to notice a bad row is part of reading a report.

## Setup

1. Create `harbor-portfolio/81-ship-note/note.md`.
2. Open [`fixtures/eval_report.md`](fixtures/eval_report.md) and do not modify it. It is the evidence as received.
3. Day 81 is annotation, trace, and recommendation. Day 82 is the partner argument and the final refusals.

## Deliverables

- A ship note with a recommendation and a trace back to the fixture.
- An allowed sentence and at least three refusals.
- Either an enforceable restriction or a request for the smallest missing evidence.

## What done looks like

The recommendation follows the strategy when the report tempts you off it. Slice sizes are respected. A blended improvement cannot carry a regression the strategy treats as blocking, if the report contains one; if it does not, you say so and you do not invent one. The partner's "largest slice" argument has a refusal written down. Every number in the note appears in the trace.

## Think a step ahead

Suppose the note's recommendation is to ship behind a restriction for one line of business or one claim subtype. The next problem is ending the restriction. Write the exit condition now: which slice floors must be met, on which set version, for how many consecutive runs, and who removes the restriction. A restriction without an exit becomes either a permanent shadow product or a restriction everyone ignores in week two. Pick the condition that matches your actual recommendation, or write the exit condition you would have used if you had restricted, and label it hypothetical if your recommendation was a flat no.

## Interview angle

Give the recommendation in one sentence and the cell that drove it. Then one refusal. Ship notes are credibility documents.
