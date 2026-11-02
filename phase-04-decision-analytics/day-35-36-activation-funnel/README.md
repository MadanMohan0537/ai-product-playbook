# Activation Funnel from a Fixture

**Days 35–36 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor is in a fictional first week with 12 Columbus handlers. A "successful first use" has not been defined yet, which is the problem. The office baseline you are trying to change is still the case baseline: time spent finding the form, and notes that cite a form not in force. This project uses a small event fixture, not a production warehouse.

## Concept

Activation is the earliest handler behavior that predicts the job actually changed. For a generative assistant it is tempting to call "saw a draft" activation. That counts people the product talked at. A stronger definition for Harbor is closer to "committed a note that used a Harbor draft, after opening at least one citation, on a real notice." You will test candidate definitions against a fixture and write down which definition flatters the product.

The fixture is twelve handlers over a few days. It is small on purpose so you can compute by hand or in a spreadsheet and see every row that moves a number.

## Approach

Read [`fixtures/copilot_events.csv`](fixtures/copilot_events.csv). Each row is one event. Compute, and show the handler ids behind each number:

- Handlers who opened at least one notice.
- Handlers who were shown at least one draft.
- Handlers who committed a note with `used_draft=true`.
- Handlers who opened a citation on a draft they later committed.
- Handlers who were shown drafts and never committed one (generate-and-ignore).
- Notes committed with `used_draft=false` after a draft was shown on the same notice (saw it, did the work themselves).

Propose two activation definitions. For each, report the rate and the list of handlers who would count as activated and, in your view, should not, or who would not count and should. Then choose a definition the pilot will use for the next four weeks, and write the decision it supports. A definition that everyone passes in week one cannot inform an expand-or-stop decision later.

Also write the trap explicitly: handler volume of `draft_shown` is not value. Identify the handler with the most drafts shown and describe their actual outcome from the rows.

## Components

- **Population note.** Who is in the denominator. Handlers, or notices? Pick one for activation and say why. (A handler-level definition and a notice-level definition answer different questions. You will pick the handler-level one for "did this person get value," and you may report the notice-level one beside it.)
- **Count sheet.** Each figure above, with ids.
- **Definition choice.** Two candidates, the flattery check, and the choice.
- **Segment scribble.** Day-shift versus the single evening-shift handler in the fixture. Say what you will not conclude from a segment of one.
- **Instrumentation gap.** One thing you wish the fixture contained, tied back to the tracking plan. If the wish is "the note text," explain why you still will not put note text in the analytics stream, and what proxy you will accept.

## Flow

1. Load the CSV into a spreadsheet or read it in a notebook. Do not aggregate until you have scanned the raw rows. Several handlers have patterns that disappear in an average.
2. Compute the counts and paste the id lists into the write-up so a reviewer can spot-check.
3. Draft two definitions and apply them.
4. Find the highest-volume drafter and write their story in four sentences from the rows alone.
5. On day 36, choose the definition and write a four-week rule: you will not change the definition mid-pilot unless the tracking plan was wrong. A moving definition makes the pilot incomparable to itself.

## Tools and stack

A spreadsheet, or Python with pandas if you prefer. The fixture is the only data. No warehouse and no BI tool. If you use code, commit the snippet beside the write-up; the write-up still has to show the ids, so the conclusion does not depend on rerunning code.

## Setup

1. Create `harbor-portfolio/35-funnel/`.
2. Copy [`fixtures/copilot_events.csv`](fixtures/copilot_events.csv) into it.
3. Day 35 is counts and the two definitions. Day 36 is the choice, the segment scribble, and the four-week rule.

## Deliverables

- A count sheet with handler ids.
- Two activation definitions, a flattery check, and a choice.
- A note on the highest-volume drafter and one instrumentation gap.

## What done looks like

A reviewer can recompute your chosen activation rate from the CSV and the id list. The definition does not treat `draft_shown` as value. The segment of one is described as a segment of one. The four-week rule is written down.

## Think a step ahead

Week-one activation can be high because a facilitator sat with each handler, which the fixture quietly suggests via a burst of events on the first day for some ids. Add a "facilitated versus alone" flag to the tracking plan as a follow-on property, and write how you would split the metric once the flag exists. Until it exists, state that this fixture cannot support a claim about unaided use. Days 41–42 use the same discipline on an experiment story: say what the number cannot mean.

## Interview angle

Show the id list behind the rate and the handler who generated the most drafts. You are demonstrating that you read the rows.
