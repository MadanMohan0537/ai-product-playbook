# Platform versus Feature Bet

**Days 95–96 · Phase 10, Advanced Bets · Advanced**

**Case.** Harbor works, narrowly, for Ohio personal-auto notices in Columbus. Two proposals arrive the same week. Proposal F: deepen the feature — glass-only handling, the partial-support flow, the commit-time corpus check — for this office, through the end of the quarter. Proposal P: extract a "Northline knowledge platform" so any team can register a corpus and get drafts with citations, starting with homeowners in another state. The platform proposal has a senior sponsor. The feature proposal has the Columbus manager. You have to write the bet, not split the difference in a way that funds neither.

## Concept

A platform-versus-feature bet is a decision record about where reuse is real and where reuse is a way to avoid finishing the job. Shared retrieval, a citation schema, and an eval harness can be platforms. "The Harbor model" cannot, because the model card, the corpus policy, and the principles are use-specific. This project writes the options, the kill criteria, the sequencing, and the chargeback question the platform will face the moment a second team wants it to be free.

## Approach

Write three options, not two. The third is the one organizations actually do and then forget they chose.

- **Option F, feature depth.** One line, one state, one office, through a dated decision to expand, hold, or stop. Platform work is limited to whatever the feature needs to meet its own gates (the publishing pipeline, the golden set, the harness brief).
- **Option P, platform first.** A shared corpus registry, citation schema, and runner, with Harbor as the first tenant and homeowners as a committed second tenant on a date. Feature depth waits.
- **Option D, declared sequence.** Feature depth until a named gate is passed, then a platform slice that is only the parts a second tenant would have to duplicate unchanged. Homeowners is not a committed tenant. It is a candidate that must pass the reuse gate you wrote on the principles project: intended reader, who the author is, what the model must not decide, and which principle would change.

For each option, write cost in the only currencies the pilot has: content-analyst hours, trainer hours, engineering weeks, and the risk to the Columbus guardrail. Do not invent a dollar ROI. You may point at the unit-economics sheet and say which assumption would have to be true for option P to pay for itself inside two quarters, and mark that assumption as untested.

Kill criteria, written so they can fire:

- F dies if the citation guardrail is in veto and the team is still adding scope. The response is restriction or pause, not a platform.
- P dies if the second tenant cannot name an author of record and a corpus owner before the registry is built. A registry without a second owner is a feature with extra layers.
- D dies if the "unchanged parts" list is empty after you write it. Then there is no platform slice, and pretending otherwise is option P without the honesty.

Write the unchanged-parts test. List the Harbor assets a homeowners team could adopt without editing the rule: the harness report schema, the deletion tree, the analytics-trust checklist shape. Then list the assets they must not adopt unchanged: the precedence rules, the golden set, the disclosure copy, the model card's jurisdiction block. If the second list is the long one, say so. That is evidence about how large the platform is.

Chargeback, because option P and the platform slice of D will be asked to be free. Write a one-page rule: a tenant pays in content-analyst time for their own corpus and their own set, and the platform team does not accept a tenant who arrives with only a model request. The payment is capacity, not an internal invoice, unless the company already has a chargeback system, in which case you name the unit (analyst hours, indexed documents) and refuse to charge per draft in a way that incentivizes hiding usage.

## Components

- **Option briefs.** F, P, and D, each half a page, with the hours and the guardrail risk.
- **Kill criteria.** One per option, observable.
- **Unchanged-parts list.** Adopt unchanged versus must rewrite, drawn from real artifacts in this playbook.
- **Chargeback rule.** What a second tenant must bring, and the request you will refuse (a model, no corpus owner).
- **Recommendation.** One option, the date you will review the kill criterion, and the sponsor sentence.

## Flow

1. Write the unchanged-parts list before the recommendation. It is the evidence, and writing the recommendation first will bias the list.
2. Draft the three options at the same length. A straw man is a way of not deciding.
3. Write kill criteria that could actually fire this quarter.
4. Choose. The sponsor sentence is what you will say to the senior sponsor if you did not choose their option, and it has to contain the kill criterion.
5. On day 96, ask a partner to argue for the option you rejected. If their best point is absent from your brief, add it, and see whether the recommendation still stands. Record the point either way.

## Tools and stack

Markdown. The model card, principles, corpus policy, and harness brief as the evidence for what is reusable. No architecture tooling. A platform bet at this stage is a scope decision. A system diagram can come after the option is chosen, and it is out of scope here.

## Setup

1. Create `harbor-portfolio/95-platform-bet/bet.md`.
2. Build the unchanged-parts list from documents you actually wrote, cited by name.
3. Day 95 is the list and the three options. Day 96 is kill criteria, chargeback, the recommendation, and the partner argument.

## Deliverables

- Three option briefs at comparable depth.
- An unchanged-parts list tied to real artifacts.
- A recommendation, kill criteria, a chargeback rule, and a note from the partner argument.

## What done looks like

The recommendation names what will not be built this quarter. The second tenant cannot arrive with only a request for "the Harbor model." Kill criteria are observable. The sponsor sentence contains the criterion, not a compliment. The unchanged-parts list is longer on the rewrite side if that is the truth, and you did not hide that to make a platform sound bigger.

## Think a step ahead

If option D or P survives, the second tenant's failure mode is using Harbor's screen for a different decision, such as a claimant-visible homeowners answer, while the registry still says "citation platform." Extend the chargeback rule with a use-review: every tenant's intended reader and author of record are re-certified when their traffic or their disclosure changes, and a tenant who cannot pass the re-certification loses retrieval access until they do. Write the trigger and the access consequence. The follow-on is how a platform stays narrow after it has customers, which is the problem a launch bet never feels yet.

## Interview angle

Give the recommendation and the kill criterion in the same breath. Then one asset a second team must rewrite. That is the bet.
