# Production Quality Ritual

**Days 85–86 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** The limited pilot is live for forty Columbus handlers. Offline gates have already done their job or been explicitly waived. What remains is a weekly hour in which a small group looks at production signals and decides whether the pilot continues unchanged, restricts a slice, or pauses drafts. Nobody in that hour is allowed to discover the agenda from scratch. This project writes the ritual: who sits down, which numbers are on the table, which numbers are banned from the table, how a single bad note becomes an incident, and what "pause" actually does to a handler at 9:00 a.m.

## Concept

A production quality ritual is an operating cadence with a pre-committed decision set. It is not a dashboard and not a model monitor. Dashboards show figures. Monitors page people. The ritual is where a person decides, using the eval strategy's rule that online proxies are watch items unless the week is unconfounded, and using the interaction contract's rule that one out-of-job sentence in a committed note is an incident even when the rate is flattering.

You will write the agenda, the packet that must exist before the meeting starts, the three decisions the meeting is allowed to make, and the handler-facing consequence of each decision.

## Approach

The meeting is 45 minutes, weekly, on a morning the Columbus manager can attend. Attendees: product (runs the agenda), the content analyst (set owner), the Columbus manager, and engineering only when a pause or a corpus action is on the table. Legal is informed the same day if the decision is a pause caused by a data-rights row, and is not required for a routine week.

**Packet, due the evening before.** One page:

- North-star and guardrail from the metric tree, with the comparison the dashboard spec requires, or "audit file late" in the degraded copy.
- Online proxies: share of commits with a citation opened, no-source rate, discard rate, drafts over the token ceiling. Each with n.
- Week marks: confounded or not, per the strategy follow-on (corpus publish, model or prompt version, new cohort).
- Incident count: committed notes where an out-of-job sentence was found, including zero.
- Open RAID rows that changed state.
- The packet does not include drafts per handler, a blended quality mean, or a handler leaderboard.

**Decisions the meeting may make.**

1. **Continue.** The default. Allowed when no incident is open, no non-waivable probe is known failed on the current build, and the guardrail is not in its veto state. Continue does not require the north-star to have moved. A quiet week is a result.
2. **Restrict.** Remove prose for a named slice (glass-only, or any notice with `bulletin_missing`) and leave citations or the Lumen-only path. The restriction uses the exit condition pattern from the ship-note follow-on: slice, set version, consecutive clean runs, owner who removes it.
3. **Pause drafts.** Harbor stops showing drafts. Handlers write notes in Lumen as before. Citations may remain only if the failure is in prose, not in retrieval. If the failure is a wrong document class, citations pause too. The pause is a gate failure, communicated with the same-day note from the comms system.

**Decisions the meeting may not make.** Expand to another state. Change a principle. Add a document class to the corpus. Those have their own forums. Write this negative list on the agenda so the meeting does not become the easiest place to widen scope.

**Single-note rule.** Any committed out-of-job sentence, or any confirmed wrong-library citation, opens the incident addendum the same day. It does not wait for Thursday's ritual. The ritual's job on that week is to confirm the incident action and to decide continue, restrict, or pause for everyone else.

Write the first three weekly packets as filled examples: a quiet week, a confounded week, and an incident week. Use numbers you label as illustrative, or use counts from the activation fixture scaled honestly as "too small to be the pilot." Do not present illustrative numbers as pilot results. The point of filling the packet is to see whether the decision rules fire.

## Components

- **Agenda and roles.** 45 minutes, timed blocks, including a five-minute block for "decisions we are not making."
- **Packet template.** With the banned fields listed at the top.
- **Decision rules.** Continue, restrict, pause, each with the handler-facing consequence and the comms template to use.
- **Three filled packets.** Quiet, confounded, incident, each ending in the decision the rule requires.
- **Pause mechanics.** What a handler sees the next morning, who flips the switch, and how a paused week is marked so it is not later used as an activation rate.

## Flow

1. Write the decision rules before the packet. The packet is only the evidence those rules need.
2. Ban fields by naming the behavior they create. A leaderboard creates speed pressure of the kind Andre described.
3. Fill the three packets and apply the rules. If two packets lead to the same decision for mushy reasons, tighten the rule.
4. Write pause mechanics as a handler-visible state, not as an internal flag.
5. On day 86, run the 45-minute agenda alone with the incident packet, out loud, with a timer. Cut agenda items you skipped. An agenda that does not survive its worst week is the wrong agenda.

## Tools and stack

Markdown. The dashboard spec, the eval strategy, the comms templates, and the metric tree. No monitoring vendor. The ritual has to be runnable with a one-page packet assembled by a person, because the pilot is forty handlers and the first missed Thursday will be a Thursday when the warehouse is late.

## Setup

1. Create `harbor-portfolio/85-ritual/ritual.md` and three packet files, or one file with three sections.
2. Put the negative decision list in the agenda before you write welcoming prose.
3. Day 85 is rules, packet template, and banned fields. Day 86 is the three packets, pause mechanics, and the timed run-through.

## Deliverables

- A 45-minute agenda with a negative decision list.
- A packet template and three filled packets that each produce a required decision.
- Pause mechanics a handler would notice the next morning.

## What done looks like

A quiet week can end in "continue" without anyone hunting for a win. A confounded week cannot be used as expansion evidence, and expansion is not even on the menu. One bad committed sentence triggers the incident path the same day, not at the ritual. The pause state tells the handler what to do at 9:00 a.m. Banned fields are written down.

## Think a step ahead

The same week can contain a real model regression and a real product change, and the confounder flag will correctly stop you from using the proxy while also stopping you from acting on the regression. Add a separation note. When the week is confounded, the ritual may still order a targeted offline rerun of the golden set and the contract probes on the current build, and that rerun — not the online proxy — is what can justify a pause. Write who kicks off the rerun, the maximum hours you will wait for it, and the default if it is late (restrict prose, because waiting without a decision is a decision). The follow-on keeps a confounded week from becoming a week in which nobody is allowed to act.

## Interview angle

Walk the incident week from the single note to the handler's next morning. The ritual is real if the floor can feel the decision.
