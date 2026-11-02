# Labeling Guideline and Adjudication

**Days 55–56 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Harbor needs a small set of human judgments to grade drafts and, later, to test edition selection when Lumen's dates are missing. The judgment is not "is this note good?" That question produces taste. The judgments you will specify are narrower: given a fixture claim, a candidate form edition, and a candidate bulletin, a trained reader marks whether the pair is the correct source set, and whether a drafted sentence stays inside that set. Two readers will disagree. The guideline is how they disagree in the same way, and how a third person resolves it.

## Concept

A labeling guideline is a product document. It defines the decision, the unit being labeled, the examples that sit on the boundary, and the adjudication path. It is also a scope tool. Every vague instruction becomes a silent labeler, and silent labelers do not match. You will write the guideline for Harbor's source-set task and sentence-support task, write fifteen gold examples with answers and rationales, and write the adjudication rule for the pairs of examples where you expect disagreement.

## Approach

Define the unit. For the source-set task the unit is a (notice, edition, bulletin-or-none) triple. The label is `correct`, `wrong_edition`, `wrong_bulletin`, or `insufficient_record`. `insufficient_record` is a real label, used when the fixture does not contain the dates a human would need. It is not a failure of the labeler.

For the sentence-support task the unit is a (sentence, cited span) pair. The label is `supported`, `unsupported`, or `out_of_job`. `out_of_job` covers coverage decisions and claimant messages. A sentence can be supported by the span and still be out of job if it draws a coverage conclusion the span did not ask for; write the precedence. Out-of-job wins, because the contract cares about that boundary even when the words appear in a form.

Write boundary examples on purpose:

- A rental limit that matches the form and ignores a newer bulletin.
- A sentence that copies the bulletin and cites only the form.
- A sentence that says "coverage applies" using words that do appear in an insuring agreement.
- A glass-only notice where the correct edition still applies and the draft adds glass advice the sources do not contain.
- A record with an effective date missing, where the honest label is `insufficient_record`.

Each gold example has the fixture text (short, fictional, marked as fixture), the label, and a two-sentence rationale a new labeler can check. Include at least three examples you consider genuinely borderline, with the rationale stating what you decided and what a reasonable labeler might do instead. Those three go to adjudication in the guideline, with a rule: if two labelers disagree and one of them chose the borderline rationale you wrote, the adjudicator may pick either, and the item is flagged `unstable` so it does not become a silent training target later.

Set an agreement target as a product goal, not as a number you pretend to have measured. For the source-set task, ask for exact agreement on a double-labeled sample before those labels are allowed to gate a pilot. State that you will compute agreement when a second reader exists, and that until then the guideline is untested. Name the statistic you expect a partner to compute later (percent agreement and a chance-corrected measure) without faking the value.

## Components

- **Task definitions.** Unit, labels, precedence, and what the labeler is forbidden to infer.
- **Fifteen gold examples.** Fixture text, label, rationale. At least three borderline.
- **Adjudication rule.** Who adjudicates (a claims trainer, not the engineer who built the draft), the `unstable` flag, and how fast a disputed item must be resolved during the pilot.
- **Labeler instruction page.** One page, in the labeler's language, including "do not fix the sentence, label it."
- **Untested stamp.** A visible note that agreement has not been measured yet, and the sample size you would want before trusting the guideline (a number of double-labeled items you choose and justify in a sentence).

## Flow

1. Write labels and precedence before examples, or the examples will invent the labels.
2. Draft fifteen examples. Mark the three you had to think about. Those are the borderline ones. If you had to think about none, the set is too easy to be a guideline.
3. Write the labeler page from the definitions, then try to label three of your own examples using only the page, a day later or after a break. Fix the page where you hesitate.
4. Write adjudication and the untested stamp.
5. On day 56, have another person label five examples from the page alone, without your rationales. Compare. Update the page where they miss for a reason the page could have prevented. Record what you changed.

## Tools and stack

Markdown. A second person for the five-item trial. No labeling platform is required at this size. If the set later lives in a tool, the guideline text is still the source of truth.

## Setup

1. Create `harbor-portfolio/55-labeling/guideline.md` and `gold-examples.md`.
2. Mark every policy sentence as fixture language so nobody mistakes it for Northline's forms.
3. Day 55 is definitions and the fifteen examples. Day 56 is the trial with a second reader and the revision.

## Deliverables

- A guideline with units, labels, precedence, and labeler instructions.
- Fifteen gold examples with rationales and three borderline calls.
- An adjudication rule, an untested stamp, and a note from the second-reader trial.

## What done looks like

A new reader can label a sixteenth item from the page. Out-of-job precedence is explicit. `insufficient_record` exists so labelers are not forced to guess. The second-reader trial changed the page, or you recorded that it did not and why. Agreement is not invented.

## Think a step ahead

Guidelines rot when a new bulletin type appears (a temporary moratorium, a state department circular) that is not an "amendment" in the sense your labels used. Add a change protocol: who can add a label, why adding a label invalidates agreement you may later measure, and how items labeled under the old guideline are marked with a guideline version. Write the version field now, on every gold example, starting at `g1`. A set without versions cannot be repaired; it can only be doubted.

## Interview angle

Show a borderline example, the two plausible labels, and the precedence that chose one. Then mention the untested stamp. Honesty about measurement is part of the craft.
