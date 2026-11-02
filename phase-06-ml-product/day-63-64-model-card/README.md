# Model Card and In-Product Disclosure

**Days 63–64 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Harbor is about to enter a limited pilot. Two different things need a plain-language description of their limits. The drafting behavior is a language model bounded by the interaction contract and by sources the rule layer selected. The audit-priority score, if you chose to pilot it, is a separate model with a different decision. They do not share a card. This project writes the drafting card and the handler-facing disclosure. The score, if it exists, gets a stub that says it is a different card and names the decision it touches.

## Concept

A model card is the document a new teammate, an auditor, or a future you can read to learn what the system is for, what it is not for, what data it sees, how it fails, and who is accountable when it fails. An in-product disclosure is the few lines a handler actually sees, which have to be true to the card and short enough to be read during training. Cards that exist only in a repository, and disclosures that say "AI may be inaccurate" without saying what the handler remains responsible for, are both incomplete. You will write both so they agree.

## Approach

Write the drafting card with these sections, filled for Harbor rather than copied as empty headings:

- **Intended use.** Propose note text and citations for new Ohio personal-auto physical-damage notices, for a handler who will edit and commit under their own name.
- **Out of scope.** Coverage determinations, reserves, claimant communications, other lines of business, other states, unattended commit, and any use of discarded draft text as if it were the file.
- **Users and affected people.** Handler, supervisor, claimant (indirectly, through delay or a wrong rental limit), and later readers of the file.
- **Inputs.** Which fields and which retrieved spans, at the level of the feature and corpus specs. Name what must not be in the prompt, from the RAID log (for example, a loss description, if that row is still red).
- **Performance evidence.** Point at the error-analysis fixture and the eval bar if you have one. Do not invent a percent. If the only evidence is a 40-draft shadow review, the card says that, with the date and the population.
- **Failure modes.** The cause groups you are willing to stand behind: wrong edition when both texts are shown, missing bulletin, out-of-job coverage sentence, wrong library.
- **Human oversight.** The commit step, what it does and does not prove, from the interaction contract.
- **Ethical and file-integrity considerations.** A wrong limit in a signed note can follow a claimant into a rental dispute. Say that in a sentence. Say that handler identity is not a model feature in the audit score, if you discuss the score at all.
- **Owners.** Product owns the intended use. Content operations owns source freshness. Engineering owns the boundary that keeps edition selection on the rule. Legal owns the reliance boundary.

The disclosure, shown in handler training and linked from the draft panel, is under 120 words. It covers: drafts are proposals, you are the author, citations have to be opened because commit does not check them for you, what the tool will refuse, and how to report a bad citation. It does not say "powered by" a vendor as a substitute for those points.

Write a disagreement test. Place the card and the disclosure side by side and list every promise in the disclosure. Each one must appear, in substance, in the card. Then list every out-of-scope item in the card and decide whether the disclosure must carry it. Coverage and claimant messaging must. The full failure taxonomy must not; the disclosure would become the card and would not be read.

## Components

- **Drafting model card.** The sections above, filled, one to three pages.
- **Audit-score stub.** Five lines: different system, different decision, card not written, do not cite the drafting evidence as if it applied.
- **Disclosure copy.** Under 120 words, plus where it appears (training, and a persistent link on the draft panel, not a one-time modal that never returns).
- **Disagreement test.** A two-column check, completed.
- **Update rule.** What changes force a card revision during the pilot: a new intended use, a new input class, a vendor version change, or a failure mode found in the monthly sample that the card does not list.

## Flow

1. Fill intended use and out of scope from the interaction contract and the principles. If you drift, stop and reconcile.
2. Write performance evidence last, after you have decided which studies are real. Invent nothing.
3. Draft the disclosure from the card, then cut it to 120 words without losing authorship and refusal.
4. Run the disagreement test and fix whichever side is wrong.
5. On day 64, read the disclosure aloud at a normal pace. If it takes more than a minute, it is still a card. Cut again.

## Tools and stack

Markdown. Source documents from earlier projects, cited by name. No card generator and no model call. The writing is the accountability exercise.

## Setup

1. Create `harbor-portfolio/63-model-card/card.md` and `disclosure.md`.
2. Start a "do not invent metrics" note at the top and delete it only when you have checked the performance section against the fixtures you actually have.
3. Day 63 is the card and the stub. Day 64 is the disclosure, the disagreement test, and the read-aloud.

## Deliverables

- A filled drafting model card.
- A separate stub for the audit score.
- Disclosure copy, a completed disagreement test, and an update rule.

## What done looks like

The performance section matches a real fixture, including its small size. The disclosure names the handler as author and names two refusals. The disagreement test has been filled, not described. The audit score cannot borrow the drafting card. A reader can find an owner for source freshness.

## Think a step ahead

A card written for Ohio personal auto will be attached, by someone helpful, to a Michigan pilot that reuses the screen. Add a jurisdiction block: the card names the state and the form family, and the product must show the handler a "not in the card's intended use" state when the notice's governing state or line differs. Write the exact state and the log event. Reuse without that state is how a careful card becomes cover for a careless rollout. The platform bet on days 95–96 will try to make reuse easy; this block is the brake.

## Interview angle

Read the disclosure, then one failure mode the disclosure deliberately leaves out, and say where a teammate would find it. You are showing you know the difference between a card and a caption.
