# Human Feedback Pipeline

**Days 87–88 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** Handlers edit Harbor drafts, discard them, and occasionally tell the Columbus manager that a citation was wrong. Those acts are feedback. Someone will propose to "just train on the edits." The edits sit in Lumen notes and in Harbor logs that, by your tracking plan, do not contain note text. A pipeline that turns feedback into an evaluation item or a training row has to cross that boundary on purpose, with a reason, a consent or employment basis you do not invent, and a place where bad rows are rejected.

## Concept

A feedback pipeline brief describes the path from a human act to a reviewed dataset: which acts are eligible, what is stripped, who reviews, what the dataset is allowed to be used for, and which uses are forbidden until a named approval exists. It is a product and data-rights document with a flow a data partner could implement. It is not the implementation. The point is to make the forbidden shortcut visible. The shortcut here is copying committed notes into a fine-tuning file because they are "high quality by definition." A committed note can contain a wrong limit the handler trusted. Commitment is not a label.

## Approach

Define three eligible acts and one ineligible act.

Eligible:

- **Citation defect report.** A handler or supervisor flags a citation. The row may contain the citation id, the notice id, the expected id if the supervisor knows it, and a reason. It may not contain the claimant's loss narrative.
- **Discard after a shown draft.** Eligible as a negative signal that the draft was not wanted. It is not eligible as a label of why, unless the handler picks a reason from a short list (`wrong source`, `too slow`, `easier to type`, `out of job`). Free-text reasons are out until legal reviews the field, because handlers will paste claim facts into a free-text box.
- **Structured edit distance bucket.** You already log `edit_size` as coarse. That bucket may be used as an eval slice. The edited text itself may not enter a training set in this pilot.

Ineligible:

- **Committed note body as a positive training example.** Forbidden in the pilot. The brief says what would have to be true to reopen it: a reviewed sample, a labeling pass against the guideline, a data-rights row closed in writing, and a use limited to evaluation before any training use is even discussed.

Write the path for an eligible citation-defect report:

1. Capture. The flag action on the citation panel, with the fields above.
2. Strip. Drop free text that is not on the allow-list. Log that stripping happened, not the dropped text.
3. Route. Content analyst queue, not an automatic set update.
4. Review. Analyst marks `accept as golden candidate`, `reject`, or `incident`. Accept does not edit the golden set by itself. It opens a charter change, with a new id, under the set owner.
5. Store. A reviewed-candidate table, versioned, separate from the gating set and separate from any training bucket.
6. Use. Evaluation candidates only. A training-use flag exists on the row and defaults to `no`. Changing it to `yes` is a principle-level decision, not a pipeline setting.

Write retention. Candidate rows live for the pilot plus a stated period you choose and can defend (for example, one quarter after the pilot decision), then expire unless they were promoted into a versioned set. Promoted rows follow the set's charter, not the feedback retention clock.

Write the failure of the pipeline itself. Duplicate flags on the same citation must not become two golden rows. A flag from a usability-test session must not enter the pilot queue. The wizard-week stream and the production stream stay apart, which the tracking plan already required; the pipeline brief repeats it because pipelines are where that promise usually dies.

## Components

- **Act inventory.** Eligible and ineligible, with the reopen conditions for the ineligible act.
- **Stage flow.** Capture, strip, route, review, store, use. A diagram in mermaid or a numbered list.
- **Field allow-list.** What a candidate row may contain.
- **Promotion rule.** How a candidate becomes a golden-set proposal without bypassing the charter.
- **Retention and separation.** Clocks, and the ban on mixing wizard-week with production.

## Flow

1. List the human acts that already exist in the product before you invent a new "thumbs" button. Add a control only if an eligible act cannot be captured otherwise. The citation flag may be new; justify it.
2. Write the ineligible act and its reopen gate first, so the rest of the brief cannot quietly route around it.
3. Specify stages and the field allow-list. If a stage has no owner, it is not a stage.
4. Write retention and the duplicate rule.
5. On day 88, walk one fictional flag through every stage and write the row as it appears after stripping. Then try to walk a committed note body through the same stages and show the stage that stops it. If no stage stops it, add the stop.

## Tools and stack

Markdown and a simple flow diagram. No pipeline framework, no label studio, and no training job. A data partner should be able to estimate the work from the brief. A model trainer should be able to see that there is nothing for them to train on yet, and why.

## Setup

1. Create `harbor-portfolio/87-feedback-pipeline/brief.md`.
2. Draw the six stages before writing prose, and keep the ineligible act on the same page.
3. Day 87 is acts, fields, and stages. Day 88 is retention, the two walkthroughs, and any stop you had to add.

## Deliverables

- A pipeline brief with eligible and ineligible acts.
- A stage flow, a field allow-list, and a promotion rule into the charter.
- Two walkthroughs: one flag that survives as a candidate, one note body that is stopped, with the stopping stage named.

## What done looks like

A committed note cannot become a training row by configuration. A citation flag can become a golden-set proposal only through a human and a new id. Free text of the loss is not on the allow-list. Wizard-week events are excluded. Retention has a clock. The reopen conditions for training use are stricter than "the model team is ready."

## Think a step ahead

Edits that are too sensitive to store may still be useful as preference pairs: the draft versus the handler's revision, with claim facts removed. That use is more dangerous than a citation flag, not less, because the revision is the note. Add a blocked design, written so a future team cannot claim you never considered it. Describe the pair, the minimum redaction (loss narrative, names, policy numbers, vehicle identifiers), the residual risk that a rare fact pattern still identifies a claimant, and the decision: not in this pilot, reopen only with counsel and a redaction review on a sample. The follow-on names the temptation precisely enough that "anonymous edits" cannot sneak through as a synonym.

## Interview angle

Name the stage that stops a committed note from becoming training data, and the reopen conditions. The pipeline is the refusal as much as the flow.
