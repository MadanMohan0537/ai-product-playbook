# Approach Decision: Rules, Classical ML, or a Language Model

**Days 53–54 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Harbor's hardest narrow subtask is not "write a helpful note." It is: given a date of loss, a policy effective window, and a set of Ohio personal-auto form editions, choose the edition that was in force, then attach any bulletin that amends that edition and was issued on or before the date of loss. A separate subtask is drafting sentences that stay inside those sources. Northline already stores edition codes and effective dates in Lumen for many policies, and the store is wrong or empty on some older notices.

## Concept

Different parts of a product want different machinery. A date comparison against a structured effective-date field is a rule. A prediction of whether a free-text loss description is glass-only might be a classical model, if you had labels and a reason to predict it. Drafting a sentence that a handler will edit is a language-model job, and only after the sources are chosen. This project writes the decision record that assigns each Harbor subtask to a kind of machinery, with the evidence that would overturn the assignment.

The record stops a team from sending an edition-selection problem to a language model because the rest of the product uses one.

## Approach

Split the pilot episode into subtasks. For each, fill a one-page decision block:

- **Input.** Structured fields, text, or both. Name the system that owns the field.
- **Output.** A class, a chosen record, or a span of text. Say whether the output must be exact.
- **Cost of a wrong output.** Tie it to the handler, the audit, or the claimant wait.
- **What "learning" would need.** Labels, their unit, who could create them, and how fast they drift (a bulletin a week is a drift rate).
- **Assigned approach.** Rule, classical model, language model, or human only.
- **Overturn condition.** The observation that would make you reopen the assignment.

Worked assignments you should pressure-test, not copy blindly:

Edition-in-force, when Lumen has effective dates: a rule. Overturn if the date fields are missing on more than a threshold of pilot notices you will set after looking at a sample, not before.
Edition-in-force, when dates are missing: human choice with both editions shown, not a model guess. Overturn if content operations can backfill dates for the Ohio personal-auto set before the pilot.
Bulletin attachment: a rule over publish dates and edition ids, once bulletins are structured. A language model reading an inbox is a different, worse product.
Sentence draft from chosen sources: a language model, with the contract's citation rules. Overturn if wizard tests show handlers accept prose they do not check; the fallback is citations with no prose.
Glass-only classification: do not build. You do not have a decision that needs the class yet. The experiment story's opt-out is a research note, not a mandate to train a classifier. Assign "not now" and write the decision that would make it real.

## Components

- **Subtask list.** The episode broken into moves a system could own.
- **Decision blocks.** One per subtask, with the six fields.
- **Boundary diagram.** Where the rule's output becomes the language model's input. This boundary is the product's actual architecture, drawn in a few boxes.
- **Overturn log.** Empty table, columns ready, plus one hypothetical row written as an example of how a future entry should look.
- **Rejection note.** The glass-only classifier, and any other tempting model, with the reason it waits.

## Flow

1. List subtasks by walking the service blueprint. Merge any two that always ship in the same component.
2. Fill decision blocks. Write the overturn condition before the assignment if you notice yourself choosing the fashionable option.
3. Draw the boundary. If the language model receives the whole library and is asked to pick the edition, the boundary is in the wrong place; move it.
4. Write the rejection note for at least one model someone on a typical team would propose.
5. On day 54, explain the boundary to an engineer and to a claims supervisor. If the supervisor cannot tell who picked the edition, the diagram is still an internal picture and you revise the words.

## Tools and stack

Markdown and a small diagram. No training run. The decision record is the deliverable. A notebook that fits a toy classifier would answer a different question than the one this pilot is stuck on.

## Setup

1. Create `harbor-portfolio/53-approach/decision.md`.
2. List subtasks before you open a model provider's site. The site is not an input to this decision.
3. Day 53 is blocks and the boundary. Day 54 is the rejection note and the two-audience explanation.

## Deliverables

- Decision blocks for each subtask, including at least one "not now."
- A boundary diagram between the rule and the language model.
- An overturn log with a hypothetical example row, and a rejection note.

## What done looks like

Edition selection is not assigned to the language model when dates exist. Every assignment has an overturn condition that names an observation. The supervisor can say, from your diagram, who or what picked the form. At least one attractive model is explicitly not now.

## Think a step ahead

The next design is a hybrid failure: the rule picks an edition, the language model drafts from it, and a second bulletin amends only one paragraph, which the rule did not represent because the bulletin was stored as a PDF. Write the degraded behavior. The draft step must not run on a partial amend when the amend is unstructured, and the handler sees "bulletin on file, not yet structured; draft withheld." Specify who structures it and the maximum age of an unstructured bulletin you will tolerate in the pilot before this state becomes a gate failure. That is the real boundary, one level down from the clean diagram.

## Interview angle

Draw the boundary and the overturn condition for edition selection. You are showing that model choice followed the subtask.
