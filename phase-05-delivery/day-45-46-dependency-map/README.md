# Dependency Map and Critical Path

**Days 45–46 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** The Harbor ten-week pilot depends on people who do not report to product: Lumen integration, the Ohio forms publisher, legal review of the reliance boundary, a model vendor or an internal model host, security review of logs, and handler training time on the Columbus floor. Training time is a dependency. The floor does not have a spare hour because a plan assumed it did.

## Concept

A dependency map lists the work that has to be true before a gate can be true, including work your team does not do. The critical path is the longest chain of those dependencies that still fits inside ten weeks, plus the chain that does not fit, which you then change the plan to remove. This project is a written map and a conversation plan for the two dependencies most likely to slip. It is not a scheduling product and not a Gantt as performance art.

## Approach

Build the map at the level of deliverables, not tasks. "Legal initialed reliance boundary" is a deliverable. "Schedule a meeting with legal" is a task and does not belong on the critical path until the deliverable's real wait time is the review queue, in which case the queue itself is the dependency and you write its lead time.

For each deliverable, record:

- the producing team,
- the lead time they have already told you, or "not yet asked,"
- the consuming gate from the milestone map,
- whether the dependency is hard (the gate is impossible) or soft (the gate is weaker without it),
- the fallback if it misses.

Hard dependencies for Harbor include the commit payload's author field in Lumen, the named content owner, and legal's position on what a supervisor may rely on. A model endpoint is hard for the limited pilot and soft for wizard week, which is the reason wizard week exists. If your map makes the model endpoint hard for wizard week, you have erased your own de-risking.

Find the critical path by hand. With this many nodes you can list chains in a table and sum lead times. Identify the chain that threatens week 10, and rewrite the plan so the chain no longer threatens it: reduce scope, start the wait this week, or move the gate. A map that only admires the risk is unfinished.

## Components

- **Deliverable list.** About fifteen items, with producer, lead time, gate, hard or soft, fallback.
- **Chain table.** Three or four chains with summed weeks, and a mark on the longest one that sits on the way to the limited pilot.
- **Two-conversation plan.** For the riskiest hard dependency and the one your team has been treating as soft and should not. Each conversation has an ask, a lead time you need, and the fallback you will state out loud.
- **Path change.** The edit you made to the milestone map after seeing the sum. Quote the old week and the new week.

## Flow

1. List deliverables by walking each gate and asking "what must exist that we do not build alone?"
2. Mark hard or soft. Check wizard week specifically. The model must not be hard there.
3. Sum chains. Show the arithmetic.
4. Rewrite one date or one scope item. Record the edit.
5. On day 46, draft the two conversations as scripts of less than a dozen lines each. Ask a partner to play the content owner who says their queue is six weeks. Your script has to survive that answer because the fallback was real.

## Tools and stack

Markdown. A whiteboard photo is optional. No scheduling suite. Lead times are numbers in a table, which is enough to see a ten-week collision.

## Setup

1. Create `harbor-portfolio/45-dependencies/map.md`.
2. Start from the six gates so every dependency has a consumer.
3. Day 45 is the list and the chains. Day 46 is the path change and the two scripts.

## Deliverables

- A deliverable-level dependency list with hard and soft marks.
- A chain table with arithmetic and one path change.
- Two conversation scripts that include a fallback.

## What done looks like

The longest chain is visible as a sum, and the milestone map changed because of it. Wizard week does not depend on a production model endpoint. Each risky conversation states a fallback the other team can believe, because it is something you will actually do.

## Think a step ahead

Vendor model hosts change versions on their own calendar. Add the vendor's model version as a named dependency with a lead time of "unscheduled." Write the pilot rule: a version change during the limited pilot pauses drafts and returns handlers to the control path until the offline bar is re-run on the new version. Name who is watching the version string. This is a dependency on a thing you do not control, which is the usual shape of the dependency that actually hurts.

## Interview angle

Show the chain sum and the date you moved. Then the fallback in the script. Planning is the change you made after the arithmetic.
