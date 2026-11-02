# Golden Question Set

**Days 69–70 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** Harbor's retrieval step needs a set of notices with known-correct source ids, so a trainer can apply the success check from the retrieval requirements. The set is a product asset. It encodes the situations you care about, including situations where the correct result is to return nothing. It is also a leakage risk: if the same items are pasted into a prompt as examples, you are grading the system on answers you handed it.

## Concept

A golden set is a list of inputs, expected outputs, and tags, built to measure a behavior you specified. For Harbor the input is a notice context (state, line, date of loss, the rule layer's edition id or the fact that it abstained, and the catalog's view of bulletins). The expected output is a set of document ids plus a reason code, not a paragraph of prose. Prose expectations belong to the drafting eval, and mixing them into the retrieval set makes both scores muddy.

You will author the set on paper, at a size you can actually curate: 25 items. You will tag slices, include unanswerables, and write the handling rules that keep the set out of prompts and out of casual demos.

## Approach

Compose 25 items so the slices are deliberate. A suggested mix, which you may adjust if you explain the change:

- 8 items where one edition is in force and no bulletin applies. Expected reason `ok`, one id.
- 5 items where a bulletin amends a limit. Expected ids: edition and bulletin.
- 4 items where a newer edition exists and is not in force for the date of loss. Expected: the older id only.
- 3 items where the catalog knows a bulletin the corpus does not contain. Expected reason `bulletin_missing`, no draft passages.
- 3 items where the rule layer abstains. Expected reason `no_edition_in_force`. The set must not smuggle the right edition into "context."
- 2 items from the wrong line or state, included because a real queue will contain them. Expected: no personal-auto Ohio passage. Choose the reason code that matches your requirements; if none fits, add `out_of_corpus` to the requirements and record that you extended the spec.

Each item is a row: id, slice tag, notice facts, catalog facts, expected ids, expected reason, and a one-line note on why it is in the set. Use fictional ids (`OH-PA-2026-02`, `BUL-1044`). Do not paste real policy language into the set. The retrieval set checks identity and reason, not wording. Wording checks use the labeling guideline's sentence-support task and should be a different file, which you may point at and should not merge.

Write the leakage rule. Items in this file are evaluation-only. They are not few-shot examples. A demo that uses a golden notice is labeled a demo and its score is not reported as the set's score. Anyone who wants to add an item copies the row format and assigns a version. Anyone who wants to delete an item marks it retired with a reason, and does not renumber the rest.

Write the bar in counts, since 25 is small. Example shape, for you to set and defend: zero wrong-line inclusions, and at most one miss on the bulletin-amendment slice, before the retrieval step can enter shadow week. A bar of "90% overall" can be met while every `bulletin_missing` item is wrong. Slice floors are the point. With three items in a slice, say so, and prefer "all of these three" to a percentage that pretends precision.

## Components

- **Row schema and 25 rows.**
- **Slice counts.** A short table so a hole is obvious. If a slice has fewer than three items, justify it or add items by shrinking a saturated slice.
- **Bar.** Slice floors, in counts, tied to the shadow-week gate.
- **Leakage and version rules.** Eval-only, no renumbering, retirement instead of deletion.
- **Known gap.** What this set does not measure (prose faithfulness, page locators, handler behavior). Point at the project that measures each, so nobody treats this file as the whole quality story.

## Flow

1. Write the row schema and the slice targets before authoring items, or you will write twenty easy matches.
2. Author the unanswerables and the wrong-line items first, while you are still willing to make the set harsh.
3. Fill the rest. Check counts.
4. Set the bar in counts. If you cannot explain a floor to the Columbus manager, the floor is a vibe and you rewrite it.
5. On day 70, try to "cheat" your own set: describe one prompt example that would inflate a demo. Write the rule that makes that cheat visible. If you cannot describe a cheat, the set is too abstract to leak, which is acceptable, and you should still write the rule.

## Tools and stack

A CSV or a markdown table. No retrieval stack. The asset is the rows and the rules. Implementation of scoring can be a later engineering task that reads this file.

## Setup

1. Create `harbor-portfolio/69-golden-set/questions.csv` and `rules.md`.
2. Freeze slice targets at the top of `rules.md`.
3. Day 69 is rows and counts. Day 70 is the bar, leakage rules, and the cheat test.

## Deliverables

- Twenty-five rows with expected ids and reason codes.
- Slice counts and a bar written in counts.
- Leakage, versioning, and retirement rules, plus a known-gap note.

## What done looks like

A trainer can grade a retrieval result against a row without watching a draft. Unanswerable items exist and expect a reason code, not a near-match passage. The bar cannot be passed by the easy slice alone. The file says it is not few-shot material. Real policy text is absent.

## Think a step ahead

Items will saturate: once the system gets all eight easy matches for a month, those rows stop teaching you anything and still dominate an overall number. Write a saturation rule. A slice that has been perfect for a number of consecutive runs you set is reported separately and is no longer allowed to carry the headline number. Replacing a saturated item requires a new id, a harder neighbor, and a retirement note on the old one. The follow-on keeps the set pointed at the failures you still have, which a frozen leaderboard will not do.

## Interview angle

Show the slice counts and the bar. Explain one unanswerable row and why a fluent paragraph would still fail it. You are grading retrieval, not charm.
