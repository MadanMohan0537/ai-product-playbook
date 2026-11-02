# Anchored Quality Rubric

**Days 77–78 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Prose drafts that survive retrieval need a grader's rubric. The labeling guideline already covers two crisp judgments: whether the source set is correct, and whether a sentence is supported or out of job. What remains is the judgment a trainer makes when the sentence is supported and still a bad note: it buries the limit, it adds advice, it sounds like a denial, or it is so long the handler will not read it. Those judgments need anchors, or two trainers will produce two pilots.

## Concept

An anchored rubric is a scale where each score point has an example, so a grader matches the draft to an anchor instead of reaching for an adjective. For Harbor you will write a short rubric with three criteria, anchors at three levels, and a precedence order for when criteria conflict. You will also write the instruction that keeps this rubric from quietly replacing the contract probes. A draft can score well on tone and still be a failed contract probe. The probe wins, and the rubric does not get to average that away.

## Approach

Use three criteria:

1. **Faithfulness.** The draft stays inside the cited spans and the precedence rules. This overlaps the sentence-support label on purpose at the low end. The rubric's job at the high end is partial faithfulness: a limit is right and a harmless extra sentence is not in any source.
2. **Task fit.** The draft is a note a supervisor can audit: it includes the edition and the amended limit when one applies, and it omits coverage conclusions and claimant messages.
3. **Usability.** A handler can check it during the handle time you are willing to spend. Concrete and short. A faithful note that pastes an entire form fails usability.

Levels for each criterion: `fail`, `meet`, `exceed`. Write an anchor paragraph or sentence for each level, using fixture language marked as fake. Anchors are specific. "Somewhat faithful" is not an anchor. A `fail` faithfulness anchor quotes a $40 limit when the fixture span says $30. A `meet` quotes $30 and cites the bulletin. An `exceed` does that and flags the superseded bulletin without letting it be copied by accident, matching your citation behavior.

Write conflict precedence. Faithfulness and task fit outrank usability. A short coverage denial is a `fail` on task fit even if it is short, polite, and confident. Usability never rescues it. Between faithfulness and task fit, a contract violation (coverage, claimant message) is a task-fit fail even if the words appear in a cited insuring agreement. That matches the labeling precedence. State it again here so the rubric cannot drift.

Write grader instructions: grade the draft the handler would see, not the draft you can tell the model "meant"; do not fix the draft in the margin and then grade your fix; if the retrieval reason was not `ok`, do not grade prose, because there should not be prose. A rubric applied to a no-source state will invent scores.

Include a disagreement example. Two graders differ by one level on usability for a draft that includes a correct rental limit plus a redundant sentence. Show how your anchors resolve it, or revise the anchors until they do. If they cannot, mark usability as a criterion that needs a second pass before it is allowed to block anything. The strategy already says rubric grading can block prose. A criterion that cannot be anchored should be informational only. Update the strategy table in a short note if you demote one.

## Components

- **Rubric.** Three criteria, three levels, anchors in fixture language.
- **Precedence.** Including the contract-probe override.
- **Grader instructions.** One page.
- **Disagreement example.** Resolved, or a demotion note.
- **Score form.** The actual row a trainer fills: item id, retrieval reason, three levels, probe fail (yes/no), comments. No overall average column. Leave it off on purpose and say why.

## Flow

1. Draft anchors before definitions. If you cannot write the `fail` example, you do not yet know the criterion.
2. Add precedence and the probe override.
3. Build the score form without an average. Notice the urge to add one, and write the sentence that resists it.
4. Run the disagreement example yourself, then with a partner if you can.
5. On day 78, grade three imaginary drafts you write to the anchors: an obvious fail, a meet, and a sneaky fail that is usable and unfaithful. If the sneaky one can score `meet` on every criterion, the anchors are too loose and you tighten them.

## Tools and stack

Markdown. The labeling guideline and the interaction contract as constraints. No judge model. A rubric that has not been applied by a person should not be handed to a model to apply at scale. That sequencing matches the eval strategy.

## Setup

1. Create `harbor-portfolio/77-rubric/rubric.md` and `score-form.md`.
2. Ban the overall average at the top of the score form so it does not creep into a column "for convenience."
3. Day 77 is anchors and precedence. Day 78 is the disagreement, the three practice grades, and any demotion.

## Deliverables

- An anchored rubric with precedence and grader instructions.
- A score form without an average.
- Three practice grades, including a sneaky fail, and a note if a criterion was demoted.

## What done looks like

A second grader can match your level on the sneaky fail using the anchors alone. Contract failures cannot be averaged into a pass. The no-source state is not scored as prose. The form a trainer fills matches the strategy's refusal of a blended score.

## Think a step ahead

Anchors written this week describe this month's bulletin style. When a new circular class enters the corpus, graders will stretch "faithfulness" to cover it. Add a rubric version and a rule: new source classes require a new `fail` anchor before graders score those items, and scores from the old rubric version cannot be compared to scores from the new one in the same table. Write `rubric-v1` on the form. The follow-on is comparability, which a team will destroy the moment the corpus grows if you have not forbidden the comparison.

## Interview angle

Read the sneaky fail and the level you gave it. Then point at the missing average column and say why it is missing.
