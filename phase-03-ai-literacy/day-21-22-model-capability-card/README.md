# Model Capability Card

**Days 21–22 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. The pilot job is to propose note text with citations to the form in force on the date of loss and the bulletin that amends it. Harbor does not decide coverage, set reserves, or message the claimant. Handle time today is about 26 minutes, of which about 9 are search.

## Concept

A capability card is a product document that says what class of model could do this job, what it costs in latency and money at the shape of the job, and which failure modes are properties of the class rather than bugs you can ticket away. It is how a PM talks about models with engineering and with a vendor without pretending to have trained one.

You will write one card with three columns: a small instruction-following model, a larger general model, and a model with a long context window that could, in theory, be handed a whole form. The columns are classes. You may name current public model families as examples, with the date you checked, and you must keep the conclusion attached to the class properties (context length, tool use, price band, citation behavior) so the card survives the next model release.

## Approach

Evaluate the classes against Harbor's job, decomposed into moves:

- Select the edition in force on a given date of loss.
- Locate a paragraph and the bulletin that amends it.
- Draft note text that stays inside the cited lines.
- Decline when the published set has no supporting line.
- Stay inside a latency budget that does not erase the 9 minutes you are trying to return.

For each move, write "fits," "fits only with a tool or a retrieval step," or "unreliable for this move," plus the reason. A long context window is not automatically a fit for edition selection. A window that can swallow a form can still quote an edition that was not in force, because the date rule is a fact about the policy record, not a fact hidden in prose. Put that distinction on the card in your own words.

Include a failure-mode row that is about the product, not the benchmark: fluent text with a citation that does not support the sentence; a refusal on a question the library does answer; a draft that slides from summary into coverage language.

## Components

- **Job moves.** The five moves above, possibly revised, each in one line.
- **Class columns.** Three classes, with an example name and the date you read its public docs, or "example unnamed" if you stay at the class level.
- **Fit table.** Move by class, using the three fit labels.
- **Latency and cost band.** A rough per-draft range you compute from public price sheets: input size you assume, output size you assume, and the resulting cents per draft. Show the arithmetic.
- **Failure modes that survive a smarter model.** At least three, and why a higher benchmark score would not retire them.
- **Recommendation.** Which class you would pilot, and which move you would not ask the model to perform even on that class.

## Flow

1. Write the job moves from the service blueprint. Cut any move that is really a human decision.
2. Read one public price page and one public context-length note. Record the date.
3. Fill the fit table. Force every cell to one of the three labels.
4. Do the cents-per-draft arithmetic in the open, with assumed token counts you state.
5. On day 22, write the recommendation and have a colleague try to move you to a different column. Note the argument that was hardest to answer.

## Tools and stack

Markdown, a calculator or a small spreadsheet, and public vendor documentation. No API key is required. If you do call a model, you are outside this project; the card is a decision document, and a demo is easy to confuse with a fit.

## Setup

1. Create `harbor-portfolio/21-capability-card/card.md` and `arithmetic.md`.
2. Pick a date and freeze the public pages you cite.
3. Day 21 is moves, sources, and the fit table. Day 22 is cost arithmetic, failure modes, and the recommendation.

## Deliverables

- A capability card a tech lead can argue with.
- Visible arithmetic for cost per draft.
- A recommendation that names a move the model will not own.

## What done looks like

The fit table uses the three labels and no "it depends" without a condition. The cost figure can be recomputed from the assumptions. The recommendation survives the question "what if the next model is better?" because the failure modes are tied to the job, not to a leaderboard.

## Think a step ahead

Vendors will offer a fine-tune or a "claims model" as a fourth column. Add a row that says what evidence would make a fourth column worth a pilot: which move it improves, against which fixture, at which cost delta, and who owns the evaluation when the vendor's number and yours disagree. Days 75–76 are where that evidence plan becomes an eval strategy.

## Interview angle

Walk through one cell you marked "fits only with retrieval" and the arithmetic under the recommendation. Class judgment plus cost is the literacy a PM is hired for.
