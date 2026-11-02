# Feature Specification, Leakage, and Prohibited Fields

**Days 57–58 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Someone on the Harbor program proposes a classical model to prioritize the audit queue: score a committed note for "likely citation defect" so supervisors sample smarter than 8% at random. The proposal is optional and separate from the draft product. It is the cleanest place in this case to practice a feature spec, because the temptation to cheat, accidentally, is concrete. Lumen holds fields that would not have existed at the time the note was written, including the supervisor's later bounce-back.

## Concept

A feature specification says what a model may see, what each field means in the business, when the value is known, and which fields are prohibited because they leak the answer or because the company will not put them in a decision. Leakage is a product bug as much as a modeling bug. A feature that includes "supervisor bounced this note yesterday" will look brilliant offline and be useless at the moment of sampling, because the bounce has not happened yet. A feature that includes the claimant's race, or a proxy the company has banned, is a different kind of prohibited, and it stays prohibited even if it predicts.

This project writes the spec for the audit-priority model as a product artifact. It does not train the model. Training would only hide a bad spec behind a score.

## Approach

Write the decision the score supports: which notes enter this week's audit sample, in the Columbus pilot, among committed Ohio personal-auto notes. The score does not decide defectiveness. A person still audits.

For each candidate feature, record:

- **Meaning.** The business definition, not the column name.
- **Source system.** Lumen, Harbor logs, or the content catalog.
- **Time rule.** The value as known at commit time. If the field is updated later, the spec says which version is legal. This is the point-in-time rule.
- **Use.** Included, included only as a slice for later error analysis, or prohibited.
- **Reason.**

Prohibited, with reasons you should write in your own words after you agree:

- The supervisor's bounce, any audit outcome, and any field derived from them. These are the label, not the features.
- The handler's identity, as a feature. It may exist as a join key for evaluation slices (new versus tenured) and must not be a model input. A model that learns "Andre's notes are risky" will punish a person.
- Claimant race, ethnicity, religion, and fields you judge to be close proxies for this decision (for example, a neighborhood code, if you cannot explain a non-proxy use). Prohibited.
- The full note text in the first version. It will smuggle the citation language you are trying to judge and will make the spec unauditable. You may list it as a later version with a review gate, not as a silent addition.

Included candidates you should pressure-test: whether a citation was opened before commit, edit size, no-source result state, hours between notice and commit, whether the bulletin on the notice was structured, claim subtype if known at notice time, and handler tenure as a slice only.

Write two leakage stories in prose. One is temporal: a feature that was added after the outcome. One is identity: a feature that looks like process and functions as a person id. Both stories use Harbor fields.

## Components

- **Decision statement.** What the score may change in the audit workflow, and what it may not change.
- **Feature table.** The columns above, for at least ten candidate fields, including prohibited ones. Prohibited fields stay in the spec so someone sees the refusal.
- **Point-in-time rule.** A paragraph your data partner can implement: "features are values as of note commit, joined on notice id."
- **Leakage stories.** Two, each ending with the test that would have caught it (train on a later field, watch the offline score collapse when the field is removed).
- **Slice plan.** Tenure and claim subtype as evaluation slices, explicitly not as inputs, and the minimum slice count below which you will not report a rate.

## Flow

1. Write the decision statement. If the score changes who gets audited and also how handlers are managed, stop and cut the second use. This spec is for audit sampling only.
2. Inventory fields from the tracking plan and from Lumen as you understand it. Mark the time each becomes known.
3. Fill the table, prohibited rows included.
4. Write the two leakage stories from fields you almost included.
5. On day 58, have a partner propose one more feature that would raise an offline score. Decide in writing, against the table's rules. If you add it, add the time rule too.

## Tools and stack

Markdown tables. The tracking plan is the inventory of Harbor-side fields. No model training and no feature store. The spec is the contract a later pipeline would have to meet.

## Setup

1. Create `harbor-portfolio/57-features/spec.md`.
2. Write "as of commit time" at the top before listing fields, so the time rule is not an afterthought.
3. Day 57 is the decision and the table. Day 58 is leakage stories, slices, and the partner's extra feature.

## Deliverables

- A decision statement for audit sampling only.
- A feature table of at least ten fields with point-in-time notes and prohibited rows.
- Two leakage stories and a slice plan.

## What done looks like

A data partner can see which version of a field is legal. Bounce-back is on the page as prohibited, with the reason. Handler identity is a slice key and not an input. The spec can be reviewed without a notebook. At least one tempting feature was refused in the partner exercise or accepted with a time rule.

## Think a step ahead

The legal time for a citation defect is not commit time alone. The form that was correct at commit may be the form that was in force on the date of loss, which can be months earlier, and a bulletin published between the date of loss and the commit is a different fact from a bulletin published after commit. Extend the point-in-time rule with two clocks: facts about the policy as of the date of loss, and facts about the handler's session as of commit. Write one feature that is legal on the first clock and illegal on the second, and one in the other direction. A spec with a single clock will be implemented with whichever timestamp was easiest to join.

## Interview angle

Tell one leakage story all the way to the test that catches it. Then name a field you prohibited for a fairness reason, separate from leakage. They are different refusals.
