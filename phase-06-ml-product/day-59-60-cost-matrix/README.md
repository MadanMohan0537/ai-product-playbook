# Cost Matrix and Offline Metric Choice

**Days 59–60 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** The audit-priority score from the feature spec is being evaluated offline on a fixture of 200 past Columbus notes, of which 20 were later judged citation defects. You are not fitting a model. You have been given two candidate score thresholds, A and B, and the confusion counts at each. You must choose the operating point and the metric that justifies it, using costs a claims manager can recognize. Accuracy is available and you are expected to explain why you are not choosing on accuracy.

## Concept

When misses and false alarms have different costs, a single summary number is a product decision disguised as math. For audit priority, a false alarm means a supervisor spends time on a clean note. A miss means a defective citation stays in the 92% of notes that are not audited, which is the current world, except that the pilot may now feel "covered" by the model and sample even less thoughtfully. The cost of a miss is not identical to the cost of a false alarm, and it is not identical for a glass-only claim and a total loss. This project makes that asymmetry explicit and picks an operating point.

## Approach

Use these counts as given for the 200-note fixture, where a "positive" prediction means "put this note in the audit sample":

|  | Defects caught (of 20) | Clean notes flagged (of 180) | Notes a supervisor would open |
| --- | --- | --- | --- |
| Threshold A | 14 | 30 | 44 |
| Threshold B | 8 | 10 | 18 |
| Random 8% sample (about 16 notes) | about 1 or 2 in a typical draw; use 2 as the planning comparison | about 14 | 16 |

The random row is a baseline, not a third model. It is the process Harbor's score has to beat to be worth existing.

Assign dollar placeholders a finance partner would replace. Write them as placeholders. A workable set to start from, and you should say you would replace it: one hour of supervisor time per audited note at a placeholder rate, and a placeholder expected cost for a missed citation defect that reaches a file a lawyer later reads. Because the second number is the whole argument, show the decision at two different miss-costs, a low one and a high one, so the reader sees the switch.

Compute, for A and B:

- precision and recall on the fixture,
- supervisor hours implied,
- total placeholder cost at the low miss-cost and at the high miss-cost,
- the comparison against the random baseline's planning numbers.

Choose an operating point for the pilot, or choose neither. Neither is allowed if the score does not beat the baseline on the cost that claims leadership believes, or if beating it requires a miss-cost they will not sign. Write the sentence you need them to sign.

Also write the metric you will report in the model review. It may be recall at a fixed supervisor-hour budget, which is a product constraint (the Columbus supervisor has hours for about 40 notes a week, not for an unlimited queue). Put that constraint in the choice. Threshold A opens 44 notes in this fixture's scale; say whether that fits the hour budget you are assuming for a week of Columbus volume, and adjust the choice if it does not. State your volume assumption.

## Components

- **Cost table.** Placeholder inputs, labeled, and the two miss-cost scenarios.
- **Operating-point sheet.** Precision, recall, hours, cost, baseline comparison.
- **Choice memo.** The point you pick or the decision to keep random sampling, the constraint that drove it, and the sentence leadership must sign.
- **Report metric.** The one number the review will headline, and the numbers that must be shown beside it so the headline cannot travel alone.
- **What accuracy does here.** A short calculation of accuracy at threshold A, and a sentence on why it flatters a screen that marks almost everything clean. Do the arithmetic. With 20 defects in 200, a screen that flags nobody is already 90% accurate.

## Flow

1. Compute the nobody-flagged accuracy first, so the trap is in the room before you look at A and B.
2. Compute precision, recall, hours, and costs. Show formulas in one line each.
3. Apply the supervisor-hour constraint. If your preferred point violates it, switch or propose a smaller sample and recompute. Do not leave the constraint as a footnote.
4. Write the choice memo and the sentence leadership must sign.
5. On day 60, change the high miss-cost to a number that flips your choice, and record that number. That sensitivity is part of the deliverable, because the placeholder is not sacred.

## Tools and stack

A spreadsheet or a calculator, plus a memo. No model fitting. The counts are the dataset.

## Setup

1. Create `harbor-portfolio/59-cost-matrix/choice.md` and a small sheet.
2. Write the placeholder rates at the top so they cannot hide in a formula.
3. Day 59 is the arithmetic and the baseline. Day 60 is the constraint, the choice, and the sensitivity flip.

## Deliverables

- An operating-point sheet with the random baseline.
- A choice memo leadership can sign, including the hour constraint.
- The accuracy trap, computed, and the miss-cost that flips the choice.

## What done looks like

The arithmetic can be redone from the memo. The choice beats random sampling on a stated cost, or the choice is to keep random sampling. Accuracy is computed and rejected as the decider, with the 90% figure visible. The hour constraint is applied, not admired.

## Think a step ahead

A missed defect on a total-loss file and a missed defect on a glass-only file do not share a cost, and this fixture does not tell them apart. Specify the next table you would demand before locking a threshold for a second quarter: the same confusion counts split by claim subtype, plus a rule that a subtype with fewer than a minimum you set is not given its own threshold. Write the minimum and the reason a separate threshold on a tiny cell would be a false precision. The follow-on is cost heterogeneity, which a single matrix hides.

## Interview angle

Lead with the 90% accuracy trap, then the operating point you actually chose and the constraint that chose it.
