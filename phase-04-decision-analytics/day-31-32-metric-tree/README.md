# Metric Tree and Counter-Metrics

**Days 31–32 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor proposes a cited note for personal-auto handlers in Northline Mutual's Columbus office, and the handler commits it under their own name. Today's baseline is 26 minutes average handle time on a new auto claim, about 9 minutes of form-finding, and 3.1% of audited notes citing a form that was not in force. The pilot is 40 handlers. Harbor does not decide coverage.

## Concept

A metric tree connects a decision you might take to a number you can move, and it pairs every efficiency number with a number that would reveal you had moved it by making the work worse. For Harbor, a drop in handle time is not success if the citation defect rises, if handlers commit drafts they did not read, or if supervisors bounce more notes. The tree is the agreement, made before the pilot, about which movements count.

You will define the tree, the decision each metric can trigger, and the metric you will refuse to call a success metric even if it goes up.

## Approach

Start from decisions, not from events you happen to be able to log. Write three decisions the pilot might face in week six:

1. Expand beyond Columbus, hold, or stop.
2. Keep prose drafts, or fall back to citations-only.
3. Change the commit rule that asks the handler to open a citation.

For each decision, name the one metric that would push you toward the more aggressive option, the guardrail that can veto it, and the counter-metric that catches a hollow win. Example of a hollow win: median handle time falls because handlers paste the draft unread, while supervisor rework rises two weeks later. If your tree has no lagging quality metric, it will bless that outcome.

Define each metric in a sentence a second analyst could implement: numerator, denominator, who is in the population, and the window. "Engagement" does not qualify. "Share of new Ohio personal-auto notices in the pilot office, during a week, where the committed note's cited form edition matches the edition in force on the date of loss, among notes that were audited" is a definition. You may also define a proxy for the days when the audit sample has not landed yet, and you must label it as a proxy.

Write the baseline beside each metric where the case gives you one, and "unknown, measure in week 0" where it does not. Do not invent a baseline for draft acceptance.

## Components

- **Decision list.** The three decisions above, possibly revised, each with the choice set.
- **Tree.** One north-star for the pilot, input metrics that should move first, guardrails, and counter-metrics. A sketch is fine if every node has a definition under it.
- **Definition table.** Name, numerator, denominator, population, window, baseline, owner.
- **Veto rule.** Which guardrail movement stops an expansion conversation even if handle time improved.
- **Refusal list.** Metrics you will compute, perhaps, and will not put in the executive sentence. Drafts generated per handler is a candidate for the refusal list, because it rewards regeneration.

## Flow

1. Write the three decisions in language the VP of Claims Operations uses. If a metric cannot change one of those decisions, it does not go on the tree.
2. Draft the north-star. Test it against the hollow-win story. Adjust until the hollow win cannot look like success.
3. Fill the definition table. Have a second person try to implement one definition from the sentence alone. Revise the sentence where they get stuck.
4. Set the veto rule with a direction and a rough magnitude you would care about (for example, a rise in citation defects in the audit sample relative to the 3.1% baseline). You are setting attention, not a statistical test.
5. On day 32, write the refusal list and the week-0 measurement plan for every baseline you marked unknown.

## Tools and stack

Markdown and a simple diagram (mermaid or indented text). A spreadsheet is optional and useful for the definition table. No analytics warehouse. You are defining measures, not querying production.

## Setup

1. Create `harbor-portfolio/31-metric-tree/tree.md`.
2. Copy the case baselines into the file so you do not invent replacements.
3. Day 31 is decisions, tree, and definitions. Day 32 is the veto, the refusal list, and the week-0 plan.

## Deliverables

- A metric tree tied to three pilot decisions.
- A definition table with owners and baselines or explicit unknowns.
- A veto rule and a refusal list.

## What done looks like

The VP can read the veto rule without a briefing. Every metric on the tree has a definition another person could implement. At least one tempting metric sits on the refusal list with a reason. The hollow-win story is addressed by a node on the tree, not by a hope.

## Think a step ahead

Audit sampling covers about 8% of notes in the case's spirit (supervisors sample notes; use 8% if you need a working figure, and label it as a planning assumption). A weekly citation-defect rate on that sample will bounce. Add a companion view you will not treat as a decision metric: the direction over four weeks, and the minimum number of audited notes you want before an expansion conversation. This is a measurement-design note, not a sample-size calculator. It stops a noisy week from looking like a quality collapse or a quality win.

## Interview angle

Explain the hollow win and the node that catches it. Then name a metric you refused to celebrate.
