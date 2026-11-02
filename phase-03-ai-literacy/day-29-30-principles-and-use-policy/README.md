# Product Principles and Acceptable Use

**Days 29–30 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor proposes note text and citations for Northline Mutual handlers. The handler commits the note to Lumen under their own name. The pilot is personal auto in the Columbus office. Harbor does not decide coverage, set reserves, or message the claimant. The note may be read later by a supervisor, an investigator, or defense counsel.

## Concept

Principles are the short list a team uses when a requirement conflicts with another requirement and nobody wants to reopen the whole spec. An acceptable-use policy is the handler-facing and manager-facing document that says what this tool is for, what it must not be asked to do, and what happens when someone asks anyway. Together they keep a pilot from drifting into a coverage engine because a regional manager requested it in week three.

This project writes both, specifically for Harbor. It also writes the decision rule for a request that violates a principle: who hears it, how fast, and what "no" sounds like when the requester is senior.

## Approach

Write five principles, no more. Each principle has a meaning paragraph, a Harbor example of following it, and a Harbor example of breaking it. Candidates you should consider, and you may replace one if you can defend the replacement:

1. **The handler is the author.** Commit writes their identity, not the model's.
2. **Citations are part of the answer.** A paragraph the handler might rely on has a source they can open, or the product says it has none.
3. **The tool stays inside the note.** Coverage, reserves, and claimant communications are out, even when phrased as "just a draft for me."
4. **Absence is a result.** A missing bulletin is shown as missing. It is not filled with plausible language.
5. **Logs exist for the file, not for surprise.** Handlers know what is retained and who in the company can read a draft they discarded.

The acceptable-use document is two pages, written to a new handler and their supervisor. It includes how to cite Harbor in a note (the note is theirs; they do not write "per the AI"), what prompts are out of bounds, and what to do when the draft and the PDF disagree (the PDF and the published bulletin win; they escalate content bugs to a named alias).

The escalation rule covers a senior request to "just let it deny obvious glass claims." The artifact names the forum, the maximum time to decision, and the default during the wait, which is that the principle stands.

## Components

- **Principle cards.** Five, with follow and break examples from the Harbor episode.
- **Handler page.** What this is, what you may ask, what you may not ask, how to commit, how to report a bad citation.
- **Supervisor page.** What an audit may rely on, what training to give in the first week, what not to measure (drafts per hour as a productivity contest).
- **Escalation rule.** Forum, clock, default-during-the-wait, and a sample reply to the senior request.
- **Conflict log template.** Date, request, principle touched, decision, decider. Empty and ready for the pilot.

## Flow

1. Draft principles from the interaction contract. If a principle is not already implied by the contract, either update your understanding of the contract or drop the principle. They should not diverge silently.
2. Write the break examples first. They are the test that the principle is real.
3. Write the handler page out loud. Cut any sentence you would be embarrassed to read in a Monday standup on the claims floor.
4. Write the supervisor page, including the metric you refuse to put on a leaderboard.
5. On day 30, write the escalation sample and run it past a friend playing the regional manager. If your "no" is vague, rewrite it until the requester knows the request was declined and where it can be re-heard.

## Tools and stack

Markdown. The interaction contract as source material. No policy-management product. The template for the conflict log is a table in the same file.

## Setup

1. Create `harbor-portfolio/29-principles/principles.md` and `acceptable-use.md`.
2. Reread the prohibitions in the case before drafting. They are the non-negotiable core.
3. Day 29 is principles and the handler page. Day 30 is the supervisor page, the escalation rule, and the spoken test.

## Deliverables

- Five principle cards with follow and break examples.
- A two-page acceptable-use document split for handlers and supervisors.
- An escalation rule and a conflict-log template, plus the sample reply.

## What done looks like

A new handler can say what they must not ask Harbor to do, and a supervisor can say what an audit relies on. The sample reply to the senior request is specific. One metric is explicitly banned from the leaderboard, with a reason. Principles and the interaction contract do not contradict each other.

## Think a step ahead

Principles written for a note-drafting pilot get pressure the moment a second team wants to reuse "the Harbor model" for a claimant-facing bot. Add a reuse gate: a one-page questionnaire another team must answer before they can call their feature a Harbor feature. Include intended reader, who the author is, what the model is forbidden to decide, and which principle would have to change. If a principle would have to change, the reuse is a new product decision, not a configuration. You will meet the same gate again in the platform-versus-feature bet on days 95–96.

## Interview angle

Read the break example for "absence is a result," then the sample reply to the senior request. Both show you can hold a line in writing.
