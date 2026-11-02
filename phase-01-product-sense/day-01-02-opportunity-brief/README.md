# Opportunity Brief

**Days 1–2 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual, a mid-size US insurer. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. The proposed pilot is the Columbus, Ohio office: 40 handlers. A claims-operations review reports 26 minutes average handle time on a new auto claim, about 9 of those minutes spent finding the policy form in force on the date of loss, and 3.1% of audited notes citing a form that was not in force. The library is roughly 1,400 pages, plus a weekly compliance bulletin.

## Concept

An opportunity brief is the one-page argument that a problem deserves a team, written before any solution sketch. It names the person who feels the pain, the job they already pay for with time and rework, the constraint that makes the pain durable, and the reason the timing is real. For an AI product the brief also states what the system is forbidden to decide. That boundary belongs in the opportunity, because an unbounded "AI for claims" pitch will stall in legal, and it should.

The reader is the VP of Claims Operations. She has budget for a ten-week pilot and no interest in a model demo.

## Approach

Use only the case facts above, and label anything you add as an assumption. Keep three layers visible on the page:

1. Observed facts, each sourced to the claims-operations review or the given pilot scope.
2. Assumptions written so that an interview could prove them false.
3. A bet small enough for forty handlers in one state.

A feature list is a different document. A paragraph about the global insurance-software market is a different document. After one pass, a reader should be able to restate the problem in a single sentence that does not mention a model.

## Components

- **Problem statement.** Who, which painful job, how often, what it costs. One sentence.
- **Who feels it.** The handler writing the note, the supervisor sampling notes, the claimant waiting. Name whose pain is primary.
- **Current alternative.** The claims system Lumen, the shared-drive library, and the bulletin email, described as a procedure.
- **Why now.** One trigger. The citation defect, audit pressure, and handler attrition are all real; pick the one that justifies a pilot this quarter and say why the others can wait.
- **Cost of inaction.** Time and audit findings you can point at. Leave any number you do not have unstated.
- **Prohibitions.** Coverage, reserves, claimant-facing text.
- **Kill assumptions.** Three beliefs that end the pilot if they are false.
- **Pilot fence.** Office, line of business, state, and what "end of pilot" means.

## Flow

1. Read the case once. Mark quantities and prohibitions.
2. Write the problem sentence. If it contains "AI" or "transform," rewrite it until the pain stands on its own.
3. Write the current procedure in five steps a new handler could follow on Monday.
4. Choose a single why-now trigger. List the kill assumptions under it.
5. Draft the bet: whose week changes, in which office, noticed how.
6. On day 2, mark every sentence as fact, assumption, or recommendation. Delete any recommendation that has neither a fact nor an assumption under it.

## Tools and stack

A markdown editor and a timer. No design tool and no model API. The constraint is the point: the brief should be something you can defend without a generated draft in front of you.

## Setup

1. Create `harbor-portfolio/01-opportunity-brief/`.
2. Create `opportunity-brief.md` with the component headings, in the order listed above.
3. Day 1: 90 minutes for the first draft. Day 2: 45 minutes for the fact-check pass.
4. Paste the case paragraph at the top of the draft so a reader who never sees this playbook still has the scene.

## Deliverables

- `opportunity-brief.md`, one to two pages.
- Three kill assumptions a researcher can turn into interview questions on days 3–4.
- A one-sentence pilot fence you could forward to counsel.

## What done looks like

A skeptical operations director can read the brief in four minutes and answer four questions: who hurts, what they do today, what we will refuse to automate, and what would make us stop. Every number traces to the case. Every forward-looking sentence is labeled as a bet.

## Think a step ahead

Handlers are not the only people who will read a Harbor draft. Supervisors audit it, special-investigation units may rely on it, and defense counsel may discover it later. Add a short secondary-readers note: for each reader, what harm follows if a draft is confident and wrong. The interaction contract on days 25–26 starts from that note.

## Interview angle

Describe the brief as a scoping decision. You fenced the pilot to one office and wrote the prohibitions before choosing a solution. That is the difference between a product bet and a demo.
