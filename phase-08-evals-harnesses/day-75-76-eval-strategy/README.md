# Evaluation Strategy

**Days 75–76 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Harbor has several behaviors a reasonable person might "evaluate": edition selection, bulletin precedence, retrieval reason codes, sentence support, out-of-job refusals, citation display, and the audit-priority score. They do not belong in one score. The pilot has a shadow-week gate and a limited-pilot gate. The strategy says which evidence must exist at each gate, who looks at it, and which fashionable evaluations you are not running.

## Concept

An evaluation strategy is the map from decisions to evidence. It chooses a small number of checks, assigns each a method and an owner, and states what the check is allowed to block. A single "quality score" that averages a refusal task with a rental-limit task will move when either moves, and the gate will become a negotiation. The strategy exists to prevent that negotiation from being improvised.

This project writes the strategy for Harbor. It does not build a harness. The harness requirements on days 83–84 have to serve this document, so this one comes first.

## Approach

Make a table of behaviors. For each: the decision it informs, the method, the artifact that already holds the expected answers, the gate it can block, and the person who can waive it. Methods to use, and to keep distinct:

- **Rule check.** Edition id and bulletin id against the catalog. Exact. Can block shadow week.
- **Set grading.** The golden question set's reason codes and ids. Can block shadow week. Slice floors from that project, not a blended accuracy.
- **Rubric grading.** Sentence support and tone, on items a trainer scores with the labeling guideline. Can block the limited pilot's prose drafts. Cannot, by itself, block citation-only mode if you have a fallback.
- **Contract probes.** A handful of scripted asks for coverage and claimant messaging. A single failure blocks. These are not averaged.
- **Human spot review.** The monthly sample from the error-analysis follow-on. Informs the card's failure-mode list. Does not by itself expand the pilot to another state.
- **Online proxies.** Citation opened before commit, discard rate, no-source rate. These watch the pilot. They are not offline "evals," and the strategy says so, because they measure handler behavior and product fit together.

Explicitly out of this pilot's strategy, with a reason: a public benchmark score, a preference-model leaderboard, a single overall grade from an automated judge, and a vendor's self-reported accuracy. You may revisit an automated judge after a person has graded a sample large enough to see whether you agree with it. Until that agreement is measured, a judge does not gate. Write that as a sequencing rule, not as a permanent ban.

Write the waiver path. A slice floor can be waived only by the claims operations A on the offline-eval gate, in writing, for one week, and a waived floor is reported as waived on the VP page. A failed contract probe cannot be waived.

## Components

- **Behavior table.** The columns above. Every behavior you have specified in earlier projects should appear or be consciously omitted with a reason.
- **Gate binding.** Which rows block shadow week, which block prose in the limited pilot, which only inform.
- **Out-of-strategy list.** With reasons and the sequencing rule for automated judges.
- **Waiver path.** Who, how long, how it shows up on the VP page.
- **Owner load.** Hours per week the trainer and the content analyst are actually spending on evals during the pilot, checked against the capacity assumption in the sprint-goal follow-on. If the strategy needs more hours than they have, cut a row. A strategy that cannot be staffed is a poster.

## Flow

1. Inventory behaviors from the interaction contract, the retrieval requirements, and the labeling guideline. This is a coverage check on your own work.
2. Assign methods. If two methods are guarding the same decision, keep the one that can fail clearly and demote the other to informational.
3. Bind rows to gates. Bind the contract probes to a non-waivable fail.
4. Write the out-of-strategy list before anyone asks for a leaderboard in the review.
5. On day 76, staff the strategy. Cut or defer a row if the hours do not fit, and record the cut as a risk, not as a silent omission.

## Tools and stack

Markdown. Earlier specs as the inventory. No eval framework. The table is the strategy. A framework that appears later is acceptable only if it implements a row in the table.

## Setup

1. Create `harbor-portfolio/75-eval-strategy/strategy.md`.
2. Start with the inventory so beloved metrics cannot crowd out contract probes.
3. Day 75 is the table and gate binding. Day 76 is waivers, the out-list, and the staffing cut.

## Deliverables

- A behavior table bound to gates.
- A non-waivable probe rule and a waiver path for slice floors.
- An out-of-strategy list and a staffing note that cuts or confirms the plan.

## What done looks like

No blended quality score gates the pilot. Contract probes can fail the gate on a single item. Automated judges are sequenced behind an agreement check you have not pretended to complete. The trainer's hours are a constraint you applied. Every row points at an artifact that holds the expected answer, or the row says the artifact is still missing.

## Think a step ahead

Online proxies arrive while you are still changing the product, so a week-over-week move mixes product changes with model changes. Add a calendar rule: any week that contains a corpus publish, a prompt or model version change, or a new handler cohort is marked "confounded" in the review, and the online proxy is reported as a watch item rather than as evidence for a gate. Write the three confounders and who marks the week. The follow-on is interpretive discipline, which a clean dashboard will not apply for you.

## Interview angle

Explain why a single quality score does not gate Harbor, and which failure cannot be waived. Strategy is the binding, not the catalog of metrics.
