# AI Interaction Tracking Plan

**Days 33–34 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor sits beside Lumen for Northline Mutual handlers. A handler opens a new personal-auto notice, requests a draft, sees citations, may edit, and commits a note under their own name. Discarding the draft and writing the note alone is an allowed outcome. The metric tree from days 31–32 is the list of decisions this tracking plan must be able to support.

## Concept

A tracking plan names the events, properties, and identities a product will record so that a metric definition can be computed later without a rewrite. For a generative feature, the plan has to distinguish a draft the model proposed, a draft the handler edited, and the text that was committed. If you log only "note saved," you will never know whether Harbor changed the work.

This project writes the plan for the pilot episode. It also writes the events you will not log, because a claims note is sensitive, and "log everything in case we want it" is how a pilot becomes a privacy incident.

## Approach

Define a small event vocabulary. Prefer a few events with strict properties over a dozen vague ones. A workable set:

- `notice_opened` — a new auto notice is opened by a handler in the pilot office.
- `draft_requested` — the handler asks Harbor for a draft on that notice.
- `draft_shown` — a draft was displayed, with a result state: `cited`, `no_source`, or `declined` (out of job, such as a coverage question).
- `citation_opened` — the handler opened a specific citation.
- `draft_edited` — the handler changed proposed text, with a coarse size of edit, not the text itself.
- `draft_discarded` — the handler threw the draft away.
- `note_committed` — Lumen received a note, with `used_draft` true or false, and the handler id as author.

Properties should include a notice id, a handler id, an office id, a draft version id, and timestamps. The plan states the join key that connects a commit to the draft version the handler saw.

Write an explicit exclusion list. Do not log the full note body, the claimant's free-text description, or the policy number in the product analytics stream. Those belong, if anywhere, in the claims system under its existing retention rules. The analytics stream carries identifiers a metric needs and a content class ("citation opened"), not the claim.

For each metric on your tree, write the event path that computes it, or write "cannot compute; definition or event missing" and fix one side. This crosswalk is the actual test of the plan.

## Components

- **Event dictionary.** Name, when it fires, when it must not fire, required properties, id allowed to be joined.
- **Identity note.** Which id is a person, which is a claim, and who approves a new join.
- **Exclusion list.** Fields that feel useful and are out, with the reason.
- **Metric crosswalk.** Each tree metric mapped to events, plus gaps.
- **Data-quality checks.** Three checks a pipeline owner could run: drafts shown without a request, commits with an unknown draft version, citation opens after discard. These are product rules, not a pipeline implementation.

## Flow

1. Start from the metric tree. List the events the definitions require before you invent any others.
2. Write the dictionary. For each event, write one case where it must not fire. Example: `draft_shown` does not fire when the wizard, in a test session, is a human. Pilot data and usability-test data stay in different streams.
3. Write the exclusion list with a privacy partner in mind. If you are alone, write the question you would ask them and take the stricter option in the meantime.
4. Build the crosswalk. Fix gaps by changing the event or by narrowing the metric. Say which you did.
5. On day 34, hand the dictionary to someone else and ask them to compute "share of shown drafts that were committed unedited" from your words alone. Revise wherever they have to guess.

## Tools and stack

Markdown tables. No event-collection SDK and no warehouse. A CSV sketch of five fake rows, with no real personal data, is optional and useful for the crosswalk.

## Setup

1. Create `harbor-portfolio/33-tracking-plan/plan.md`.
2. Paste the metric names from the tree at the top.
3. Day 33 is the dictionary, identities, and exclusions. Day 34 is the crosswalk and the second-person read.

## Deliverables

- An event dictionary with must-not-fire cases.
- An exclusion list and an identity note.
- A metric crosswalk with gaps resolved, plus three data-quality checks.

## What done looks like

An engineer can implement the events without inventing properties. A privacy reviewer can see that note text stays out of the analytics stream. Every north-star and guardrail metric has an event path or a written reason it waits on the audit sample instead.

## Think a step ahead

Handlers will work around a clumsy commit path, and your events will then describe the workaround rather than the work. Add a "shadow path" note: how you would detect notes committed to Lumen with no Harbor events at all, using a count from the system of record compared with `note_committed`. Define the ratio and who looks at it weekly. A tracking plan that cannot see its own bypass will report a rosy adoption number while the real notes go around it. The analytics trust runbook on days 89–90 is the operational version of this worry.

## Interview angle

Explain one field you refused to log, and the metric crosswalk entry that was hardest to support without it. That is product analytics judgment.
