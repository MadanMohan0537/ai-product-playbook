# Gold-Set Charter

**Days 79–80 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Harbor now has more than one curated set: 25 retrieval rows, 15 labeling examples, contract probes, and rubric anchors that quote fixture spans. They will be copied into slides, pasted into prompts, extended by whoever is online, and used to claim a gate passed. A charter is the rulebook that keeps a set from becoming a prop.

## Concept

A gold-set charter names each set, its purpose, its owner, what it is allowed to gate, how items are added and retired, how leakage is prevented, and what must be true before a number from that set is spoken in a VP review. It is governance for a small pile of files. The pile is small enough that governance feels like overhead, which is why the charter has to be short enough to be kept.

This project writes the charter for the sets you already have and for the one set you do not have yet and will be asked for: a "general quality" set that blends everything. The charter declines that set.

## Approach

One section per existing set, plus a declined section. For each living set:

- **Purpose.** The decision it supports, copied from the eval strategy, not reinvented.
- **Unit and schema.** Point at the file. Do not fork a second schema in the charter.
- **Owner and editor.** One owner. Editors may propose rows; the owner accepts. For the retrieval set the owner is the content analyst. For contract probes the owner is product, with legal consulted when a probe's expected behavior changes.
- **Gate use.** What it may block, matching the strategy. If this project and the strategy disagree, fix one of them in this pass and say which you changed.
- **Change control.** New ids, no renumbering, retirement notes, version on every row. You already wrote pieces of this. The charter is where they become one policy.
- **Leakage controls.** Not used as few-shot examples. Demo runs that use set items are tagged `demo` and excluded from gate reports. A set file does not live in the same repository directory as prompt text. Write the directory rule even if both are just folders in a portfolio; the habit is the point.
- **Reporting minimum.** Below a stated count, or below a slice floor, the report says "not reported" rather than a percent. Reuse the floors you already set. Where you never set one, set it here.

The declined "general quality" set gets a short section: the reason a blended set invites a blended score, the stakeholder sentence you expect ("we need one number"), and the alternative you will offer (the VP page's three separate figures). Do not create the set "just so we have it."

Add a sampling rule for growth. When a set grows past a size you choose (for example, 100 retrieval rows), gate reports move from "full set" to "full set on contract probes, stratified sample on the rest," and the charter names who draws the sample. Until that size, you run the full set, because 25 rows that are sampled into 10 are theater.

## Components

- **Set sections.** Purpose, owner, gate, change control, leakage, reporting minimum.
- **Declined set.** The blend, with the alternative offer.
- **Directory and demo rules.** Where files live relative to prompts, how a demo is tagged.
- **Disagreement log.** Any place you changed the eval strategy or a set's earlier rules to match the charter.
- **Growth rule.** The size at which you stop implying that every row runs every day, and what replaces it.

## Flow

1. List the sets you actually have files for. A set that exists only as a paragraph in an earlier README is marked "not chartered until the file exists."
2. Fill owners. If the content analyst owns every set, say so and cut the gate scope until the hours from the strategy still hold.
3. Write the declined blend and the sentence you will say in the meeting.
4. Reconcile with the strategy. Record every edit.
5. On day 80, simulate a helpful engineer pasting three golden notices into a prompt "as examples of good behavior." Write the review comment you leave, citing the charter section. The comment is a deliverable. It shows the charter can be applied.

## Tools and stack

Markdown. The set files and the eval strategy. No annotation platform. Governance at this scale is a short document people can find.

## Setup

1. Create `harbor-portfolio/79-charter/charter.md` and `review-comment.md`.
2. Inventory files first so you do not charter ghosts.
3. Day 79 is set sections and the declined blend. Day 80 is reconciliation, the growth rule, and the review comment.

## Deliverables

- A charter covering the living sets and declining the blended set.
- A disagreement log of reconciliations.
- A review comment that applies the leakage rule to a concrete paste.

## What done looks like

Each living set has one owner and a gate that matches the strategy. The blended set does not exist. The review comment cites a section and tells the engineer where examples may come from instead (a separate, non-gating example file, which you may create as an empty file with a header that says it is not a gold set). Reporting minimums are in counts. Growth has a rule before the set is large.

## Think a step ahead

Sets that gate releases become targets. A team will write drafts that pass the 25 retrieval ids and fail the notice that arrives on Thursday. Add a holdout rule. A fraction of new items you choose (for example, one in five, with a minimum of five items once the set is large enough) is marked `holdout`, excluded from any prompt-development loop, and reported separately. Developers do not get the holdout expected answers in the everyday file; the owner runs that slice. Write how small Harbor's current set is and the size at which the holdout rule turns on. Turning it on at 25 may be too early; leaving it off forever guarantees a set that has been memorized. Pick the threshold and the reason.

## Interview angle

Explain the declined set and the review comment. You are showing you can govern an eval asset, not only author one.
