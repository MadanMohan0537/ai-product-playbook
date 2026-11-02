# Decision Dashboard Spec

**Days 39–40 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor's pilot owner is the Columbus claims manager. She has twenty minutes on Monday morning. The VP of Claims Operations joins once a month and asks whether to hold, expand, or stop. Both of them need a dashboard. They do not need the same one. The underlying metrics are the tree from days 31–32, computed from the tracking plan, with audit results arriving later than product events.

## Concept

A dashboard spec is a decision tool described on paper: the question the page answers, the person who answers it, the chart or figure that answers it, the comparison that makes the figure mean something, and the action that is allowed from this page. A chart without an allowed action is a poster. This project specifies two pages, manager and VP, and the page you will not build.

You will not implement a BI tool. A spec that names sources, windows, and the sentence under each figure is the product work. Implementation can follow in whatever stack the company already uses.

## Approach

For every figure, write five lines:

1. Decision it serves.
2. Metric definition name, matching the tree exactly. If the name is new, the tree is incomplete; go back and add it there first, or drop the figure.
3. Comparison: versus the prior week, versus the 3.1% citation baseline, or versus the citations-only fallback. A number without a comparison does not go on the page.
4. Freshness: when the figure can be wrong because audit results lag, or because Friday's library index has not run.
5. Allowed action: what this person may decide from this figure alone, and what they must not.

The manager page is operational. Include the tail-cost count from the unit-economics follow-on if you wrote one (drafts over the token ceiling), the share of commits with no citation opened, the no-source rate, and a list of notices where the draft was discarded. She can act on coaching and on content bugs.

The VP page is the three-decision page: expand, hold, or stop. It shows the north-star, the veto guardrail, and the counter-metric, each with the comparison, and it shows sample size in audited notes so a noisy week cannot look precise. It does not show drafts per handler.

Specify an empty state for week 0 and a degraded state for "audit file late." Degraded is a designed page, not a blank chart.

## Components

- **Audience and cadence.** Who opens which page, which day, for how long.
- **Figure list.** The five-line block for each figure. Six figures is enough. More than eight means you are designing a poster.
- **Layout note.** What is above the fold for a laptop screen the manager actually has. One sentence on what a phone view would drop.
- **Degraded and empty states.** Copy for "not enough audited notes" and "pipeline late," including who gets notified.
- **Will-not-build list.** At least three charts a stakeholder is likely to request, and the reason each is absent. Leaderboards of handlers by speed belong here.

## Flow

1. Write the allowed actions for each audience before you pick charts. Actions constrain figures.
2. Select figures from the metric tree only.
3. Write comparison, freshness, and degraded copy for each.
4. Draft the will-not-build list by imagining the VP's staff meeting. Put the flattering charts there.
5. On day 40, read the spec as if the audit file failed to arrive. Confirm the Monday page still tells the manager what to do this week, and tells the VP that the monthly decision waits.

## Tools and stack

Markdown. Optional wireframe in mermaid or a rough grid. No BI license. If you later build the page, the spec remains the source of what the page is allowed to cause.

## Setup

1. Create `harbor-portfolio/39-dashboard/spec.md`.
2. Have the metric names in front of you. Do not rename them in the spec.
3. Day 39 is audiences, actions, and figures. Day 40 is degraded states, the will-not-build list, and the late-audit read-through.

## Deliverables

- Two page specs, manager and VP, with five-line figure blocks.
- Empty and degraded copy.
- A will-not-build list.

## What done looks like

A designer can lay out the page without inventing a metric. An analyst can see the freshness risk on the citation figure. The VP page cannot be used to rank handlers. The Monday page still has an allowed action when the audit file is late.

## Think a step ahead

A dashboard that becomes a target will be gamed. Handlers who learn that "citation opened" is on the manager page may click a citation and not read it. Add a note on the metric you will watch for that gaming, such as citation opens with a time-to-close under a threshold you set, and the conversation you will have if it moves. Write the threshold as a hypothesis. This is a product risk of measurement, and it belongs in the spec so the page does not pretend to be neutral.

## Interview angle

Describe one chart you left off and the allowed action on the chart you kept. Dashboard work is the editing.
