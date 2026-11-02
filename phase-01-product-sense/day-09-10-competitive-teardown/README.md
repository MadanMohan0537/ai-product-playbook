# Competitive Teardown

**Days 9–10 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. The job to beat is specific: find the form in force on the date of loss, apply the latest bulletin, and leave an auditable note the handler signed.

## Concept

A teardown explains how other products solve a job, which buyer they serve, and which of their choices you should refuse. It is a decision tool for scope. It is not a feature matrix copied from marketing pages, and it is not a claim that you have a moat because a slide says so.

You will compare three public products that a claims or insurance-operations leader could already buy or copy. Use only public documentation, pricing pages, and help centers. Where a public page is silent, write "not stated" and move on. Inventing a competitor's accuracy number is a worse outcome than a hole in the table.

## Approach

Pick three products in three different seats, so the comparison teaches positioning:

1. A horizontal document assistant that can be pointed at a policy folder (a general copilot with file search).
2. A vertical claims or insurance operations product that advertises note drafting or policy Q&A.
3. The incumbent workaround treated as a product: shared drive plus email bulletins plus the system of record. Incumbents win more pilots than startups do.

For each, record the job they claim, the user who is the buyer, what they show as evidence for an answer, whether a human commit is visible, and what they say about audit or retention. Then write the implication for Harbor in one paragraph per product: what to copy, what to refuse, and which assumption of theirs does not hold in a regulated claims note.

Moat language has to be falsifiable. "We will have proprietary prompts" is not falsifiable. "A horizontal assistant does not know which bulletin amends which form edition, and the public docs do not describe an edition-in-force rule" is a claim you can check.

## Components

- **Product cards.** One page each: buyer, user, job claimed, evidence shown to the user, human commit, audit story, what is not stated.
- **Comparison table.** Rows are the jobs in the Harbor episode, not a grocery list of features. Columns are the three products plus Harbor's intended stance.
- **Refusal list.** Three capabilities you will not chase because they belong to a different buyer or a different risk posture.
- **Switching-cost note.** What a Columbus handler would lose by leaving `oh-auto-deltas` and the supervisor relationship, even if Harbor is better at search.
- **Open questions for a vendor demo.** Five questions you would ask if Northline ran a bake-off. Each question asks the vendor to show a behavior on a conflict case, not to show a slide.

## Flow

1. Choose the three products and save the public URLs and the date you read them. The teardown expires; the date is part of the artifact.
2. Fill the product cards. Every cell is either a short paraphrase with a URL, or "not stated."
3. Build the comparison table around the episode: edition-in-force, bulletin overlay, citation visible to the handler, named author on the note, refusal to draft claimant text.
4. Write the refusal list and the switching-cost note.
5. On day 10, write the five demo questions. At least two must be questions the public docs could not answer.

## Tools and stack

A browser, a markdown file, and the public web. No vendor login, no scraped review mine, and no paid dataset. If a page requires an account, record that the information is gated and choose a different public source.

## Setup

1. Create `harbor-portfolio/09-teardown/teardown.md`.
2. Spend the first hour selecting products. Prefer products whose docs you can actually read.
3. Cap research at half a day. A teardown that takes a week has become a market report. This artifact is a decision aid for Harbor's pilot scope.
4. Record access dates next to every URL.

## Deliverables

- Three product cards with URLs and access dates.
- A comparison table tied to the Harbor episode.
- A refusal list, a switching-cost note, and five bake-off questions.

## What done looks like

Someone preparing a vendor meeting can use your questions without redoing the research. The table contains "not stated" where the evidence stopped. Harbor's column is a stance, clearly marked as intent, and is not disguised as a fact about a product that does not exist yet.

## Think a step ahead

Public docs rarely describe what a product does when two policy documents conflict or when an edition was withdrawn. Add a one-page "conflict case" you would hand every vendor: date of loss, two form editions, one bulletin that amends only the newer edition, and a handler who must not cite the withdrawn file. You will grade Harbor itself against that case in the retrieval postmortem on days 73–74.

## Interview angle

Bring the refusal list. A PM who can say what they will not build, and why a competitor's feature belongs to a different buyer, sounds like someone who has shipped.
