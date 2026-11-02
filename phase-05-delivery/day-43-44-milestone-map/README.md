# Milestone Map and RACI

**Days 43–44 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** Northline has agreed to a ten-week Harbor pilot in Columbus for new Ohio personal-auto notices. The handler signs the note. The interaction contract, metric tree, and acceptable-use page exist as drafts. Engineering has not started a production integration with Lumen. Content operations has not named an owner for bulletins. Legal has not signed the reliance boundary.

## Concept

A milestone map for an AI feature is a sequence of evidence gates, not a sequence of build percentages. "Model integration 60% complete" can be true while nobody has agreed what the handler is allowed to rely on. This project writes the gates for the ten-week pilot, the artifact that proves each gate, and a RACI that gives every gate one accountable owner. Dates are included because a gate without a week is a wish. The dates are a plan you are willing to revise when a gate fails, not a promise that the model will cooperate.

## Approach

Use six gates. You may rename them, and you may not drop the evidence each one asks for:

1. **Contract freeze.** The interaction contract's six behaviors are accepted by claims operations, with the reliance boundary initialed by legal. Proof: signed contract version.
2. **Content owner.** A named person publishes and withdraws Ohio personal-auto forms and bulletins for the pilot, on a stated cadence. Proof: owner name and the first published set's date.
3. **Wizard week.** Five handlers complete the usability tasks, including a reject-the-draft task, on the scripted interface. Proof: observation sheets and the change list.
4. **Offline eval bar.** A gold set you will define later passes a bar you write in plain language this week (for example, no unacceptable output on the coverage-decline behavior in the contract). Proof: the bar, written now, and a placeholder for the report.
5. **Shadow week.** Harbor produces drafts that are stored and not shown as the default note, or are shown to a facilitator-side reviewer only. Proof: a written rule for what shadow may not do, which includes "may not be pasted into Lumen."
6. **Limited pilot.** Forty handlers, Ohio personal auto only, with the dashboard's degraded state defined and the veto rule in force. Proof: the go document, one page, signed by the accountable owner.

RACI rows are the gates plus three cross-cutting concerns: Lumen commit payload, analytics exclusions, and handler training. Roles to include: product, claims operations, content operations, engineering, legal, security, and the Columbus manager. Exactly one A per row. If legal and product both want the A on the contract, the map has not decided.

## Components

- **Gate table.** Gate, week number, proof artifact, what "fail" means, and the only person who can waive the gate.
- **RACI.** One A per row, with R, C, and I filled for the real functions above.
- **Waiver rule.** A waiver is written, expires in one week, and cannot waive the prohibition on coverage decisions or claimant messaging. Some gates are waivable. Those two prohibitions are not gates; they are scope.
- **Slip plan.** If the content owner is unnamed by the end of week 2, what the other work is allowed to do in the meantime. The answer is not "build the integration anyway and hope."

## Flow

1. Place the six gates on a ten-week line. Leave slack between wizard week and the limited pilot. A map with no slack is a wish.
2. Write the fail condition for each gate as a concrete missing artifact.
3. Fill the RACI. Read down the A column. If one person holds every A, redistribute or acknowledge the bottleneck in writing.
4. Write the waiver rule and the week-2 slip plan.
5. On day 44, walk the map with someone playing legal and someone playing the Columbus manager. Note the first gate they each think is "just a formality." That gate needs a clearer proof, or it will be skipped.

## Tools and stack

Markdown tables. A one-page timeline in mermaid is optional. No project-management suite is required to finish the artifact. If the company lives in a tracker, the map is still the source, and tickets are copies.

## Setup

1. Create `harbor-portfolio/43-milestones/map.md`.
2. Put the ten-week boundary in the header so scope does not grow a quarter while you plan.
3. Day 43 is gates and proofs. Day 44 is RACI, waiver, slip plan, and the two-role read.

## Deliverables

- A ten-week gate map with proofs and fail conditions.
- A RACI with a single A per row.
- A waiver rule and a slip plan for a missing content owner.

## What done looks like

A program review can tell, for each week, which artifact must exist and who is accountable. The prohibitions cannot be waived. The slip plan keeps engineering from integrating a library nobody owns. Someone other than product holds at least one A.

## Think a step ahead

Shadow week is where teams quietly start showing drafts to handlers "just to learn." Add a shadow integrity check: a named reviewer compares the count of drafts produced with the count of drafts that reached a Lumen note, and any match is a failed gate, not a funny story. Write the query in words (which two counts, who runs it daily, what they do on a mismatch). This is the delivery control that makes the word "shadow" mean something.

## Interview angle

Point at the gate you will not let a senior stakeholder waive, and at the A that is not you. Delivery judgment is the boundary and the owner.
