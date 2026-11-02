# Interview Field Kit

**Days 3–4 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. Baseline: 26 minutes average handle time on a new auto claim, about 9 minutes finding the form in force on the date of loss, 3.1% of audited notes citing a form that was not in force. Library: about 1,400 pages plus a weekly compliance bulletin.

## Concept

An interview kit is how a product manager hears the work, rather than the opinion of the work. Handlers are skilled at the job and uneven at describing it. If you ask "would you use an AI assistant?", you will collect politeness. If you ask them to walk the last claim they touched, you will collect the procedure, the workaround, and the moment they got nervous.

This project produces a discussion guide, a note taxonomy, and an insight memo grounded in two supplied transcripts. The transcripts are fiction, written for practice, and they contain both signal and noise on purpose.

## Approach

Design the guide before you read the transcripts, so you feel the gap between the questions you planned and the evidence you actually get. Then annotate the transcripts with four tags only:

- **Observation.** Something the handler did or quoted a screen as doing.
- **Pain.** A cost they named: time, rework, anxiety, a supervisor bounce-back.
- **Workaround.** A step that exists because the official path failed.
- **Opinion.** A preference or a prediction about a future tool.

Insights may cite observations, pains, and workarounds. An insight may not cite an opinion as if it were evidence. "I would love a copilot" is an opinion. "I paste the bulletin into a personal document because search misses the latest form" is a workaround.

Write questions that ask for a specific recent case. Ask what happened, what they looked at, where they hesitated, and what the supervisor changed. Leave product pitches out of the guide.

## Components

- **Discussion guide.** Opening, a recent-case walkthrough, a form-finding probe, a bulletin probe, a supervisor-rework probe, and a close. Eight to twelve questions.
- **Note taxonomy.** The four tags above, with one example sentence of each, so a second interviewer tags the same way.
- **Evidence table.** Quote, tag, transcript id, and the claim it supports.
- **Insight memo.** Three insights. Each one states the behavior, the cost, and the open question. Each one quotes the transcript.
- **Question backlog.** What you still need to ask a third handler, because two transcripts are not a finding about the office.

## Flow

1. Draft the discussion guide from the opportunity brief's kill assumptions. One question per assumption, asked indirectly.
2. Read `fixtures/transcripts.md` once without tagging.
3. Tag on the second pass. Copy quotes into the evidence table. Keep the words exact.
4. Write three insights. Under each, list the quotes that carry it and one quote you almost used but classified as opinion.
5. On day 4, rewrite the guide. Add the question the transcripts showed you should have asked, and strike any question that would have produced only an opinion.

## Tools and stack

A markdown editor. The transcripts in this folder. Optional: a second person to tag the same transcript so you can compare tags. No transcription vendor and no sentiment model. Tagging by hand is the lesson.

## Setup

1. Read the opportunity brief if you wrote one; otherwise use the case paragraph above.
2. Open [`fixtures/transcripts.md`](fixtures/transcripts.md).
3. Create `harbor-portfolio/03-interview-kit/` with `guide.md`, `evidence-table.md`, and `insight-memo.md`.
4. Budget two hours to tag and one hour to rewrite the guide.

## Deliverables

- Discussion guide, ready to hand to a second interviewer.
- Evidence table with at least twelve tagged quotes.
- Insight memo of three insights, each tied to quotes, plus a question backlog of at least four unanswered questions.

## What done looks like

A reader who skips the transcripts can see which sentences are evidence and which were set aside as opinion. The rewritten guide asks about a behavior the first draft missed. No insight recommends a feature by name. Recommendations start only after the insight is stated.

## Think a step ahead

Two Columbus handlers can share a workaround that the night shift does not use. Add a sampling note: which shifts, tenures, and claim types (glass-only, total loss, injury) are absent from these transcripts, and which insight you will refuse to generalize until that gap is filled. Days 11–12 pick up the same gap as an extreme-user map.

## Interview angle

Show the evidence table, not the insights alone. Hiring managers trust a PM who can point at the quote they refused to treat as evidence.
