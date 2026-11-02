# Unit Economics and Latency Budget

**Days 27–28 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor proposes one note draft per new personal-auto claim for handlers in Columbus: 40 people. A new auto claim takes about 26 minutes today, about 9 of them spent finding the form. You do not yet know how many new auto notices that office opens in a week. You will treat that volume as an assumption and show how the decision moves when the assumption moves.

## Concept

An AI feature can be loved in a pilot and unaffordable at the volume the pilot was meant to justify, or fast enough in a demo and too slow on the claims floor. Unit economics for Harbor means the cost of a successful drafted note, the latency a handler will tolerate inside a 26-minute task, and the gross margin of the pilot under assumptions you write down. The artifact is a spreadsheet a finance partner can audit, plus a one-page memo of what would change your recommendation.

## Approach

Build the model from a few drivers, all visible:

- Notices per handler per day, as a range (low, base, high).
- Drafts per notice. The base case is one. The high case includes regenerations. State the regeneration assumption explicitly, because a sloppy interface multiplies the bill.
- Input and output tokens per draft, taken from the capability card's arithmetic, with the citation text counted in the output the handler sees.
- Price per token from the public price sheet you already dated, plus a second price column for a smaller model class.
- Handler minutes returned, as an assumption, not as a fact. Use a base of 4 minutes returned of the 9 spent searching, and show a case at 1 minute and at 8.
- Loaded handler cost per minute, as an assumption you label "finance must replace." Use a placeholder and never present it as Northline's real wage.

Latency budget, separate from cost: the draft appears within 8 seconds in the base case, matching the wizard script, and you define what the product does at 20 seconds (keep the handler in the note with a visible wait, or let them start typing and reconcile later). Pick one and say what it costs in abandoned drafts.

The output is a recommendation: pilot on the smaller class, pilot on the larger class, or do not pilot until volume and minutes-returned are measured. The recommendation has to cite a cell in the sheet.

## Components

- **Driver sheet.** Every input in one column, with source or "assumption."
- **Scenario block.** Low, base, high, for weekly cost and for minutes returned.
- **Break-even note.** The minutes-returned figure at which base-case weekly cost equals assumed time saved, in the base volume. Show the formula in a sentence.
- **Latency policy.** The 8-second target, the 20-second behavior, and what you log when the wait exceeds it.
- **Decision memo.** Half a page. What you would pilot, what assumption flips the decision, and which number you will measure in week one rather than assume.

## Flow

1. List drivers before you open a spreadsheet, so the sheet cannot grow a hidden cell that the memo never mentions.
2. Implement the sheet. Color or label assumptions differently from sourced prices.
3. Compute the three scenarios and the break-even minutes.
4. Write the latency policy and check it against the 26-minute handle time. A policy that saves search and then blocks the handler on a spinner has failed even if the cents look good.
5. On day 28, change one driver at a time and write down which single change flips the recommendation. That driver is the one the pilot must measure.

## Tools and stack

A spreadsheet you can export to CSV, plus a short markdown memo. Public price pages. No cloud billing account. If you keep the sheet local, paste the assumption table into the memo so the portfolio still reads without the file.

## Setup

1. Create `harbor-portfolio/27-economics/drivers.csv` and `memo.md`.
2. Reuse token assumptions from the capability card; if you skipped it, state new assumptions here and mark them as fresh.
3. Day 27 is the driver sheet and scenarios. Day 28 is break-even, latency policy, and the flip test.

## Deliverables

- A driver sheet with sources and assumptions separated.
- Scenario costs, break-even minutes, and a latency policy.
- A decision memo that names the driver the pilot must measure.

## What done looks like

A finance partner can recompute the base case from the driver table without asking you which cell mattered. The wage figure is labeled as a placeholder. The recommendation names the assumption that would reverse it. Latency has a handler-visible behavior, not only a percentile target.

## Think a step ahead

A pilot at forty handlers can hide a distribution problem: a handful of long-tail claims pull whole forms into the prompt and dominate the bill. Add a tail policy. For example, drafts whose retrieved text exceeds a token ceiling you set fall back to "citations only, no prose," and those events are counted separately in the weekly cost. Write the ceiling, the fallback the handler sees, and how the weekly review would notice the tail eating the average. Days 39–40's dashboard is where that count should appear.

## Interview angle

Quote the break-even minutes and the driver that flips the decision. Cost conversations that include the measurement plan are the ones that hold up in a review.
