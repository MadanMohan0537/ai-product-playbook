# Answer Experience and Human Handoff

**Days 71–72 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** A Harbor handler sees a draft only when retrieval returned `ok`. They see a reason sentence when it did not. Some notices are only partly supported: the edition is published, the bulletin that amends one limit is not. The handler can always abandon Harbor and write the note in Lumen. That path is the handoff, and it has to be designed with the same care as the draft, because it is what careful handlers will use on the worst files.

## Concept

The answer experience is everything after retrieval returns: which passages are shown, how partial support is described, how the handler edits, and how the work moves to a person, a queue, or the plain Lumen note when the product should get out of the way. Handoff is not a failure message. It is a destination, with the context the next step needs so the handler does not re-search from scratch.

This project specifies that experience for Harbor, including copy, and the rule for when a partial answer is more dangerous than silence.

## Approach

Specify four states. For each, write the layout in words, the exact copy, the actions, and what is logged.

1. **Full support.** Every sentence in the draft has a displayable citation under the precedence rules. The handler can edit, open a citation, discard, or commit. Commit records author, draft version, and citation ids available.
2. **Partial support.** The edition is citable and a required bulletin is not published. Default action: do not draft the limit that the bulletin would have amended, and do not draft a cheerful partial note that omits the limit. Show the edition citation, the `bulletin_missing` sentence, and a single primary action: "Write the note in Lumen," with the edition id copied to the clipboard or inserted as a source line the handler asked for. Justify this default against the alternative, which is a draft that is faithful to an incomplete corpus and therefore wrong in the file.
3. **No support.** Reason sentence, no passages, same primary action. Do not show "related" documents from another line.
4. **Out of job.** The handler asked for coverage or a claimant message. Decline copy from the interaction contract, and leave any in-job draft request usable if it was a second sentence. This is the fix for error-analysis item 13, where a combined message lost the note entirely. Specify how the interface separates the two asks.

Handoff details matter. "Write the note in Lumen" should land the handler in the note with the notice context intact, not at a home screen. If the integration cannot do that in the pilot, the spec says what the handler sees instead, and that gap is a named limitation on the model card's oversight section. Update the card's limitation list in a short addendum here; do not pretend the deep link exists.

Write the partial-answer danger rule as a principle the team can reuse: if the missing source would change a number or a prohibition in the note, suppress the draft. If the missing source is a page locator only, and the span text is in the corpus, the draft may proceed with the locator flagged. Item 19 in the error analysis (wrong page, right span) is the second case. The rental limit is the first.

## Components

- **State specs.** Four states, copy included, actions included, logs included.
- **Handoff destination.** Where the handler lands, and the pilot limitation if the destination is weaker than you want.
- **Partial-answer rule.** The number-or-prohibition test, with the rental example and the page-locator example.
- **Combined-ask behavior.** How out-of-job and in-job requests in one message are separated.
- **Card addendum.** The limitation you added, in two or three sentences, ready to paste into the model card.

## Flow

1. Start with partial support. It is the state teams design last and handlers hit on bad weeks.
2. Write copy in handler language. Read it against Priya's failure line. If the copy could be pasted into the note as if it were a coverage statement, rewrite it.
3. Specify handoff destination and the pilot limitation honestly.
4. Write the combined-ask behavior and test it against a single text box, because that is the interface you are likely to have.
5. On day 72, take the twenty error-analysis items and assign each to a state or to "should never reach the handler." Any item that has no state is a hole in this spec. Close the hole or name the earlier project that must close it.

## Tools and stack

Markdown, plus copy you are willing to show a handler. No front-end build is required. A wireframe image is optional; the words and the rules are the spec. If you draw a wireframe, the copy on it must match the document exactly.

## Setup

1. Create `harbor-portfolio/71-answer-ux/states.md`.
2. Keep the reason codes and the precedence rules open while you write copy.
3. Day 71 is the four states and the partial-answer rule. Day 72 is handoff, combined-ask, the card addendum, and the error-item mapping.

## Deliverables

- State specs with copy, actions, and logs.
- A partial-answer rule with two contrasting examples.
- A mapping from the twenty error items to states, and a model-card addendum.

## What done looks like

Partial support does not draft the unamended rental limit. The no-support state shows no "related" commercial form. A combined coverage question and note request still allows the note. Every error-analysis item has a state or a named upstream fix. The disclosure and the new copy do not conflict.

## Think a step ahead

Handlers will ask for a side-by-side of "what I would have written" and the draft, once they trust the tool enough to argue with it. That view is a different product surface: it needs their in-progress Lumen text, which may contain claimant details your RAID log forbids sending to a vendor. Specify the comparison as a local view that never leaves the workstation: both texts rendered on the client, no new model call, no logging of the note body to the analytics stream. Write what you will refuse (a cloud "diff explanation" that uploads the note). The follow-on is a useful surface that would quietly break the data-rights row if you built the obvious version.

## Interview angle

Read the partial-support copy and the reason a faithful-but-incomplete draft is worse than silence. Then mention the combined-ask fix. Experience design here is a safety choice.
