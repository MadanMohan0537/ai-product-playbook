# Retrieval Failure Postmortem

**Days 73–74 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** In week 6 of the limited pilot, a Columbus handler committed a note for an Ohio personal-auto notice. The draft cited a rental limit of $40 per day from a document titled "PP 00 01." The document was a commercial-auto form that shared a short title with the personal-auto form. The handler opened the citation, saw familiar rental language, and committed. A supervisor caught it two days later because the form code prefix was wrong. No claimant decision had been sent. The limit on the correct personal-auto form, as amended, was $30. This postmortem is fictional and is the practice case.

## Concept

A postmortem after a bad citation is a product review of how several layers agreed to be wrong together: corpus boundary, retrieval, citation display, handler training, and the commit step. Its output is a set of changes to requirements, specs, and gates, with owners and dates. A narrative that ends in "the model hallucinated" is not finished, and in this scenario it is also inaccurate. The commercial form was a real document. It was the wrong document. That distinction changes the fix.

## Approach

Write the postmortem in a structure a claims organization can accept:

- **Facts.** Timeline from retrieval to supervisor catch, using only the scenario above plus behaviors you already specified. When you need a fact the scenario does not give (how the commercial form entered the index), write it as an unknown and list the question, rather than inventing a comforting cause.
- **Impact.** What reached the file, what did not (no claimant message), and what the residual risk is (the note is still in Lumen until someone corrects it).
- **What each layer allowed.** Corpus policy, reason codes, citation schema, answer experience, training, commit. For each, say whether the layer behaved as specified and the spec was weak, or the implementation violated the spec. You do not have an implementation; do this as "if we had built exactly the specs so far, would this have been possible?" That question is the value of the exercise. For example, your corpus boundary excluded commercial forms. A retrieval that returned one means either the spec was not testable, or this scenario assumes a violation. Pick the reading that matches your actual documents, and if your golden set's two wrong-line items would have caught a commercial form only when the notice was commercial, say that. The hole may be "a commercial form returned on a personal notice," which your set might already cover. Look at your rows. If it covers them, the postmortem's question becomes detection speed and the handler's ability to see the prefix, not set coverage.
- **Detection.** The supervisor caught it in the ordinary sample. The product did not catch it. Write the detection gap in one sentence.
- **Actions.** Each action changes a spec, a golden-set row, a citation field, a training line, or a gate. Each has an owner and a date inside the remaining pilot, or an explicit "next pilot" mark. Include the correction of the committed note as an operational action, not only a product action.
- **What we are not doing.** A model retrain as the primary action, unless your layer analysis says the drafter invented the $40 rather than quoting the wrong real form. In this scenario it quoted a real form. Write the refusal.

Use the incident addendum from the comms system for the hour-of note, and check that the postmortem's facts match the note a handler would have been sent. If the addendum's handler sentence is wrong for this incident ("stop using Harbor" versus "open the form prefix before you commit"), revise the sentence and record the revision. The postmortem that does not update the incident copy leaves the next incident on the old words.

## Components

- **Timeline and unknowns.**
- **Layer analysis.** Spec-weak versus spec-violated, for each layer, grounded in your documents.
- **Action list.** Owner, date, artifact changed. Include the file correction.
- **Refusal.** The primary action you will not take, and why.
- **Comms revision.** The handler sentence, updated if needed.

## Flow

1. Write the timeline. Mark unknowns in a separate list so they do not become fake facts by the last page.
2. Walk each spec. Quote the line that would have prevented the miss, or write that there is no such line.
3. Draft actions from the holes only. An action that does not cite a hole is extra credit the pilot cannot afford.
4. Write the refusal and the file-correction action.
5. On day 74, read the postmortem next to the golden set. Add or retire a row if the set would still pass while this bug lives. Record the row id.

## Tools and stack

Markdown. Your own earlier specs as the system under review. No log platform. The discipline is holding the scenario against the documents you wrote.

## Setup

1. Create `harbor-portfolio/73-postmortem/postmortem.md`.
2. Have the corpus policy, golden-set rules, and answer-experience states available.
3. Day 73 is timeline, layers, and unknowns. Day 74 is actions, the refusal, the comms revision, and the golden-set edit.

## Deliverables

- A postmortem with unknowns separated from facts.
- Layer analysis quoting your specs.
- Actions with owners, a refused action, a comms revision if needed, and any golden-set row change.

## What done looks like

The write-up does not blame "hallucination" for a wrong real document. At least one action changes a spec or a test row, not only a prompt. The committed note has a correction action. Unknowns are listed. A reader can see whether the specs you have today would have made the incident possible.

## Think a step ahead

The commercial form was the wrong product in the right company. The next incident is the right product in the wrong tenancy: a passage from another carrier's form, or another Northline customer's policy packet, retrieved because it was embedded in a shared index. Write the product requirement that would make that incident a failed gate rather than a surprise. Passages must carry a tenant and a corpus-class marker, retrieval must filter on both before any passage reaches the drafter, and a golden-set row must try to retrieve across that boundary and expect zero hits. State the pilot behavior if the marker is missing on even one document: that document is not retrievable, and the reason is logged. The follow-on is isolation, which content similarity will never give you.

## Interview angle

Tell the story in four sentences ending in the action that changes a test, not a prompt. The refused retrain is the judgment.
