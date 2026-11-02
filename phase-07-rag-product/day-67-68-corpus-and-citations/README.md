# Corpus Policy and Citation Behavior

**Days 67–68 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** Harbor may cite Ohio personal-auto forms and the bulletins that amend them. Two sources can both look current and disagree: a form PDF and a bulletin issued later, or two bulletins where the later one narrows the earlier one. The handler has to see enough to open the right page, and the draft has to obey a precedence rule you write down. A citation that says "source: policy" is not a citation in this product.

## Concept

Corpus policy decides which documents are allowed to support a sentence and which win when they conflict. Citation behavior decides what the handler sees, what is logged, and what the drafter is allowed to do when the winning source is missing. Together they are the product's notion of evidence. This project writes both as rules with examples, including the conflict case you sketched in the competitive teardown: a date of loss, two editions, and a bulletin that amends only the newer one.

## Approach

Write precedence in an order a content analyst can apply without a meeting:

1. The edition in force on the date of loss, as chosen by the rule layer, is the only form that may be cited.
2. A structured bulletin published on or before the date of loss, and marked as amending that edition, overrides the form where it explicitly amends it, and nowhere else.
3. A later bulletin overrides an earlier bulletin on the same point.
4. Email, desktop notes, and the handler's memory are not sources, even when they are right. The recovery is to get the bulletin structured, not to cite the inbox.
5. If the applicable bulletin is known to exist and is not structured, the draft is withheld and the reason code from the retrieval requirements is shown. The form's unamended limit is not an acceptable fallback, because it is the error Priya already gets written up for.

Write citation fields the handler can use: document title, edition id, in-force window, bulletin id and publish date if used, and a locator (section heading or page). A citation missing any of these is not displayable, and an undisplayable citation cannot support a sentence.

Write three worked conflicts as if they were fixtures:

- Bulletin amends the rental limit; the form has the old limit. The draft uses the bulletin's number and cites both, with the bulletin marked as overriding.
- Bulletin amends only the newer edition; the loss falls under the older edition. The newer bulletin is not cited.
- Two bulletins, a week apart, different rental numbers. The later one is cited as overriding, and the earlier one is visible as superseded, not silently dropped, so a supervisor can see why the number is not the one they remember.

Specify the click behavior. Opening a citation shows the locator in the published document, not a model paraphrase of it. If you cannot deep-link, the requirement is to show the exact quoted span beside the locator, copied from the corpus, not regenerated.

## Components

- **Precedence rules.** The ordered list, plus who is allowed to mark a bulletin as "amending" a given edition. That marking is a content action with a name and a second-person check for the pilot.
- **Citation schema.** Required fields, and the rule that a sentence with no displayable citation is not drafted.
- **Three conflict fixtures.** Inputs, the winning source, the citation the handler sees, and one wrong behavior that would be easy to ship.
- **Superseded-source display.** How the handler sees a source that was considered and rejected, without letting it be copied into the note by accident.
- **Corpus change control.** Who may add a document class to the pilot corpus. The default answer is nobody during the ten weeks, and the path for an exception is the same escalation rule as a principle change.

## Flow

1. Draft precedence from Priya's rental-limit error, so the rule solves a real miss and not a taxonomy exercise.
2. Write the citation schema and apply it to each conflict fixture. If a field is missing in your own example, the schema is fantasy.
3. Specify superseded-source display and the accidental-copy risk.
4. Write change control, including the refusal of desktop files.
5. On day 68, give the three fixtures to a partner and your precedence list. They apply the rules. Wherever they get a different winner, fix the rule's wording, not their reading, unless they skipped a line. Record the edit.

## Tools and stack

Markdown. Short fixture passages you write and label as fake. No document parser and no search stack. The policy has to be computable by a careful person, which is the right bar for a rule the product will automate later.

## Setup

1. Create `harbor-portfolio/67-corpus/policy.md` and `conflicts.md`.
2. Number the precedence rules. You will refer to them by number in later projects.
3. Day 67 is precedence, schema, and fixtures. Day 68 is superseded display, change control, and the partner application.

## Deliverables

- Ordered precedence rules and a named content action for "amending."
- A citation schema with a no-display, no-draft rule.
- Three conflict fixtures a partner has tried to apply, plus the wording change you made.

## What done looks like

A partner reaches the same winner on all three fixtures using the written rules. The unamended form is not a fallback when a known bulletin is unstructured. Citations have fields a supervisor could check six months later. Desktop files are refused in the change-control section.

## Think a step ahead

A state insurance department circular can bind the company without fitting the word "bulletin," and it can arrive as a PDF that amends many forms at once. Add a source class, `circular`, with a precedence position relative to form and bulletin, an owner, and a pilot decision: either circulars are in scope and the schema has a field for them, or they are out of scope and the handler sees a specific sentence ("department circulars are not in Harbor; use the compliance site"). Pick one for the ten-week pilot and write the sentence. The dangerous outcome is a silent middle, where the circular is sometimes retrieved because it was in the same folder.

## Interview angle

Walk one conflict fixture from the rule number to the citation fields. Then say what the product does when the winning bulletin is not structured. That second beat is the policy.
