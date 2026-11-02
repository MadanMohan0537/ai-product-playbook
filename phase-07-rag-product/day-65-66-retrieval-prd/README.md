# Retrieval Product Requirements

**Days 65–66 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** Harbor's drafting model is only allowed to see sources a selection step has already narrowed: the Ohio personal-auto edition in force on the date of loss, and bulletins that amend it and were published on or before that date. The library is about 1,400 pages across lines and states. The pilot uses a thin slice of it. Handlers have been compensating for library gaps with personal documents and forwarded emails. Those personal stores are not a corpus you will index.

## Concept

Retrieval is a product, not a preprocessor. It has users, a corpus, a freshness promise, a behavior when nothing qualifies, and a success measure that a claims trainer can grade. A requirements document for Harbor's retrieval step says what "the right document" means, who is allowed to add one, how current "current" is, and what the handler sees when the step should return nothing. It does not choose a vector index, a chunk size, or a framework. Those are implementation choices that have to satisfy this document.

## Approach

Write the requirements for one retrieval job: given a notice's state, line of business, date of loss, and the edition records the rule layer already trusts, return the passages the drafter may see, or return an empty set with a reason code. The reason codes are part of the product:

- `no_edition_in_force` — the rule layer has no edition, and retrieval must not guess one.
- `edition_not_published` — an edition id exists and the body is not in the published corpus.
- `bulletin_missing` — the catalog says a bulletin applies and the body is not published.
- `ok` — one or more passages, each with edition id or bulletin id, effective dates, and a passage locator a human can open.

Each code has a handler-visible sentence and a log event. Empty is a successful call when the honest result is empty. A requirements document that only specifies the happy passage list will be implemented as "always return the nearest paragraph."

Write success measures the trainer can apply without a model: on a set of notices with known correct ids, the returned set contains the required ids and contains no id from the wrong state or the wrong line. You will design the question set itself on days 69–70. Here you write the measure and the bar you would hold a pilot to, in words, and you note that the bar is unmeasured until that set exists.

Write non-goals. Retrieving from the open web, searching a handler's desktop, answering a question that has no notice context, and selecting an edition when the rule layer abstained are non-goals. State the non-goal that will be requested first ("just let it search all of SharePoint") and the response, which points back at the reason codes.

## Components

- **Job statement.** Inputs, outputs, reason codes, and the user who sees each output.
- **Corpus boundary.** What is in the pilot corpus, by named class (Ohio personal-auto forms in force for the pilot window, structured bulletins for those forms). What is out (other states, commercial, email inboxes, handler desktops, the web).
- **Freshness promise.** The maximum age of the published set relative to a bulletin email, during the pilot, and the behavior when the promise is broken. Tie this to a content owner from the milestone map. If the owner cannot meet the promise, the requirement is the `bulletin_missing` path, not a quiet staleness.
- **Success and bar.** The trainer's check, the bar, and the "unmeasured" stamp.
- **Requirement non-goals and the first request you will refuse.**

## Flow

1. Write reason codes before you write any requirement that assumes a passage exists.
2. Define the corpus boundary as classes of documents, not as a folder path. Paths change. Classes are the contract.
3. Set the freshness promise in hours or business days, with the behavior on breach.
4. Write the success check in trainer language and stamp it unmeasured.
5. On day 66, read the document as an engineer looking for permission to "return the top three anyway" on an empty result. Close every sentence that grants that permission. Then read it as the content owner and underline the promise you are making about their weekend. Adjust the promise if a weekend bulletin would make you liars by Monday.

## Tools and stack

Markdown. The approach decision and the interaction contract are inputs. No retrieval library, no embeddings tutorial, and no index. This is the spec those things would be accepted against.

## Setup

1. Create `harbor-portfolio/65-retrieval-prd/prd.md`.
2. Start from the reason codes. If you start from a user story about "powerful search," delete the first page and start again.
3. Day 65 is job, codes, and corpus boundary. Day 66 is freshness, the bar, the refusal, and the two-role read.

## Deliverables

- A retrieval requirements document with reason codes and handler-visible sentences.
- A corpus boundary and a freshness promise with a breach behavior.
- A trainer-grade success check, stamped unmeasured, and a written refusal of unscoped search.

## What done looks like

An engineer can implement an empty result without inventing a fallback query. A content owner can see the freshness number they are being asked to hit. The success check talks about document ids and wrong-line exclusions. "Top k" does not appear as a requirement. Personal desktop files are out of the corpus in a sentence someone can point to.

## Think a step ahead

The next request will be a question that needs two hops: the edition's exclusion, and an endorsement that puts the exclusion back for a specific vehicle class. A single passage cannot be "the answer." Extend the job statement with an optional `set` output: an ordered pair of passages plus a note that the drafter must not answer from only one of them when the catalog says both apply. Write the handler-visible behavior when the second passage is missing (`bulletin_missing` is close; decide whether endorsement-missing is the same code or a new one, and why). The follow-on is multi-document completeness, which a single-hit search requirement will silently drop.

## Interview angle

Explain empty-as-success and the freshness breach behavior. Retrieval requirements are about what the product does when the library is not ready.
