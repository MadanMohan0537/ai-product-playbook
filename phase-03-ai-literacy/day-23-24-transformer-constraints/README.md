# Transformer Constraints on the Product

**Days 23–24 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor drafts a claims note and shows citations. The handler signs the note. The sources are policy forms and bulletins, some of them long, some of them amended by a later bulletin that is a separate document. Harbor does not decide coverage.

## Concept

A transformer is the model architecture behind most products a PM now ships. You do not need to implement one. You do need a mental model that is accurate enough to make product decisions: what the model can look at while it writes the next word, why a long document is not the same thing as a remembered document, why a citation can be fluent and unfaithful, and which of those facts are constraints on Harbor's interface.

This project turns that mental model into a constraint backlog: product requirements that exist because of how these models work, written so a designer and an engineer can accept them without a math lecture.

## Approach

Write a two-page explanation in product language, aimed at Harbor's designer. Cover these mechanisms and stop before you copy a textbook:

- **Tokens.** The unit the model reads and writes. A policy clause and a form code may tokenize in ways that make exact codes fragile. The product implication is to pass codes as structured fields when you have them, and to show the handler the code you retrieved, not only the sentence the model wrote.
- **Context window.** The working space for one request. Anything outside it is invisible unless a retrieval step or a tool brings it in. The product implication is a designed behavior when the form plus the bulletin plus the claim facts do not fit, or when someone is tempted to paste the entire 1,400-page library.
- **Attention, in one paragraph.** While predicting the next token, the model weights the tokens it can see. It does not look up "the edition in force" as a database would, unless you give it that fact. The product implication is that edition selection is a query against the policy record, and the model's job starts after that fact is known.
- **Next-token generation.** The draft is a continuation, not a retrieved paragraph. It can sound like the form while saying a limit the form does not state. The product implication is that every drafted sentence the handler might rely on needs a citation path the handler can open, and a no-source state when there is nothing to open.
- **Sampling.** The same prompt can yield different drafts. The product implication is that "regenerate" changes the text under an already-reviewed paragraph, so the interface must not silently regenerate a section the handler has edited.

Check your explanation against a failure you can tell in plain language: Harbor quotes a rental limit from the November form on a March loss, in prose that sounds exactly like the February form. Say which mechanism made that easy.

## Components

- **Mechanism notes.** The five above, each in a short paragraph that ends with a Harbor implication.
- **Constraint backlog.** Eight to twelve items in the form "Because \[mechanism\], the product must \[behavior\], which we will see in \[artifact\]."
- **What this does not mean.** Three misconceptions you will stop using in meetings. Write the replacement sentence. Example misconception: "a bigger context window means we can drop retrieval." Replacement: a window is still a single request's working space, and edition-in-force is a record fact.
- **Question list for engineering.** Five questions that are fair for a PM to ask, such as where the edition-in-force fact is bound before generation, and what the token budget is for the draft call.

## Flow

1. Draft the mechanism notes from memory first, then correct them against a reliable public source. Cite the source and the date. Correcting your own first draft is part of the project.
2. Turn each note into backlog items. If an item does not change a behavior a handler could notice, or a fact engineering must bind, cut it.
3. Write the misconception list from phrases you have actually heard or used.
4. On day 24, walk the backlog against the wizard-of-oz screen. Mark which constraints your screen already meets and which are new.

## Tools and stack

Markdown, plus one or two public references (a model provider's guide to context windows, or a careful survey article). No training run, no notebook of matrix multiplies, and no framework tutorial. Those belong in a build curriculum. This artifact is the product backlog those constraints imply.

## Setup

1. Create `harbor-portfolio/23-transformer-constraints/explanation.md` and `backlog.md`.
2. Timebox the first draft to 45 minutes before you open a reference, so you can see what you had wrong.
3. Day 23 is mechanisms and corrections. Day 24 is the backlog, the misconceptions, and the screen check.

## Deliverables

- A two-page explanation a designer will actually read.
- A constraint backlog of eight to twelve items.
- A misconception list and five engineering questions.

## What done looks like

A designer can point at a screen region that exists because of a constraint on the list. An engineer can see which facts must be bound before generation. The explanation does not include a formula, and it does not contain a false claim you left in after the correction pass. Your first-draft mistakes are fixed, not published.

## Think a step ahead

Context windows and prices will change this year. Separate the backlog into items that survive a cheaper, longer context (authorship, no-source state, regenerate-destroys-edits) and items that are about today's limits (what fits in one call). Add a review date and the single public number that would make you retire an item. A constraint backlog that cannot expire will clog the roadmap after it stops being true.

## Interview angle

Explain edition-in-force as a fact the model should be given, not a fact it should recall from a PDF. Then show two backlog items that follow from that sentence.
