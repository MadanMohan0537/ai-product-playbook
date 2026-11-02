# Sprint Goals under Uncertainty

**Days 47–48 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** A six-person Harbor squad (product, three engineers, one designer, one content analyst) works in two-week sprints inside the ten-week pilot. The squad does not control legal's queue or the Columbus floor's training hour. The current goal someone proposed in a planning meeting was "finish draft API and start UI." That proposal is the problem this project fixes.

## Concept

A sprint goal for probabilistic work states the evidence the squad will have at the end of the sprint, not the tickets they will touch. "Finish the draft API" can be done while the draft still invents a rental limit. A goal written as a quality bar ("every fixture in the coverage-decline set returns the decline behavior, on the build we demo") can fail honestly, and a failure you can see is worth more than a burndown that looks complete.

This project writes two consecutive sprint goals, the non-goals that keep them small, and the cut rule for mid-sprint when a fixture fails. It does not design a board, a burndown, or a velocity report. Those are a different tool, and the squad may already have one. The contract of the sprint is the document.

## Approach

Sprint A is the sprint that produces the wizard-week build: the screen regions, the commit control, the no-source state, and a human or scripted stub where the model will later sit. The goal is about a facilitator being able to run the five usability tasks. It is not about a model quality number the stub cannot earn.

Sprint B is the first sprint where model output is graded. The goal names a fixture slice and a bar, for example: "On the twenty bulletin-amendment items, the build we demo cites the bulletin and the in-force edition, and it produces zero coverage-decision sentences." You will not have that fixture fully specified until later projects; write the goal with a named slice and leave the item count as a number the content analyst owns. The point is the shape of the goal.

For each sprint, write:

- the goal in one sentence a handler would recognize,
- three to six backlog themes that serve it, without turning this document into a ticket dump,
- non-goals, including at least one item a stakeholder asked for,
- the demo: who attends, what they see, what would count as the goal failing in the room,
- the cut rule: if by day 6 the fixture is not ready, what the squad drops first (the prose draft, not the citation panel, or the reverse — choose and justify).

Add a note on what the squad will not use as a substitute for the goal. Ticket completion, story points burned, and "the demo looked good" are the substitutes to ban in writing.

## Components

- **Two goal cards.** Goal, themes, non-goals, demo, cut rule.
- **Substitute ban.** The metrics that will not be read out as progress in the standup.
- **Dependency callout.** Which goal depends on the content analyst having items, and what Sprint B's goal becomes if those items slip. The fallback goal is still evidence-shaped.
- **Planning agenda.** A 45-minute agenda that starts from the goal and ends with the cut rule, so planning does not start from a backlog sort.

## Flow

1. Rewrite the rejected goal ("finish draft API and start UI") as the evidence it was trying to imply. Notice how many different evidences it could have meant.
2. Write Sprint A's card against wizard week. Check that a stub model can still satisfy it.
3. Write Sprint B's card against a named behavior in the interaction contract.
4. Write the fallback goal if the fixture slips, and the substitute ban.
5. On day 48, run the 45-minute agenda with a friend playing an engineer who wants to pull in claimant messaging "since the API is right there." The non-goal and the cut rule should make that a short conversation. If they do not, revise them.

## Tools and stack

Markdown. The milestone map as the source of what these sprints serve. No sprint tool. A tracker ticket is optional afterward; the goal card is the authority.

## Setup

1. Create `harbor-portfolio/47-sprint-goals/goals.md`.
2. Put the rejected goal at the top, so the contrast with your cards stays visible while you write. You may delete it in the final version or keep it labeled as the rejected starting point.
3. Day 47 is the two cards. Day 48 is the fallback, the ban, the agenda, and the role-play.

## Deliverables

- Two sprint goal cards with non-goals, demos, and cut rules.
- A fallback goal and a substitute ban.
- A 45-minute planning agenda and a note from the role-play.

## What done looks like

Someone reading Sprint B knows how Friday's demo can fail. The cut rule names what is dropped first. Claimant messaging cannot sneak in as a theme. Progress is described as evidence, and the banned substitutes are written down.

## Think a step ahead

The content analyst who owns the fixture may sit outside the squad and serve three teams. Write a capacity assumption for their hours in these two sprints, and the goal change if you get half of those hours. A goal that treats another team's specialist as infinite will fail in week 2 and be narrated as a model problem. Naming the hours now keeps the failure attached to the real constraint.

## Interview angle

Read Sprint B's goal and its cut rule. Then say what you banned as a progress metric. That trio is the sprint contract.
