# AI Product Playbook — Full Plan

This is the consolidated curriculum. It is the entire 100-day plan written out in one place: the goal and skills of each phase, and the full write-up of every project. The catalog tables live in [README.md](README.md). Each project also has a working copy in its own folder; those copies are linked from the headings below so you can open the fixtures beside the text.

The plan runs from beginner product sense to advanced bets. Phases 1 and 2 are beginner. Phases 3 through 5 are intermediate. Phases 6 through 10 are advanced. Every project includes a follow-on, "Think a step ahead," that names the next harder problem. On advanced projects that follow-on is part of the required work, not an optional extra.

No paid model, cloud account, or running service is required. The deliverable of each project is a decision artifact: a brief, a spec, a rubric, a ship note, a runbook, or a narrative.

## The continuing case

Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual, a fictional mid-size US insurer. Handlers remain the author of every note committed to the claims system, Lumen. Harbor does not decide coverage, set reserves, or write to the claimant. The pilot is the Columbus, Ohio office, 40 handlers. Baseline from the case: 26 minutes average handle time on a new auto claim, about 9 minutes spent finding the form in force on the date of loss, and 3.1% of audited notes citing a form that was not in force. The library is about 1,400 pages plus a weekly compliance bulletin.

Fixtures, transcripts, and result tables in this plan are invented so the practice has something to push against. They are not evidence from a real carrier.

## How the hundred days are organized

| Phase | Days | Level | Projects |
| --- | --- | --- | ---: |
| 1. Product Sense Studio | 1–10 | Beginner | 5 |
| 2. Design Thinking Studio | 11–20 | Beginner | 5 |
| 3. AI Product Literacy | 21–30 | Intermediate | 5 |
| 4. Decision Analytics | 31–42 | Intermediate | 6 |
| 5. Delivery for AI Products | 43–52 | Intermediate | 5 |
| 6. Machine Learning Product Practice | 53–64 | Advanced | 6 |
| 7. Retrieval-Augmented Product Design | 65–74 | Advanced | 5 |
| 8. Evaluation and Harness Practice | 75–86 | Advanced | 6 |
| 9. Data Pipelines and Trust | 87–94 | Advanced | 4 |
| 10. Advanced Bets | 95–100 | Advanced | 3 |

Fifty projects. Days are inclusive and do not overlap. A project is a one- or two-day unit with its own folder and its own write-up.

## Phase 1 — Product Sense Studio

**Days 1–10 · Beginner · 5 projects**

### Goals

This phase produces a problem statement a later specification is allowed to serve. You fence Harbor to one office, one line, and one episode. You separate what handlers did from what they predict they would like. You describe the workaround each person has already hired, and you tell the before-and-after of a single claim without handing coverage decisions to a model. You close by deciding which public alternatives are instructive and which capabilities you will not copy. The phase is done when a skeptical operator can restate who hurts, what they do today, what the pilot will not automate, and which idea you killed.

### Skills covered

Product management: problem framing, interview evidence, jobs-to-be-done, solution narrative, competitive judgment.

### Days 1–2 — Opportunity Brief

Working copy and fixtures: [phase-01-product-sense/day-01-02-opportunity-brief/README.md](phase-01-product-sense/day-01-02-opportunity-brief/README.md)

**Days 1–2 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual, a mid-size US insurer. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. The proposed pilot is the Columbus, Ohio office: 40 handlers. A claims-operations review reports 26 minutes average handle time on a new auto claim, about 9 of those minutes spent finding the policy form in force on the date of loss, and 3.1% of audited notes citing a form that was not in force. The library is roughly 1,400 pages, plus a weekly compliance bulletin.

#### Concept

An opportunity brief is the one-page argument that a problem deserves a team, written before any solution sketch. It names the person who feels the pain, the job they already pay for with time and rework, the constraint that makes the pain durable, and the reason the timing is real. For an AI product the brief also states what the system is forbidden to decide. That boundary belongs in the opportunity, because an unbounded "AI for claims" pitch will stall in legal, and it should.

The reader is the VP of Claims Operations. She has budget for a ten-week pilot and no interest in a model demo.

#### Approach

Use only the case facts above, and label anything you add as an assumption. Keep three layers visible on the page:

1. Observed facts, each sourced to the claims-operations review or the given pilot scope.
2. Assumptions written so that an interview could prove them false.
3. A bet small enough for forty handlers in one state.

A feature list is a different document. A paragraph about the global insurance-software market is a different document. After one pass, a reader should be able to restate the problem in a single sentence that does not mention a model.

#### Components

- **Problem statement.** Who, which painful job, how often, what it costs. One sentence.
- **Who feels it.** The handler writing the note, the supervisor sampling notes, the claimant waiting. Name whose pain is primary.
- **Current alternative.** The claims system Lumen, the shared-drive library, and the bulletin email, described as a procedure.
- **Why now.** One trigger. The citation defect, audit pressure, and handler attrition are all real; pick the one that justifies a pilot this quarter and say why the others can wait.
- **Cost of inaction.** Time and audit findings you can point at. Leave any number you do not have unstated.
- **Prohibitions.** Coverage, reserves, claimant-facing text.
- **Kill assumptions.** Three beliefs that end the pilot if they are false.
- **Pilot fence.** Office, line of business, state, and what "end of pilot" means.

#### Flow

1. Read the case once. Mark quantities and prohibitions.
2. Write the problem sentence. If it contains "AI" or "transform," rewrite it until the pain stands on its own.
3. Write the current procedure in five steps a new handler could follow on Monday.
4. Choose a single why-now trigger. List the kill assumptions under it.
5. Draft the bet: whose week changes, in which office, noticed how.
6. On day 2, mark every sentence as fact, assumption, or recommendation. Delete any recommendation that has neither a fact nor an assumption under it.

#### Tools and stack

A markdown editor and a timer. No design tool and no model API. The constraint is the point: the brief should be something you can defend without a generated draft in front of you.

#### Setup

1. Create `harbor-portfolio/01-opportunity-brief/`.
2. Create `opportunity-brief.md` with the component headings, in the order listed above.
3. Day 1: 90 minutes for the first draft. Day 2: 45 minutes for the fact-check pass.
4. Paste the case paragraph at the top of the draft so a reader who never sees this playbook still has the scene.

#### Deliverables

- `opportunity-brief.md`, one to two pages.
- Three kill assumptions a researcher can turn into interview questions on days 3–4.
- A one-sentence pilot fence you could forward to counsel.

#### What done looks like

A skeptical operations director can read the brief in four minutes and answer four questions: who hurts, what they do today, what we will refuse to automate, and what would make us stop. Every number traces to the case. Every forward-looking sentence is labeled as a bet.

#### Think a step ahead

Handlers are not the only people who will read a Harbor draft. Supervisors audit it, special-investigation units may rely on it, and defense counsel may discover it later. Add a short secondary-readers note: for each reader, what harm follows if a draft is confident and wrong. The interaction contract on days 25–26 starts from that note.

#### Interview angle

Describe the brief as a scoping decision. You fenced the pilot to one office and wrote the prohibitions before choosing a solution. That is the difference between a product bet and a demo.

### Days 3–4 — Interview Field Kit

Working copy and fixtures: [phase-01-product-sense/day-03-04-interview-field-kit/README.md](phase-01-product-sense/day-03-04-interview-field-kit/README.md)

**Days 3–4 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. Baseline: 26 minutes average handle time on a new auto claim, about 9 minutes finding the form in force on the date of loss, 3.1% of audited notes citing a form that was not in force. Library: about 1,400 pages plus a weekly compliance bulletin.

#### Concept

An interview kit is how a product manager hears the work, rather than the opinion of the work. Handlers are skilled at the job and uneven at describing it. If you ask "would you use an AI assistant?", you will collect politeness. If you ask them to walk the last claim they touched, you will collect the procedure, the workaround, and the moment they got nervous.

This project produces a discussion guide, a note taxonomy, and an insight memo grounded in two supplied transcripts. The transcripts are fiction, written for practice, and they contain both signal and noise on purpose.

#### Approach

Design the guide before you read the transcripts, so you feel the gap between the questions you planned and the evidence you actually get. Then annotate the transcripts with four tags only:

- **Observation.** Something the handler did or quoted a screen as doing.
- **Pain.** A cost they named: time, rework, anxiety, a supervisor bounce-back.
- **Workaround.** A step that exists because the official path failed.
- **Opinion.** A preference or a prediction about a future tool.

Insights may cite observations, pains, and workarounds. An insight may not cite an opinion as if it were evidence. "I would love a copilot" is an opinion. "I paste the bulletin into a personal document because search misses the latest form" is a workaround.

Write questions that ask for a specific recent case. Ask what happened, what they looked at, where they hesitated, and what the supervisor changed. Leave product pitches out of the guide.

#### Components

- **Discussion guide.** Opening, a recent-case walkthrough, a form-finding probe, a bulletin probe, a supervisor-rework probe, and a close. Eight to twelve questions.
- **Note taxonomy.** The four tags above, with one example sentence of each, so a second interviewer tags the same way.
- **Evidence table.** Quote, tag, transcript id, and the claim it supports.
- **Insight memo.** Three insights. Each one states the behavior, the cost, and the open question. Each one quotes the transcript.
- **Question backlog.** What you still need to ask a third handler, because two transcripts are not a finding about the office.

#### Flow

1. Draft the discussion guide from the opportunity brief's kill assumptions. One question per assumption, asked indirectly.
2. Read `fixtures/transcripts.md` once without tagging.
3. Tag on the second pass. Copy quotes into the evidence table. Keep the words exact.
4. Write three insights. Under each, list the quotes that carry it and one quote you almost used but classified as opinion.
5. On day 4, rewrite the guide. Add the question the transcripts showed you should have asked, and strike any question that would have produced only an opinion.

#### Tools and stack

A markdown editor. The transcripts in this folder. Optional: a second person to tag the same transcript so you can compare tags. No transcription vendor and no sentiment model. Tagging by hand is the lesson.

#### Setup

1. Read the opportunity brief if you wrote one; otherwise use the case paragraph above.
2. Open [`fixtures/transcripts.md`](fixtures/transcripts.md).
3. Create `harbor-portfolio/03-interview-kit/` with `guide.md`, `evidence-table.md`, and `insight-memo.md`.
4. Budget two hours to tag and one hour to rewrite the guide.

#### Deliverables

- Discussion guide, ready to hand to a second interviewer.
- Evidence table with at least twelve tagged quotes.
- Insight memo of three insights, each tied to quotes, plus a question backlog of at least four unanswered questions.

#### What done looks like

A reader who skips the transcripts can see which sentences are evidence and which were set aside as opinion. The rewritten guide asks about a behavior the first draft missed. No insight recommends a feature by name. Recommendations start only after the insight is stated.

#### Think a step ahead

Two Columbus handlers can share a workaround that the night shift does not use. Add a sampling note: which shifts, tenures, and claim types (glass-only, total loss, injury) are absent from these transcripts, and which insight you will refuse to generalize until that gap is filled. Days 11–12 pick up the same gap as an extreme-user map.

#### Interview angle

Show the evidence table, not the insights alone. Hiring managers trust a PM who can point at the quote they refused to treat as evidence.

### Days 5–6 — Jobs-to-be-Done Switch Story

Working copy and fixtures: [phase-01-product-sense/day-05-06-switch-story/README.md](phase-01-product-sense/day-05-06-switch-story/README.md)

**Days 5–6 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. Baseline: 26 minutes average handle time on a new auto claim, about 9 minutes finding the form in force on the date of loss, 3.1% of audited notes citing a form that was not in force.

#### Concept

People hire a new way of working only when the push of the current situation and the pull of a new situation together beat anxiety and habit. A switch story records that struggle for one real episode. It is the unit of evidence behind a jobs-to-be-done claim. "Handlers need AI" is a slogan. "Priya hired a personal document because the bulletin and the PDF disagreed, and she will fire that document only if a new path covers the bulletin on the days she is out" is a job.

You will write one switch story from the practice transcripts, then a second story as a plan for an interview you have not conducted yet, so you can see which forces you still have to ask about.

#### Approach

Use the four forces, and keep them attached to a moment in time:

- **Push.** What became intolerable in the current procedure, on that claim.
- **Pull.** What the hired workaround promised, specifically.
- **Anxiety.** What almost stopped them from trusting the workaround, or from trusting a future tool.
- **Habit.** What they will keep doing even after a better path exists, because it is how they stay safe.

The hire in Priya's transcript is the desktop document `oh-auto-deltas`, not Harbor. Harbor does not exist for her yet. Write the story of the workaround she already hired. Then write the forces that would have to be true before she would fire that document and hire a pilot tool. Andre's transcript is a contrasting hire: a paper notebook of corrected codes, plus a stated willingness to accept errors in exchange for speed. Those are different jobs. Do not average them into one persona.

#### Components

- **Timeline.** First notice, search, paste, doubt, supervisor bounce, consequence for the claimant. Clock times where the transcript gives them.
- **Force map.** Push, pull, anxiety, habit, each with a quote and a one-line reading.
- **Hire statement.** "When \[situation\], I hire \[workaround\] so I can \[progress\]." One statement for Priya, one for Andre.
- **Firing condition.** What the workaround would have to fail at, or what a new path would have to guarantee, before the hire changes.
- **Anxiety list for a future pilot.** The specific fears a Harbor pilot must design for. Priya's write-up is one. Andre's "I will fix it at the end of the day" is a different risk: a handler who will accept a wrong paragraph if the queue is long.

#### Flow

1. Rebuild Priya's Thursday-to-Friday timeline from transcript T1. Use her words for the force map.
2. Write her hire statement about `oh-auto-deltas`. Check that the statement names progress (a correct rental limit) and not a feature.
3. Repeat the exercise for Andre. Keep his hire statement about the notebook and the supervisor, since that is what he actually hired.
4. Write three anxieties a pilot must address, each traced to a quote.
5. On day 6, draft the switch-interview guide you would use with a third handler: four questions, one per force, each asking for a recent episode.

#### Tools and stack

Markdown. The transcripts in [`../day-03-04-interview-field-kit/fixtures/transcripts.md`](../day-03-04-interview-field-kit/fixtures/transcripts.md). A simple two-by-two force map is enough; a whiteboard photo is optional and not required.

#### Setup

1. Skim the transcripts again, this time looking only for the moment someone changed their behavior.
2. Create `harbor-portfolio/05-switch-story/switch-story.md`.
3. Give the timeline 40 minutes and the force map 40 minutes. Day 6 is the interview guide and a rewrite of any force that has no quote.

#### Deliverables

- One switch story for Priya and one for Andre, each with a timeline, a force map, and a hire statement.
- A firing-condition sentence for each.
- A four-question switch-interview guide for the next handler.

#### What done looks like

The two hire statements are different, and you can explain why averaging them would produce a tool neither of them hired. Every force has a quote. The firing condition is testable in a pilot, not a slogan about delight.

#### Think a step ahead

A switch story about a workaround tells you what the pilot has to beat on day one. The harder problem is the second hire: after three weeks, handlers may keep both Harbor and the personal document, which splits the audit trail. Add a note on the "dual running" risk and what you would count, during a pilot, as evidence that the old workaround has actually been fired. The activation funnel on days 35–36 is where that count becomes a metric.

#### Interview angle

Tell the two hire statements out loud. They show you can hold two segments in your head without collapsing them into "the user."

### Days 7–8 — Problem-Solution Narrative

Working copy and fixtures: [phase-01-product-sense/day-07-08-problem-solution-narrative/README.md](phase-01-product-sense/day-07-08-problem-solution-narrative/README.md)

**Days 7–8 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. Baseline: 26 minutes average handle time on a new auto claim, about 9 minutes finding the form in force on the date of loss, 3.1% of audited notes citing a form that was not in force.

#### Concept

A problem-solution narrative is the short story of a before, a change, and an after, written so a builder can see what "better" means for one episode. It is narrower than a full requirements document. It fixes the episode you intend to improve, the behavior that should be different at the end of that episode, and the behaviors you are leaving alone on purpose.

You will write the narrative for a single claim type: a new personal-auto physical-damage notice in Ohio, where the handler must cite the form in force on the date of loss and the latest bulletin that amends it. Coverage determination stays with the handler.

#### Approach

Write the narrative in scenes, not in requirements identifiers. Scene one is the handler's current path, taken from the switch stories. Scene two is the same claim with Harbor in the loop, told as handler actions and system responses, still without screens. Scene three is the after: what the supervisor sees in the audit sample, and what the claimant experiences (a faster note, not a message from a model).

Hold the narrative to one episode so scope cannot leak. If a sentence would also apply to injury claims, commercial policies, or a claimant chatbot, move it to an explicit out-of-episode list.

Name the authorship rule inside the story. The note that lands in Lumen is the handler's note. Harbor may propose text. The moment of authorship is a human action with a name, such as "Add to note," and the story should say what is true of the file after that action.

#### Components

- **Episode fence.** Claim type, state, what the handler is trying to produce, who signs it.
- **Before scene.** Five steps, with the failure from the case (wrong form or stale bulletin) placed where it actually happens.
- **After scene.** The same five steps, with Harbor's proposal, the citation the handler can see, and the human action that commits text.
- **Unchanged scene.** What the supervisor and the claimant still experience, so "better" is not allowed to mean "the model talks to the customer."
- **Success anecdote.** A paragraph you could read in a pilot retrospective, written in the past tense, with a number you would need to observe. Mark that number as a target, not a result.
- **Non-goals.** At least four, written as episodes you are not telling.

#### Flow

1. Write the before scene from Priya's timeline. Keep the bulletin problem in the scene. A narrative that only solves PDF search has dropped half the job.
2. Write the after scene. Every system action is paired with a handler action. If the system acts twice in a row with no human, rewrite it.
3. Write the unchanged scene for the supervisor's audit and for the claimant's phone call.
4. Draft the success anecdote. Then strike any sentence you could not verify from a file, a clock, or an audit sample.
5. On day 8, read the narrative to someone who has not seen the case. Ask them what Harbor decided. If they say "coverage," the story leaked, and you revise.

#### Tools and stack

Markdown. No wireframe yet. Days 17–18 are where the interaction becomes a script. Staying in prose forces you to get the responsibility right before you get the layout right.

#### Setup

1. Have the switch stories or the transcripts within reach.
2. Create `harbor-portfolio/07-narrative/narrative.md` with the six component headings.
3. Day 1 of the project: before, after, unchanged. Day 2: anecdote, non-goals, and the read-aloud test.

#### Deliverables

- A narrative of about 700 to 1,000 words covering one episode.
- A non-goal list of at least four neighboring episodes.
- A one-paragraph note on what the read-aloud test revealed, including what you changed.

#### What done looks like

A designer and a claims supervisor can both retell the episode. The designer can see the human commit point. The supervisor can see that the audit sample still has a named author. The success anecdote contains a target and no pretended result.

#### Think a step ahead

The narrative covers the happy claim, where the form and the bulletin agree once they are both on screen. The next episode is a conflict: the bulletin and the PDF disagree, and the handler has to choose. Add a six-line "conflict beat" that says what Harbor shows when two sources cannot both be cited as current, and who is allowed to resolve it. The corpus policy on days 67–68 turns that beat into a precedence rule.

#### Interview angle

Walk a hiring manager through the before and after using one claim, and end on the commit point. Responsibility is the part most AI narratives skip.

### Days 9–10 — Competitive Teardown

Working copy and fixtures: [phase-01-product-sense/day-09-10-competitive-teardown/README.md](phase-01-product-sense/day-09-10-competitive-teardown/README.md)

**Days 9–10 · Phase 1, Product Sense Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. The job to beat is specific: find the form in force on the date of loss, apply the latest bulletin, and leave an auditable note the handler signed.

#### Concept

A teardown explains how other products solve a job, which buyer they serve, and which of their choices you should refuse. It is a decision tool for scope. It is not a feature matrix copied from marketing pages, and it is not a claim that you have a moat because a slide says so.

You will compare three public products that a claims or insurance-operations leader could already buy or copy. Use only public documentation, pricing pages, and help centers. Where a public page is silent, write "not stated" and move on. Inventing a competitor's accuracy number is a worse outcome than a hole in the table.

#### Approach

Pick three products in three different seats, so the comparison teaches positioning:

1. A horizontal document assistant that can be pointed at a policy folder (a general copilot with file search).
2. A vertical claims or insurance operations product that advertises note drafting or policy Q&A.
3. The incumbent workaround treated as a product: shared drive plus email bulletins plus the system of record. Incumbents win more pilots than startups do.

For each, record the job they claim, the user who is the buyer, what they show as evidence for an answer, whether a human commit is visible, and what they say about audit or retention. Then write the implication for Harbor in one paragraph per product: what to copy, what to refuse, and which assumption of theirs does not hold in a regulated claims note.

Moat language has to be falsifiable. "We will have proprietary prompts" is not falsifiable. "A horizontal assistant does not know which bulletin amends which form edition, and the public docs do not describe an edition-in-force rule" is a claim you can check.

#### Components

- **Product cards.** One page each: buyer, user, job claimed, evidence shown to the user, human commit, audit story, what is not stated.
- **Comparison table.** Rows are the jobs in the Harbor episode, not a grocery list of features. Columns are the three products plus Harbor's intended stance.
- **Refusal list.** Three capabilities you will not chase because they belong to a different buyer or a different risk posture.
- **Switching-cost note.** What a Columbus handler would lose by leaving `oh-auto-deltas` and the supervisor relationship, even if Harbor is better at search.
- **Open questions for a vendor demo.** Five questions you would ask if Northline ran a bake-off. Each question asks the vendor to show a behavior on a conflict case, not to show a slide.

#### Flow

1. Choose the three products and save the public URLs and the date you read them. The teardown expires; the date is part of the artifact.
2. Fill the product cards. Every cell is either a short paraphrase with a URL, or "not stated."
3. Build the comparison table around the episode: edition-in-force, bulletin overlay, citation visible to the handler, named author on the note, refusal to draft claimant text.
4. Write the refusal list and the switching-cost note.
5. On day 10, write the five demo questions. At least two must be questions the public docs could not answer.

#### Tools and stack

A browser, a markdown file, and the public web. No vendor login, no scraped review mine, and no paid dataset. If a page requires an account, record that the information is gated and choose a different public source.

#### Setup

1. Create `harbor-portfolio/09-teardown/teardown.md`.
2. Spend the first hour selecting products. Prefer products whose docs you can actually read.
3. Cap research at half a day. A teardown that takes a week has become a market report. This artifact is a decision aid for Harbor's pilot scope.
4. Record access dates next to every URL.

#### Deliverables

- Three product cards with URLs and access dates.
- A comparison table tied to the Harbor episode.
- A refusal list, a switching-cost note, and five bake-off questions.

#### What done looks like

Someone preparing a vendor meeting can use your questions without redoing the research. The table contains "not stated" where the evidence stopped. Harbor's column is a stance, clearly marked as intent, and is not disguised as a fact about a product that does not exist yet.

#### Think a step ahead

Public docs rarely describe what a product does when two policy documents conflict or when an edition was withdrawn. Add a one-page "conflict case" you would hand every vendor: date of loss, two form editions, one bulletin that amends only the newer edition, and a handler who must not cite the withdrawn file. You will grade Harbor itself against that case in the retrieval postmortem on days 73–74.

#### Interview angle

Bring the refusal list. A PM who can say what they will not build, and why a competitor's feature belongs to a different buyer, sounds like someone who has shipped.

## Phase 2 — Design Thinking Studio

**Days 11–20 · Beginner · 5 projects**

### Goals

This phase turns the fenced problem into a service a handler can be responsible for. You map the people at the edges, including the ones you have not interviewed and must label as supposed. You run a small workshop whose output includes the ideas that lost. You blueprint the episode so the model, the content operation, and the waiting claimant each have a lane. You test the interaction with a human behind the curtain before any model is in the loop, and you write a critique and a test plan aimed at the ways generative screens hide authorship, provenance, and reversibility. The phase is done when a second facilitator could run a session from your script and your tasks.

### Skills covered

Design thinking: empathy mapping, facilitated selection, service blueprinting, wizard-of-oz prototyping, generative-UI critique and usability planning.

### Days 11–12 — Empathy Maps and Extreme Users

Working copy and fixtures: [phase-02-design-thinking/day-11-12-empathy-and-extremes/README.md](phase-02-design-thinking/day-11-12-empathy-and-extremes/README.md)

**Days 11–12 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. Baseline: 26 minutes on a new auto claim, about 9 minutes finding the form in force, 3.1% of audited notes citing a form that was not in force. Practice transcripts for two day-shift handlers live in [`../../phase-01-product-sense/day-03-04-interview-field-kit/fixtures/transcripts.md`](../../phase-01-product-sense/day-03-04-interview-field-kit/fixtures/transcripts.md).

#### Concept

An empathy map puts one person's situation on a single page: what they are trying to do, what they see on screen, what they say to a coworker, what they do under pressure, and what they fear will be true of them if they are wrong. Extreme users are the people at the edge of that situation, where a design that works for a confident four-year handler fails in a way that matters.

For Harbor, the instructive extremes are not "power users who love AI." They are the new handler who will paste a wrong paragraph rather than leave a note blank, the night-shift handler whose help-desk index is stale, the supervisor who must defend the note six months later, and the handler who was written up because a sentence in a note sounded like a coverage denial.

#### Approach

Build four maps. Two are grounded in the transcripts (Priya, Andre). Two are extreme sketches you label as hypotheses, because you have not interviewed them: a night-shift handler, and a supervisor who audits 8% of notes. A hypothesis map is useful only if every item is marked "heard" or "supposed." Mixing the two is how teams invent a user and then build for the invention.

On each map, add a failure line: the sentence this person is afraid will appear in a file with their name on it. That line is more useful than a demographic. Priya's failure line is a denial that she did not mean to write. Andre's failure line is a blank note that fails audit, which pushes him toward copying anything the tool offers at the end of a long day.

#### Components

- **Map header.** Role, tenure, shift, claim mix, and whether the map is heard or supposed.
- **Doing and seeing.** The actual artifacts on their desk or screen during a new auto notice.
- **Saying and hearing.** What coworkers and supervisors tell them. Quote the transcripts where you have them.
- **Fearing.** The career or claimant consequence they are managing.
- **Failure line.** The bad sentence in the file.
- **Design implication.** One behavior Harbor must support or prevent for this person. Implications are not features. "Must show the bulletin date next to the form edition" is an implication. "Add a chatbot" is not.

#### Flow

1. Fill Priya's map only from transcript quotes. If you cannot point at a line, it does not go in the heard map.
2. Fill Andre's map the same way. Pay attention to the closure metric he named. Speed pressure is part of his empathy map, and it is a risk to accuracy.
3. Draft the night-shift and supervisor maps. Stamp every sticky as supposed. Write the interview question that would promote it to heard.
4. Compare failure lines. Circle the place where helping Andre's speed makes Priya's failure line more likely.
5. On day 12, choose the extreme you will design for first, and write five lines on what you will deliberately make slightly worse for a different user in order to protect that extreme.

#### Tools and stack

Markdown, or four sheets of paper photographed and summarized back into markdown. The durable artifact is the markdown, because a photo of stickies does not survive a portfolio review on its own.

#### Setup

1. Create `harbor-portfolio/11-empathy/maps.md`.
2. Open the transcripts beside the file.
3. Day 11 is the two heard maps. Day 12 is the two supposed maps, the conflict between them, and the choice of who you design for first.

#### Deliverables

- Four empathy maps with heard and supposed stamps.
- Four failure lines.
- A one-page choice: which extreme the pilot protects first, what that costs another user, and the interview that would change your mind.

#### What done looks like

A designer can start a workshop from the maps without inventing a new persona. The two supposed maps are visibly less certain than the heard maps. The choice of who to protect first is explicit, including the cost.

#### Think a step ahead

Empathy maps decay when the office changes shift patterns or when a new bulletin type arrives. Add a refresh rule: which map items expire after the next bulletin cycle, and who on the pilot team is responsible for re-hearing them. A map that cannot say when it becomes fiction will be treated as fact in a roadmap review three months from now.

#### Interview angle

Show the heard-versus-supposed stamp. It signals that you know the difference between research and a plausible story.

### Days 13–14 — How-Might-We Workshop

Working copy and fixtures: [phase-02-design-thinking/day-13-14-how-might-we/README.md](phase-02-design-thinking/day-13-14-how-might-we/README.md)

**Days 13–14 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. The pilot job is narrow: on a new Ohio personal-auto notice, help the handler cite the form in force on the date of loss and the bulletin that amends it, and commit a note they are willing to sign. Coverage, reserves, and claimant messages stay out.

#### Concept

"How might we" questions turn a specific pain into a space of possible responses, wide enough to escape the first idea and narrow enough to still be about the pain. The workshop is the diverge-and-converge loop around those questions, including the kill criteria you declare before you fall in love with an idea.

You will run the workshop alone or with one partner, on paper, against the Harbor episode. The output is a selected concept and a written record of what you killed and why. The record matters more than the winning sketch. Portfolio reviewers and future teammates need to see the ideas that lost.

#### Approach

Write how-might-we questions from failure lines, not from a solution you already want. A good question for this case: "How might we make the January bulletin visible at the moment Priya pastes a paragraph, without asking her to remember a desktop file?" A weak question: "How might we use AI to delight handlers?"

Diverge in silence first. Eight ideas in twelve minutes, each on its own line, each allowed to be impractical. Then converge with criteria you wrote down before looking at the list:

- Protects the named author on the note.
- Handles a bulletin that is newer than the PDF.
- Can be explained to a supervisor in a minute.
- Can be piloted with forty handlers without a new system of record.
- Does not require the model to decide coverage.

Score ideas against the criteria in plain language. A weighted numeric score is optional and easy to fake with eight ideas; a sentence per criterion is harder to fake and easier to defend.

#### Components

- **Question set.** Four how-might-we questions, each traced to a failure line or a transcript quote.
- **Idea list.** At least eight responses, mixed in type: a process change, a screen change, a content-ops change, and a model-backed change. At least two ideas contain no model at all. If every idea is a model, the workshop was a feature brainstorm.
- **Kill criteria.** The five above, or your revision of them, fixed before scoring.
- **Selection note.** The idea you will carry into the service blueprint, the runner-up, and the first idea you killed.
- **Parking lot.** Ideas that are real and out of pilot scope, so they are not lost and not smuggled in.

#### Flow

1. Draft four questions from the empathy maps. Read each question and strike the ones that contain a solution noun ("chatbot," "copilot," "RAG").
2. Set a twelve-minute timer and list eight ideas. Stop when the timer ends, even if you have a ninth.
3. Write the kill criteria on a separate page before you score.
4. For the top three, write one sentence per criterion. Select one.
5. On day 14, stress the winner: describe the claim where it fails. If you cannot name that claim, you have not understood the idea yet. Then write the parking lot.

#### Tools and stack

Paper or markdown. A timer. No workshop software. The point of a small studio exercise is the thinking sequence, which a facilitation tool tends to hide behind stickies.

#### Setup

1. Create `harbor-portfolio/13-hmw/workshop.md`.
2. Have the failure lines from the empathy maps at the top of the file.
3. Day 13 is questions, divergence, and criteria. Day 14 is selection, the failure claim, and the parking lot.

#### Deliverables

- Four how-might-we questions mapped to evidence.
- Eight ideas and a visible set of non-model ideas.
- A selection note with criteria applied in sentences, plus a parking lot.

#### What done looks like

A facilitator who was not in the room can see why the winner won and why the first exciting idea lost. The selected concept can be handed to the service-blueprint project without a new brainstorm. Scope that belongs later is parked, not deleted in silence.

#### Think a step ahead

Workshops produce a winner that assumes the policy library is already trustworthy. Add a question you did not ask in the main set: "How might we know the library itself is safe to cite this week?" That question is the seed of the knowledge publishing pipeline on days 91–92. Write it down now so the concept you selected does not pretend content operations are free.

#### Interview angle

Tell the killed idea first. Then the criteria. Then the winner. That order shows judgment rather than taste.

### Days 15–16 — Service Blueprint for a Human and a Model

Working copy and fixtures: [phase-02-design-thinking/day-15-16-service-blueprint/README.md](phase-02-design-thinking/day-15-16-service-blueprint/README.md)

**Days 15–16 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. Harbor may propose text and citations for the form in force on the date of loss and for the bulletin that amends it. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot: Columbus, Ohio, personal auto, 40 handlers.

#### Concept

A service blueprint is a picture of one episode across time, with the customer's path, the employee's path, the visible frontstage, and the backstage work that makes the frontstage true. When a model joins the service, it gets its own lane. It is not a decoration on the employee's lane, and it is not the customer. For Harbor the claimant never sees the model. The employee is the handler. The model lane proposes. A fourth lane, content operations, keeps the library and the bulletin true. Most AI blueprints forget that fourth lane and then act surprised when the draft cites a withdrawn form.

#### Approach

Blueprint a single episode: a new Ohio personal-auto physical-damage notice, from the moment the first notice is opened in Lumen to the moment the handler commits the note and the supervisor's audit sample could include it. Use five lanes:

1. **Claimant.** What they are waiting on. They do not interact with Harbor.
2. **Handler frontstage.** What the handler sees and does, including the commit action.
3. **Model lane.** What Harbor retrieves, drafts, and refuses. Include the moment it has no safe citation.
4. **Content and compliance backstage.** Who published the form, who published the bulletin, and how an old edition is withdrawn.
5. **Supervision.** What the supervisor sees later, and which artifacts make the note defensible.

Mark fail points with a specific recovery, not a red dot. A fail point without a recovery is a complaint. Example: the bulletin arrived this morning and is not in the library yet. Recovery: Harbor shows "bulletin not in the published set as of \[time\]" and the handler falls back to the official email, which is an explicit path, not a hidden workaround.

#### Components

- **Episode header.** Trigger, end state, actors, and the evidence each actor leaves behind.
- **Lane table or mermaid diagram.** Steps in order. Each step names the actor and the artifact produced.
- **Fail points.** At least five. For each: how the handler notices, what they do next, what gets logged.
- **Line of visibility.** What the handler is allowed to see about the model's sources. Citations are above the line. Hidden chain-of-thought is below it and stays there.
- **Support processes.** Library publish, bulletin ingest, access removal when a handler changes office.

#### Flow

1. List the steps of the before-path from the problem-solution narrative. Place each step in a lane.
2. Insert the model lane only where the selected how-might-we concept acts. Do not insert it into every step.
3. Add the content-operations lane. If you cannot name a human owner for "bulletin published," write "owner missing" and treat it as a fail point.
4. Write five fail points with recoveries. At least one recovery must be "do not draft."
5. On day 16, walk the blueprint with a clock. Note which steps add handle time. A blueprint that saves nine minutes of searching and adds ten minutes of checking citations has not yet earned its place.

#### Tools and stack

Markdown with a [mermaid](https://mermaid.js.org/) sequence or flowchart is enough. A spreadsheet with one column per lane also works and is easier to review in a pull request. Pick one and keep it legible in plain text.

#### Setup

1. Create `harbor-portfolio/15-blueprint/blueprint.md`.
2. Put the selected concept from the workshop at the top, in two sentences.
3. Day 15 is lanes and the happy path. Day 16 is fail points, the line of visibility, and the clock check.

#### Deliverables

- A blueprint of the episode with five lanes.
- Five fail points, each with a handler-visible recovery and a log line.
- A short timing note: which steps you expect to get faster, which get slower, and what you will time in a pilot.

#### What done looks like

An engineer can see where a model call happens and where it must not. A compliance partner can see who publishes a bulletin and what the handler sees if today's bulletin is missing. The claimant lane contains waiting and a phone call, and contains no chat with Harbor.

#### Think a step ahead

The blueprint assumes one office and one library. The next stress is a handler in Columbus opening a claim for a policy written in another state, or a temporary supervisor from a different line of business. Add a lane note for "wrong library": what the service does when the handler's office and the policy's governing state disagree. That note becomes an access and precedence requirement in the retrieval work on days 65–74.

#### Interview angle

Narrate one fail point end to end, including the log line. Service design for AI is the recovery, not the happy path.

### Days 17–18 — Wizard-of-Oz Interaction Script

Working copy and fixtures: [phase-02-design-thinking/day-17-18-wizard-of-oz/README.md](phase-02-design-thinking/day-17-18-wizard-of-oz/README.md)

**Days 17–18 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. The pilot episode is a new Ohio personal-auto physical-damage notice: cite the form in force on the date of loss, apply the latest bulletin, commit the note. Harbor does not decide coverage, set reserves, or message the claimant.

#### Concept

A wizard-of-oz prototype tests the interaction while a human supplies the intelligence behind the curtain. You learn whether the handler can understand, edit, and responsibly commit a draft before you learn whether a model can produce one. For Harbor this is the right order. A fluent draft that handlers paste without reading would be a failed test, even if the draft were correct.

You will write the script a human wizard follows, the screen the handler thinks they are using, and the test protocol for five handlers. You will also write the latency budget. If the wizard is faster than any model you could deploy, the test has lied to you about pacing, so the script includes a deliberate wait.

#### Approach

Specify the interaction as a script with two roles, Handler and Wizard, plus a Facilitator who does not help. The wizard may use the real policy PDFs and the bulletin. The wizard may not invent policy language. If the wizard cannot find a citation in sixty seconds, the scripted behavior is the product's "I do not have a published source" state, not a best guess.

The handler's screen, described in words and a rough layout, shows three regions: the claim facts already in Lumen (read-only), the proposed note with citations under each paragraph, and a commit control that stays disabled until the handler has expanded at least one citation or typed an edit. That last rule is a hypothesis you are testing, not a law. The protocol asks whether the forced expand feels like safety or like nagging.

Write a latency budget in the script: after the handler asks for a draft, the wizard waits eight seconds even if they are ready sooner, then reveals the draft in one piece. Handlers should feel a pause. You will record whether they use the pause to keep reading the first notice or whether they context-switch away.

#### Components

- **Screen description.** Regions, what is read-only, the commit control and its disabled rule, the empty and error states.
- **Wizard script.** What the wizard may open, the sixty-second citation rule, the eight-second floor, and the exact text of the no-source state.
- **Task set.** Three tasks: a clean match, a bulletin-amends-PDF case, and a no-source case. Claim facts may be fictional; policy sentences the wizard pastes must come from a document you actually provide as a fixture.
- **Observation sheet.** Time to commit, whether the citation was opened, edits made, and any sentence the handler committed that the wizard did not support.
- **Debrief.** Four questions that ask about the episode, not about whether the prototype was "cool."

#### Flow

1. Write the screen description. Mark the commit rule as a hypothesis.
2. Write the wizard script, including the behaviors the wizard is forbidden to do (no coverage language, no extra helpfulness).
3. Author three tiny fictional claim facts and a one-page fixture excerpt the wizard is allowed to cite. Keep the fixture obviously fake if you do not have a real public form; label it "fixture language, not Northline policy."
4. Run the script once with a friend as handler, you as wizard. Fill the observation sheet.
5. On day 18, revise the one moment that confused the handler. Write what you will measure if you later run all five sessions. Running all five is ideal and not required to finish this project.

#### Tools and stack

Markdown script, a printed or on-screen mock laid out with plain text or a simple diagram, and a stopwatch. A slide is enough of a screen. No Figma requirement and no model in the loop. The human wizard is the method.

#### Setup

1. Create `harbor-portfolio/17-wizard/` with `script.md`, `fixture-excerpt.md`, and `observation.md`.
2. Recruit one colleague who is not a PM to play the handler. Brief them with the case in five lines and no more.
3. Day 17 is the script and the fixture. Day 18 is the live run and the revision.

#### Deliverables

- Wizard script with latency floor, citation deadline, and forbidden moves.
- Screen description and three tasks.
- One completed observation sheet and a revision note.

#### What done looks like

A second facilitator could run session two from the script without you. The observation sheet says whether the handler opened a citation before committing. The no-source task has a written state, and the wizard did not improvise a paragraph when the fixture had no answer.

#### Think a step ahead

A wizard who knows the fixture will unconsciously write clearer citations than a retrieval system will. Add a "degraded wizard" pass: on one task, the wizard must include one irrelevant sentence and one citation that points at the right document and the wrong paragraph. Record whether the handler catches each. That pass is a preview of the error-analysis workshop on days 61–62, and it tells you how much checking the commit step really buys.

#### Interview angle

Describe what the handler did during the eight seconds, and whether they caught the planted bad citation. Interaction tests are about behavior under a realistic flaw.

### Days 19–20 — Generative UI Critique and Test Plan

Working copy and fixtures: [phase-02-design-thinking/day-19-20-critique-and-test-plan/README.md](phase-02-design-thinking/day-19-20-critique-and-test-plan/README.md)

**Days 19–20 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. The on-screen proposal is a draft note with citations, sitting beside read-only claim facts from Lumen. Harbor does not decide coverage, set reserves, or message the claimant.

#### Concept

Generative interfaces fail in ways ordinary forms do not. The text looks finished. The citation looks like proof even when it is the wrong paragraph. The handler can become the editor of a document they did not start, which changes where errors hide. A critique rubric for this kind of interface asks whether a skilled worker can tell what is known, what is proposed, what they can change, and how they get back to a state they trust.

This project writes that rubric, applies it to your own wizard-of-oz screen, and turns the gaps into a five-task usability plan you could run in the Columbus office without a model in the loop.

#### Approach

Use six critique lenses, each scored with evidence from the screen description rather than with a vibe:

1. **Authorship.** Can the handler see that the committed note will carry their name, and what "commit" writes to Lumen?
2. **Provenance.** Can they see the document, edition, and bulletin date for each paragraph, and notice a missing one?
3. **Uncertainty.** Does the interface have a designed state for "no published source," or does empty space look like a loading spinner?
4. **Editability.** Can they change one paragraph without regenerating the rest and losing their edits?
5. **Reversibility.** Can they discard the entire draft and return to an empty note they type themselves, in one action?
6. **Pace.** Does the latency floor and the disabled-commit rule respect a 26-minute handle time, or do they stack friction that handlers will route around?

Write the usability plan around tasks, not around screens. Each task has a setup, a success condition a facilitator can observe, and a failure that would change the design. Include one task where the correct behavior is to reject the draft.

#### Components

- **Rubric.** The six lenses, each with a pass question and a fail example drawn from Harbor.
- **Self-critique.** Your wizard screen scored on each lens, with the sentence in the screen description that justified the score.
- **Test plan.** Five tasks, facilitator script, what you record, and what you will not ask ("did you like it?").
- **Recruiting note.** Who in a forty-person office you want: tenure mix, including one person in their first year, and why you will not recruit only volunteers who like new tools.
- **Stop rules.** Conditions under which you halt a session, for example if a participant tries to put coverage language into the note because the draft invited it.

#### Flow

1. Write the pass question for each lens before you look at your screen description, so the rubric is not a retroactive defense.
2. Score your screen. Quote yourself. Any lens you cannot score because the screen never mentioned it is an automatic gap.
3. Turn the two weakest lenses into tasks. Then add a clean success task, a bulletin-conflict task, and a reject-the-draft task, for five total.
4. Write the recruiting note and the stop rules.
5. On day 20, dry-run the facilitator script with a timer. Cut any task that needs more than eight minutes. A plan that takes an hour per handler will not survive a claims floor.

#### Tools and stack

Markdown. The screen description and observation sheet from days 17–18. A stopwatch for the dry run. No usability-lab software. If you later run sessions, a shared notes doc and a clock are sufficient.

#### Setup

1. Create `harbor-portfolio/19-test-plan/critique.md` and `test-plan.md`.
2. Keep the wizard screen description open while you score.
3. Day 19 is the rubric and the self-critique. Day 20 is the five tasks, recruiting, stop rules, and the timed dry run.

#### Deliverables

- Critique rubric with pass questions and Harbor-specific fail examples.
- Self-critique with quotes from your own screen description.
- Five-task test plan, recruiting note, and stop rules.

#### What done looks like

A researcher who has never attended your workshop can facilitate task three tomorrow. Every task has an observable success condition. The plan includes a task whose success is rejecting the draft. The rubric caught at least one gap you then wrote into the plan, so the critique changed the work.

#### Think a step ahead

A five-person test on a wizard will not tell you how the interface behaves when the draft is usually right and occasionally, quietly wrong. Add a follow-on study design, one page, for a later week when a real model is in the loop: how you will salt known-bad citations at a low rate, how you will tell participants that salting happened after the session, and what consent that requires. Salting without consent is a different, unacceptable study. Write the consent sentence now.

#### Interview angle

Show one lens you failed and the task you added because of it. Critique that does not change the plan is taste.

## Phase 3 — AI Product Literacy

**Days 21–30 · Intermediate · 5 projects**

### Goals

This phase gives you language for what a model class can own and what the product must own instead. You compare model classes against Harbor's actual moves and show the cost arithmetic. You translate transformer behavior — tokens, the context window, attention, next-token generation, sampling — into a backlog a designer can accept. You write the interaction contract as observable behavior, then the economics and latency policy that decide whether a pilot is affordable, then the principles and the handler-facing rules that keep a regional request from turning the pilot into a coverage engine. The phase is done when the contract, the principles, and the economics do not contradict each other.

### Skills covered

AI literacy and transformers: model-class fit, token and context constraints, interaction contracts, unit economics, product principles and acceptable use.

### Days 21–22 — Model Capability Card

Working copy and fixtures: [phase-03-ai-literacy/day-21-22-model-capability-card/README.md](phase-03-ai-literacy/day-21-22-model-capability-card/README.md)

**Days 21–22 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. The pilot job is to propose note text with citations to the form in force on the date of loss and the bulletin that amends it. Harbor does not decide coverage, set reserves, or message the claimant. Handle time today is about 26 minutes, of which about 9 are search.

#### Concept

A capability card is a product document that says what class of model could do this job, what it costs in latency and money at the shape of the job, and which failure modes are properties of the class rather than bugs you can ticket away. It is how a PM talks about models with engineering and with a vendor without pretending to have trained one.

You will write one card with three columns: a small instruction-following model, a larger general model, and a model with a long context window that could, in theory, be handed a whole form. The columns are classes. You may name current public model families as examples, with the date you checked, and you must keep the conclusion attached to the class properties (context length, tool use, price band, citation behavior) so the card survives the next model release.

#### Approach

Evaluate the classes against Harbor's job, decomposed into moves:

- Select the edition in force on a given date of loss.
- Locate a paragraph and the bulletin that amends it.
- Draft note text that stays inside the cited lines.
- Decline when the published set has no supporting line.
- Stay inside a latency budget that does not erase the 9 minutes you are trying to return.

For each move, write "fits," "fits only with a tool or a retrieval step," or "unreliable for this move," plus the reason. A long context window is not automatically a fit for edition selection. A window that can swallow a form can still quote an edition that was not in force, because the date rule is a fact about the policy record, not a fact hidden in prose. Put that distinction on the card in your own words.

Include a failure-mode row that is about the product, not the benchmark: fluent text with a citation that does not support the sentence; a refusal on a question the library does answer; a draft that slides from summary into coverage language.

#### Components

- **Job moves.** The five moves above, possibly revised, each in one line.
- **Class columns.** Three classes, with an example name and the date you read its public docs, or "example unnamed" if you stay at the class level.
- **Fit table.** Move by class, using the three fit labels.
- **Latency and cost band.** A rough per-draft range you compute from public price sheets: input size you assume, output size you assume, and the resulting cents per draft. Show the arithmetic.
- **Failure modes that survive a smarter model.** At least three, and why a higher benchmark score would not retire them.
- **Recommendation.** Which class you would pilot, and which move you would not ask the model to perform even on that class.

#### Flow

1. Write the job moves from the service blueprint. Cut any move that is really a human decision.
2. Read one public price page and one public context-length note. Record the date.
3. Fill the fit table. Force every cell to one of the three labels.
4. Do the cents-per-draft arithmetic in the open, with assumed token counts you state.
5. On day 22, write the recommendation and have a colleague try to move you to a different column. Note the argument that was hardest to answer.

#### Tools and stack

Markdown, a calculator or a small spreadsheet, and public vendor documentation. No API key is required. If you do call a model, you are outside this project; the card is a decision document, and a demo is easy to confuse with a fit.

#### Setup

1. Create `harbor-portfolio/21-capability-card/card.md` and `arithmetic.md`.
2. Pick a date and freeze the public pages you cite.
3. Day 21 is moves, sources, and the fit table. Day 22 is cost arithmetic, failure modes, and the recommendation.

#### Deliverables

- A capability card a tech lead can argue with.
- Visible arithmetic for cost per draft.
- A recommendation that names a move the model will not own.

#### What done looks like

The fit table uses the three labels and no "it depends" without a condition. The cost figure can be recomputed from the assumptions. The recommendation survives the question "what if the next model is better?" because the failure modes are tied to the job, not to a leaderboard.

#### Think a step ahead

Vendors will offer a fine-tune or a "claims model" as a fourth column. Add a row that says what evidence would make a fourth column worth a pilot: which move it improves, against which fixture, at which cost delta, and who owns the evaluation when the vendor's number and yours disagree. Days 75–76 are where that evidence plan becomes an eval strategy.

#### Interview angle

Walk through one cell you marked "fits only with retrieval" and the arithmetic under the recommendation. Class judgment plus cost is the literacy a PM is hired for.

### Days 23–24 — Transformer Constraints on the Product

Working copy and fixtures: [phase-03-ai-literacy/day-23-24-transformer-constraints/README.md](phase-03-ai-literacy/day-23-24-transformer-constraints/README.md)

**Days 23–24 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor drafts a claims note and shows citations. The handler signs the note. The sources are policy forms and bulletins, some of them long, some of them amended by a later bulletin that is a separate document. Harbor does not decide coverage.

#### Concept

A transformer is the model architecture behind most products a PM now ships. You do not need to implement one. You do need a mental model that is accurate enough to make product decisions: what the model can look at while it writes the next word, why a long document is not the same thing as a remembered document, why a citation can be fluent and unfaithful, and which of those facts are constraints on Harbor's interface.

This project turns that mental model into a constraint backlog: product requirements that exist because of how these models work, written so a designer and an engineer can accept them without a math lecture.

#### Approach

Write a two-page explanation in product language, aimed at Harbor's designer. Cover these mechanisms and stop before you copy a textbook:

- **Tokens.** The unit the model reads and writes. A policy clause and a form code may tokenize in ways that make exact codes fragile. The product implication is to pass codes as structured fields when you have them, and to show the handler the code you retrieved, not only the sentence the model wrote.
- **Context window.** The working space for one request. Anything outside it is invisible unless a retrieval step or a tool brings it in. The product implication is a designed behavior when the form plus the bulletin plus the claim facts do not fit, or when someone is tempted to paste the entire 1,400-page library.
- **Attention, in one paragraph.** While predicting the next token, the model weights the tokens it can see. It does not look up "the edition in force" as a database would, unless you give it that fact. The product implication is that edition selection is a query against the policy record, and the model's job starts after that fact is known.
- **Next-token generation.** The draft is a continuation, not a retrieved paragraph. It can sound like the form while saying a limit the form does not state. The product implication is that every drafted sentence the handler might rely on needs a citation path the handler can open, and a no-source state when there is nothing to open.
- **Sampling.** The same prompt can yield different drafts. The product implication is that "regenerate" changes the text under an already-reviewed paragraph, so the interface must not silently regenerate a section the handler has edited.

Check your explanation against a failure you can tell in plain language: Harbor quotes a rental limit from the November form on a March loss, in prose that sounds exactly like the February form. Say which mechanism made that easy.

#### Components

- **Mechanism notes.** The five above, each in a short paragraph that ends with a Harbor implication.
- **Constraint backlog.** Eight to twelve items in the form "Because \[mechanism\], the product must \[behavior\], which we will see in \[artifact\]."
- **What this does not mean.** Three misconceptions you will stop using in meetings. Write the replacement sentence. Example misconception: "a bigger context window means we can drop retrieval." Replacement: a window is still a single request's working space, and edition-in-force is a record fact.
- **Question list for engineering.** Five questions that are fair for a PM to ask, such as where the edition-in-force fact is bound before generation, and what the token budget is for the draft call.

#### Flow

1. Draft the mechanism notes from memory first, then correct them against a reliable public source. Cite the source and the date. Correcting your own first draft is part of the project.
2. Turn each note into backlog items. If an item does not change a behavior a handler could notice, or a fact engineering must bind, cut it.
3. Write the misconception list from phrases you have actually heard or used.
4. On day 24, walk the backlog against the wizard-of-oz screen. Mark which constraints your screen already meets and which are new.

#### Tools and stack

Markdown, plus one or two public references (a model provider's guide to context windows, or a careful survey article). No training run, no notebook of matrix multiplies, and no framework tutorial. Those belong in a build curriculum. This artifact is the product backlog those constraints imply.

#### Setup

1. Create `harbor-portfolio/23-transformer-constraints/explanation.md` and `backlog.md`.
2. Timebox the first draft to 45 minutes before you open a reference, so you can see what you had wrong.
3. Day 23 is mechanisms and corrections. Day 24 is the backlog, the misconceptions, and the screen check.

#### Deliverables

- A two-page explanation a designer will actually read.
- A constraint backlog of eight to twelve items.
- A misconception list and five engineering questions.

#### What done looks like

A designer can point at a screen region that exists because of a constraint on the list. An engineer can see which facts must be bound before generation. The explanation does not include a formula, and it does not contain a false claim you left in after the correction pass. Your first-draft mistakes are fixed, not published.

#### Think a step ahead

Context windows and prices will change this year. Separate the backlog into items that survive a cheaper, longer context (authorship, no-source state, regenerate-destroys-edits) and items that are about today's limits (what fits in one call). Add a review date and the single public number that would make you retire an item. A constraint backlog that cannot expire will clog the roadmap after it stops being true.

#### Interview angle

Explain edition-in-force as a fact the model should be given, not a fact it should recall from a PDF. Then show two backlog items that follow from that sentence.

### Days 25–26 — Interaction Contract

Working copy and fixtures: [phase-03-ai-literacy/day-25-26-interaction-contract/README.md](phase-03-ai-literacy/day-25-26-interaction-contract/README.md)

**Days 25–26 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor proposes a claims note and citations. The handler at Northline Mutual is the author who commits the note to Lumen. The pilot episode is a new Ohio personal-auto physical-damage notice. Harbor does not decide coverage, set reserves, or message the claimant. Secondary readers include supervisors, investigators, and, later, defense counsel.

#### Concept

An interaction contract is the product's promise about behavior: what the handler may rely on, what the product will refuse to do, how a citation relates to a sentence, and what "commit" means in the system of record. It is the spec a prompt, a rubric, and a test plan all implement. It is written as observable behavior, so a reviewer can grade a draft against it without seeing the prompt that produced the draft.

Prompt text, model choice, and release mechanics change. The contract changes when the promise to the handler changes. Write it that way, and keep prompt wording in an appendix only if you need examples of acceptable and unacceptable outputs.

#### Approach

Write the contract as behaviors with acceptance examples and rejection examples. Every behavior has:

- a situation (the claim facts and the library state),
- the product's response,
- what the handler can do next,
- what is written to Lumen on commit, and who is recorded as author.

Cover at least these situations, using the Harbor episode:

1. One form edition is in force and a bulletin amends a limit. The draft uses the amended limit and cites both.
2. Two editions exist and only one was in force on the date of loss. The draft cites the in-force edition and does not quote the other.
3. The library has the form and does not yet have this morning's bulletin. The product says so and does not invent the amendment.
4. The handler asks Harbor whether the claim is covered. The product declines and points back to the note-drafting job.
5. The handler asks for a message to the claimant. The product declines.
6. The handler edits a paragraph and then asks to regenerate a different paragraph. The edit survives.

For each, include one unacceptable output. Unacceptable outputs are short and concrete. "The rental limit is $40 per day under the February form" when the fixture says $30 is an unacceptable output. "Hallucination" is a category, not an example.

Add the authorship clause in operational detail: the commit payload contains the handler's user id, a timestamp, the draft version they saw, and the citation ids they had available. Whether they opened them is a separate logged fact and is not, by itself, proof they agreed with the text.

#### Components

- **Promise statement.** Five sentences a handler could be shown during training.
- **Behavior table.** The six situations, acceptable response, unacceptable response, commit payload.
- **Reliance boundary.** What a supervisor may treat as evidence later (the signed note and the citations that were attached) and what they may not (the fact that a model was confident).
- **Change rule.** What kind of product change requires a contract revision: a new situation, a new reader, or a new write to Lumen. A model upgrade alone does not, unless the promise changed.
- **Examples appendix.** Optional. Labeled as illustrations, not as the spec.

#### Flow

1. Draft the promise statement in language a new handler will sit through during a twenty-minute training.
2. Fill the behavior table. Write unacceptable examples before acceptable ones. They are easier to dodge if you write the happy path first.
3. Write the reliance boundary for a supervisor reading the file six months later.
4. On day 26, try to break your own contract with a seventh situation you had not listed. Either add it or write why it is out of scope. Then mark which behaviors the wizard script already enforces.

#### Tools and stack

Markdown. The wizard script and the service blueprint as inputs. No prompt-engineering framework. If you later version prompts, this contract is the document those versions claim to implement.

#### Setup

1. Create `harbor-portfolio/25-contract/interaction-contract.md`.
2. Put the six situations in the file before you draft prose, so none get lost.
3. Day 25 is the promise, the table, and the reliance boundary. Day 26 is the seventh situation and the cross-check against the wizard script.

#### Deliverables

- An interaction contract with a promise statement, six behaviors, unacceptable examples, and a reliance boundary.
- A change rule of half a page.
- A gap list against the current wizard script.

#### What done looks like

A tester can build a case from each row without asking you what you meant. Unacceptable examples contain specific words, numbers, or actions. The authorship clause names the fields written on commit. Coverage and claimant messaging have explicit declines.

#### Think a step ahead

Counsel will ask what happens when a handler commits text the contract calls unacceptable, because the commit control is in human hands on purpose. Add an exceptions clause: the product does not block every risky sentence (it cannot know them all), the log retains the draft that was proposed versus the text that was committed, and a weekly sample reviews the gap. That clause is a product decision about responsibility, and it is the seed of the production quality ritual on days 85–86.

#### Interview angle

Read one unacceptable example and the commit payload. You are showing that you can specify model behavior as product behavior.

### Days 27–28 — Unit Economics and Latency Budget

Working copy and fixtures: [phase-03-ai-literacy/day-27-28-unit-economics/README.md](phase-03-ai-literacy/day-27-28-unit-economics/README.md)

**Days 27–28 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor proposes one note draft per new personal-auto claim for handlers in Columbus: 40 people. A new auto claim takes about 26 minutes today, about 9 of them spent finding the form. You do not yet know how many new auto notices that office opens in a week. You will treat that volume as an assumption and show how the decision moves when the assumption moves.

#### Concept

An AI feature can be loved in a pilot and unaffordable at the volume the pilot was meant to justify, or fast enough in a demo and too slow on the claims floor. Unit economics for Harbor means the cost of a successful drafted note, the latency a handler will tolerate inside a 26-minute task, and the gross margin of the pilot under assumptions you write down. The artifact is a spreadsheet a finance partner can audit, plus a one-page memo of what would change your recommendation.

#### Approach

Build the model from a few drivers, all visible:

- Notices per handler per day, as a range (low, base, high).
- Drafts per notice. The base case is one. The high case includes regenerations. State the regeneration assumption explicitly, because a sloppy interface multiplies the bill.
- Input and output tokens per draft, taken from the capability card's arithmetic, with the citation text counted in the output the handler sees.
- Price per token from the public price sheet you already dated, plus a second price column for a smaller model class.
- Handler minutes returned, as an assumption, not as a fact. Use a base of 4 minutes returned of the 9 spent searching, and show a case at 1 minute and at 8.
- Loaded handler cost per minute, as an assumption you label "finance must replace." Use a placeholder and never present it as Northline's real wage.

Latency budget, separate from cost: the draft appears within 8 seconds in the base case, matching the wizard script, and you define what the product does at 20 seconds (keep the handler in the note with a visible wait, or let them start typing and reconcile later). Pick one and say what it costs in abandoned drafts.

The output is a recommendation: pilot on the smaller class, pilot on the larger class, or do not pilot until volume and minutes-returned are measured. The recommendation has to cite a cell in the sheet.

#### Components

- **Driver sheet.** Every input in one column, with source or "assumption."
- **Scenario block.** Low, base, high, for weekly cost and for minutes returned.
- **Break-even note.** The minutes-returned figure at which base-case weekly cost equals assumed time saved, in the base volume. Show the formula in a sentence.
- **Latency policy.** The 8-second target, the 20-second behavior, and what you log when the wait exceeds it.
- **Decision memo.** Half a page. What you would pilot, what assumption flips the decision, and which number you will measure in week one rather than assume.

#### Flow

1. List drivers before you open a spreadsheet, so the sheet cannot grow a hidden cell that the memo never mentions.
2. Implement the sheet. Color or label assumptions differently from sourced prices.
3. Compute the three scenarios and the break-even minutes.
4. Write the latency policy and check it against the 26-minute handle time. A policy that saves search and then blocks the handler on a spinner has failed even if the cents look good.
5. On day 28, change one driver at a time and write down which single change flips the recommendation. That driver is the one the pilot must measure.

#### Tools and stack

A spreadsheet you can export to CSV, plus a short markdown memo. Public price pages. No cloud billing account. If you keep the sheet local, paste the assumption table into the memo so the portfolio still reads without the file.

#### Setup

1. Create `harbor-portfolio/27-economics/drivers.csv` and `memo.md`.
2. Reuse token assumptions from the capability card; if you skipped it, state new assumptions here and mark them as fresh.
3. Day 27 is the driver sheet and scenarios. Day 28 is break-even, latency policy, and the flip test.

#### Deliverables

- A driver sheet with sources and assumptions separated.
- Scenario costs, break-even minutes, and a latency policy.
- A decision memo that names the driver the pilot must measure.

#### What done looks like

A finance partner can recompute the base case from the driver table without asking you which cell mattered. The wage figure is labeled as a placeholder. The recommendation names the assumption that would reverse it. Latency has a handler-visible behavior, not only a percentile target.

#### Think a step ahead

A pilot at forty handlers can hide a distribution problem: a handful of long-tail claims pull whole forms into the prompt and dominate the bill. Add a tail policy. For example, drafts whose retrieved text exceeds a token ceiling you set fall back to "citations only, no prose," and those events are counted separately in the weekly cost. Write the ceiling, the fallback the handler sees, and how the weekly review would notice the tail eating the average. Days 39–40's dashboard is where that count should appear.

#### Interview angle

Quote the break-even minutes and the driver that flips the decision. Cost conversations that include the measurement plan are the ones that hold up in a review.

### Days 29–30 — Product Principles and Acceptable Use

Working copy and fixtures: [phase-03-ai-literacy/day-29-30-principles-and-use-policy/README.md](phase-03-ai-literacy/day-29-30-principles-and-use-policy/README.md)

**Days 29–30 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor proposes note text and citations for Northline Mutual handlers. The handler commits the note to Lumen under their own name. The pilot is personal auto in the Columbus office. Harbor does not decide coverage, set reserves, or message the claimant. The note may be read later by a supervisor, an investigator, or defense counsel.

#### Concept

Principles are the short list a team uses when a requirement conflicts with another requirement and nobody wants to reopen the whole spec. An acceptable-use policy is the handler-facing and manager-facing document that says what this tool is for, what it must not be asked to do, and what happens when someone asks anyway. Together they keep a pilot from drifting into a coverage engine because a regional manager requested it in week three.

This project writes both, specifically for Harbor. It also writes the decision rule for a request that violates a principle: who hears it, how fast, and what "no" sounds like when the requester is senior.

#### Approach

Write five principles, no more. Each principle has a meaning paragraph, a Harbor example of following it, and a Harbor example of breaking it. Candidates you should consider, and you may replace one if you can defend the replacement:

1. **The handler is the author.** Commit writes their identity, not the model's.
2. **Citations are part of the answer.** A paragraph the handler might rely on has a source they can open, or the product says it has none.
3. **The tool stays inside the note.** Coverage, reserves, and claimant communications are out, even when phrased as "just a draft for me."
4. **Absence is a result.** A missing bulletin is shown as missing. It is not filled with plausible language.
5. **Logs exist for the file, not for surprise.** Handlers know what is retained and who in the company can read a draft they discarded.

The acceptable-use document is two pages, written to a new handler and their supervisor. It includes how to cite Harbor in a note (the note is theirs; they do not write "per the AI"), what prompts are out of bounds, and what to do when the draft and the PDF disagree (the PDF and the published bulletin win; they escalate content bugs to a named alias).

The escalation rule covers a senior request to "just let it deny obvious glass claims." The artifact names the forum, the maximum time to decision, and the default during the wait, which is that the principle stands.

#### Components

- **Principle cards.** Five, with follow and break examples from the Harbor episode.
- **Handler page.** What this is, what you may ask, what you may not ask, how to commit, how to report a bad citation.
- **Supervisor page.** What an audit may rely on, what training to give in the first week, what not to measure (drafts per hour as a productivity contest).
- **Escalation rule.** Forum, clock, default-during-the-wait, and a sample reply to the senior request.
- **Conflict log template.** Date, request, principle touched, decision, decider. Empty and ready for the pilot.

#### Flow

1. Draft principles from the interaction contract. If a principle is not already implied by the contract, either update your understanding of the contract or drop the principle. They should not diverge silently.
2. Write the break examples first. They are the test that the principle is real.
3. Write the handler page out loud. Cut any sentence you would be embarrassed to read in a Monday standup on the claims floor.
4. Write the supervisor page, including the metric you refuse to put on a leaderboard.
5. On day 30, write the escalation sample and run it past a friend playing the regional manager. If your "no" is vague, rewrite it until the requester knows the request was declined and where it can be re-heard.

#### Tools and stack

Markdown. The interaction contract as source material. No policy-management product. The template for the conflict log is a table in the same file.

#### Setup

1. Create `harbor-portfolio/29-principles/principles.md` and `acceptable-use.md`.
2. Reread the prohibitions in the case before drafting. They are the non-negotiable core.
3. Day 29 is principles and the handler page. Day 30 is the supervisor page, the escalation rule, and the spoken test.

#### Deliverables

- Five principle cards with follow and break examples.
- A two-page acceptable-use document split for handlers and supervisors.
- An escalation rule and a conflict-log template, plus the sample reply.

#### What done looks like

A new handler can say what they must not ask Harbor to do, and a supervisor can say what an audit relies on. The sample reply to the senior request is specific. One metric is explicitly banned from the leaderboard, with a reason. Principles and the interaction contract do not contradict each other.

#### Think a step ahead

Principles written for a note-drafting pilot get pressure the moment a second team wants to reuse "the Harbor model" for a claimant-facing bot. Add a reuse gate: a one-page questionnaire another team must answer before they can call their feature a Harbor feature. Include intended reader, who the author is, what the model is forbidden to decide, and which principle would have to change. If a principle would have to change, the reuse is a new product decision, not a configuration. You will meet the same gate again in the platform-versus-feature bet on days 95–96.

#### Interview angle

Read the break example for "absence is a result," then the sample reply to the senior request. Both show you can hold a line in writing.

## Phase 4 — Decision Analytics

**Days 31–42 · Intermediate · 6 projects**

### Goals

This phase makes measurement a decision tool. You define the tree before the events, including the guardrail that can veto a faster handle time. You specify a tracking plan that can compute the tree without copying claim text into an analytics stream. You compute activation from a small fixture and reject a definition that counts generation as value. You write one memo where quotes and counts have to agree, a dashboard spec whose charts have allowed actions, and an experiment story that refuses sentences the result table cannot support. The phase is done when every headline number has a definition, a comparison, and a sentence you are willing to have repeated.

### Skills covered

Analytics and data analytics: metric trees, event tracking plans, funnel definitions, qualitative-quantitative triangulation, dashboard specification, experiment readout narrative.

### Days 31–32 — Metric Tree and Counter-Metrics

Working copy and fixtures: [phase-04-decision-analytics/day-31-32-metric-tree/README.md](phase-04-decision-analytics/day-31-32-metric-tree/README.md)

**Days 31–32 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor proposes a cited note for personal-auto handlers in Northline Mutual's Columbus office, and the handler commits it under their own name. Today's baseline is 26 minutes average handle time on a new auto claim, about 9 minutes of form-finding, and 3.1% of audited notes citing a form that was not in force. The pilot is 40 handlers. Harbor does not decide coverage.

#### Concept

A metric tree connects a decision you might take to a number you can move, and it pairs every efficiency number with a number that would reveal you had moved it by making the work worse. For Harbor, a drop in handle time is not success if the citation defect rises, if handlers commit drafts they did not read, or if supervisors bounce more notes. The tree is the agreement, made before the pilot, about which movements count.

You will define the tree, the decision each metric can trigger, and the metric you will refuse to call a success metric even if it goes up.

#### Approach

Start from decisions, not from events you happen to be able to log. Write three decisions the pilot might face in week six:

1. Expand beyond Columbus, hold, or stop.
2. Keep prose drafts, or fall back to citations-only.
3. Change the commit rule that asks the handler to open a citation.

For each decision, name the one metric that would push you toward the more aggressive option, the guardrail that can veto it, and the counter-metric that catches a hollow win. Example of a hollow win: median handle time falls because handlers paste the draft unread, while supervisor rework rises two weeks later. If your tree has no lagging quality metric, it will bless that outcome.

Define each metric in a sentence a second analyst could implement: numerator, denominator, who is in the population, and the window. "Engagement" does not qualify. "Share of new Ohio personal-auto notices in the pilot office, during a week, where the committed note's cited form edition matches the edition in force on the date of loss, among notes that were audited" is a definition. You may also define a proxy for the days when the audit sample has not landed yet, and you must label it as a proxy.

Write the baseline beside each metric where the case gives you one, and "unknown, measure in week 0" where it does not. Do not invent a baseline for draft acceptance.

#### Components

- **Decision list.** The three decisions above, possibly revised, each with the choice set.
- **Tree.** One north-star for the pilot, input metrics that should move first, guardrails, and counter-metrics. A sketch is fine if every node has a definition under it.
- **Definition table.** Name, numerator, denominator, population, window, baseline, owner.
- **Veto rule.** Which guardrail movement stops an expansion conversation even if handle time improved.
- **Refusal list.** Metrics you will compute, perhaps, and will not put in the executive sentence. Drafts generated per handler is a candidate for the refusal list, because it rewards regeneration.

#### Flow

1. Write the three decisions in language the VP of Claims Operations uses. If a metric cannot change one of those decisions, it does not go on the tree.
2. Draft the north-star. Test it against the hollow-win story. Adjust until the hollow win cannot look like success.
3. Fill the definition table. Have a second person try to implement one definition from the sentence alone. Revise the sentence where they get stuck.
4. Set the veto rule with a direction and a rough magnitude you would care about (for example, a rise in citation defects in the audit sample relative to the 3.1% baseline). You are setting attention, not a statistical test.
5. On day 32, write the refusal list and the week-0 measurement plan for every baseline you marked unknown.

#### Tools and stack

Markdown and a simple diagram (mermaid or indented text). A spreadsheet is optional and useful for the definition table. No analytics warehouse. You are defining measures, not querying production.

#### Setup

1. Create `harbor-portfolio/31-metric-tree/tree.md`.
2. Copy the case baselines into the file so you do not invent replacements.
3. Day 31 is decisions, tree, and definitions. Day 32 is the veto, the refusal list, and the week-0 plan.

#### Deliverables

- A metric tree tied to three pilot decisions.
- A definition table with owners and baselines or explicit unknowns.
- A veto rule and a refusal list.

#### What done looks like

The VP can read the veto rule without a briefing. Every metric on the tree has a definition another person could implement. At least one tempting metric sits on the refusal list with a reason. The hollow-win story is addressed by a node on the tree, not by a hope.

#### Think a step ahead

Audit sampling covers about 8% of notes in the case's spirit (supervisors sample notes; use 8% if you need a working figure, and label it as a planning assumption). A weekly citation-defect rate on that sample will bounce. Add a companion view you will not treat as a decision metric: the direction over four weeks, and the minimum number of audited notes you want before an expansion conversation. This is a measurement-design note, not a sample-size calculator. It stops a noisy week from looking like a quality collapse or a quality win.

#### Interview angle

Explain the hollow win and the node that catches it. Then name a metric you refused to celebrate.

### Days 33–34 — AI Interaction Tracking Plan

Working copy and fixtures: [phase-04-decision-analytics/day-33-34-tracking-plan/README.md](phase-04-decision-analytics/day-33-34-tracking-plan/README.md)

**Days 33–34 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor sits beside Lumen for Northline Mutual handlers. A handler opens a new personal-auto notice, requests a draft, sees citations, may edit, and commits a note under their own name. Discarding the draft and writing the note alone is an allowed outcome. The metric tree from days 31–32 is the list of decisions this tracking plan must be able to support.

#### Concept

A tracking plan names the events, properties, and identities a product will record so that a metric definition can be computed later without a rewrite. For a generative feature, the plan has to distinguish a draft the model proposed, a draft the handler edited, and the text that was committed. If you log only "note saved," you will never know whether Harbor changed the work.

This project writes the plan for the pilot episode. It also writes the events you will not log, because a claims note is sensitive, and "log everything in case we want it" is how a pilot becomes a privacy incident.

#### Approach

Define a small event vocabulary. Prefer a few events with strict properties over a dozen vague ones. A workable set:

- `notice_opened` — a new auto notice is opened by a handler in the pilot office.
- `draft_requested` — the handler asks Harbor for a draft on that notice.
- `draft_shown` — a draft was displayed, with a result state: `cited`, `no_source`, or `declined` (out of job, such as a coverage question).
- `citation_opened` — the handler opened a specific citation.
- `draft_edited` — the handler changed proposed text, with a coarse size of edit, not the text itself.
- `draft_discarded` — the handler threw the draft away.
- `note_committed` — Lumen received a note, with `used_draft` true or false, and the handler id as author.

Properties should include a notice id, a handler id, an office id, a draft version id, and timestamps. The plan states the join key that connects a commit to the draft version the handler saw.

Write an explicit exclusion list. Do not log the full note body, the claimant's free-text description, or the policy number in the product analytics stream. Those belong, if anywhere, in the claims system under its existing retention rules. The analytics stream carries identifiers a metric needs and a content class ("citation opened"), not the claim.

For each metric on your tree, write the event path that computes it, or write "cannot compute; definition or event missing" and fix one side. This crosswalk is the actual test of the plan.

#### Components

- **Event dictionary.** Name, when it fires, when it must not fire, required properties, id allowed to be joined.
- **Identity note.** Which id is a person, which is a claim, and who approves a new join.
- **Exclusion list.** Fields that feel useful and are out, with the reason.
- **Metric crosswalk.** Each tree metric mapped to events, plus gaps.
- **Data-quality checks.** Three checks a pipeline owner could run: drafts shown without a request, commits with an unknown draft version, citation opens after discard. These are product rules, not a pipeline implementation.

#### Flow

1. Start from the metric tree. List the events the definitions require before you invent any others.
2. Write the dictionary. For each event, write one case where it must not fire. Example: `draft_shown` does not fire when the wizard, in a test session, is a human. Pilot data and usability-test data stay in different streams.
3. Write the exclusion list with a privacy partner in mind. If you are alone, write the question you would ask them and take the stricter option in the meantime.
4. Build the crosswalk. Fix gaps by changing the event or by narrowing the metric. Say which you did.
5. On day 34, hand the dictionary to someone else and ask them to compute "share of shown drafts that were committed unedited" from your words alone. Revise wherever they have to guess.

#### Tools and stack

Markdown tables. No event-collection SDK and no warehouse. A CSV sketch of five fake rows, with no real personal data, is optional and useful for the crosswalk.

#### Setup

1. Create `harbor-portfolio/33-tracking-plan/plan.md`.
2. Paste the metric names from the tree at the top.
3. Day 33 is the dictionary, identities, and exclusions. Day 34 is the crosswalk and the second-person read.

#### Deliverables

- An event dictionary with must-not-fire cases.
- An exclusion list and an identity note.
- A metric crosswalk with gaps resolved, plus three data-quality checks.

#### What done looks like

An engineer can implement the events without inventing properties. A privacy reviewer can see that note text stays out of the analytics stream. Every north-star and guardrail metric has an event path or a written reason it waits on the audit sample instead.

#### Think a step ahead

Handlers will work around a clumsy commit path, and your events will then describe the workaround rather than the work. Add a "shadow path" note: how you would detect notes committed to Lumen with no Harbor events at all, using a count from the system of record compared with `note_committed`. Define the ratio and who looks at it weekly. A tracking plan that cannot see its own bypass will report a rosy adoption number while the real notes go around it. The analytics trust runbook on days 89–90 is the operational version of this worry.

#### Interview angle

Explain one field you refused to log, and the metric crosswalk entry that was hardest to support without it. That is product analytics judgment.

### Days 35–36 — Activation Funnel from a Fixture

Working copy and fixtures: [phase-04-decision-analytics/day-35-36-activation-funnel/README.md](phase-04-decision-analytics/day-35-36-activation-funnel/README.md)

**Days 35–36 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor is in a fictional first week with 12 Columbus handlers. A "successful first use" has not been defined yet, which is the problem. The office baseline you are trying to change is still the case baseline: time spent finding the form, and notes that cite a form not in force. This project uses a small event fixture, not a production warehouse.

#### Concept

Activation is the earliest handler behavior that predicts the job actually changed. For a generative assistant it is tempting to call "saw a draft" activation. That counts people the product talked at. A stronger definition for Harbor is closer to "committed a note that used a Harbor draft, after opening at least one citation, on a real notice." You will test candidate definitions against a fixture and write down which definition flatters the product.

The fixture is twelve handlers over a few days. It is small on purpose so you can compute by hand or in a spreadsheet and see every row that moves a number.

#### Approach

Read [`fixtures/copilot_events.csv`](fixtures/copilot_events.csv). Each row is one event. Compute, and show the handler ids behind each number:

- Handlers who opened at least one notice.
- Handlers who were shown at least one draft.
- Handlers who committed a note with `used_draft=true`.
- Handlers who opened a citation on a draft they later committed.
- Handlers who were shown drafts and never committed one (generate-and-ignore).
- Notes committed with `used_draft=false` after a draft was shown on the same notice (saw it, did the work themselves).

Propose two activation definitions. For each, report the rate and the list of handlers who would count as activated and, in your view, should not, or who would not count and should. Then choose a definition the pilot will use for the next four weeks, and write the decision it supports. A definition that everyone passes in week one cannot inform an expand-or-stop decision later.

Also write the trap explicitly: handler volume of `draft_shown` is not value. Identify the handler with the most drafts shown and describe their actual outcome from the rows.

#### Components

- **Population note.** Who is in the denominator. Handlers, or notices? Pick one for activation and say why. (A handler-level definition and a notice-level definition answer different questions. You will pick the handler-level one for "did this person get value," and you may report the notice-level one beside it.)
- **Count sheet.** Each figure above, with ids.
- **Definition choice.** Two candidates, the flattery check, and the choice.
- **Segment scribble.** Day-shift versus the single evening-shift handler in the fixture. Say what you will not conclude from a segment of one.
- **Instrumentation gap.** One thing you wish the fixture contained, tied back to the tracking plan. If the wish is "the note text," explain why you still will not put note text in the analytics stream, and what proxy you will accept.

#### Flow

1. Load the CSV into a spreadsheet or read it in a notebook. Do not aggregate until you have scanned the raw rows. Several handlers have patterns that disappear in an average.
2. Compute the counts and paste the id lists into the write-up so a reviewer can spot-check.
3. Draft two definitions and apply them.
4. Find the highest-volume drafter and write their story in four sentences from the rows alone.
5. On day 36, choose the definition and write a four-week rule: you will not change the definition mid-pilot unless the tracking plan was wrong. A moving definition makes the pilot incomparable to itself.

#### Tools and stack

A spreadsheet, or Python with pandas if you prefer. The fixture is the only data. No warehouse and no BI tool. If you use code, commit the snippet beside the write-up; the write-up still has to show the ids, so the conclusion does not depend on rerunning code.

#### Setup

1. Create `harbor-portfolio/35-funnel/`.
2. Copy [`fixtures/copilot_events.csv`](fixtures/copilot_events.csv) into it.
3. Day 35 is counts and the two definitions. Day 36 is the choice, the segment scribble, and the four-week rule.

#### Deliverables

- A count sheet with handler ids.
- Two activation definitions, a flattery check, and a choice.
- A note on the highest-volume drafter and one instrumentation gap.

#### What done looks like

A reviewer can recompute your chosen activation rate from the CSV and the id list. The definition does not treat `draft_shown` as value. The segment of one is described as a segment of one. The four-week rule is written down.

#### Think a step ahead

Week-one activation can be high because a facilitator sat with each handler, which the fixture quietly suggests via a burst of events on the first day for some ids. Add a "facilitated versus alone" flag to the tracking plan as a follow-on property, and write how you would split the metric once the flag exists. Until it exists, state that this fixture cannot support a claim about unaided use. Days 41–42 use the same discipline on an experiment story: say what the number cannot mean.

#### Interview angle

Show the id list behind the rate and the handler who generated the most drafts. You are demonstrating that you read the rows.

### Days 37–38 — Qual and Quant Triangulation Memo

Working copy and fixtures: [phase-04-decision-analytics/day-37-38-triangulation-memo/README.md](phase-04-decision-analytics/day-37-38-triangulation-memo/README.md)

**Days 37–38 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor's Columbus pilot has a metric tree, a tracking plan, and a week of fixture events. You also have the two practice transcripts from days 3–4, which describe the work before Harbor existed, and you may use one additional fictional observation from the wizard test: a handler committed a draft without opening the citation because the queue on their desk was "already behind." Treat that observation as a single usability note, not as a rate.

#### Concept

A triangulation memo answers one product question with two kinds of evidence, and it says where the kinds disagree. Numbers tell you how often a pattern appears in the logged population. Quotes and sessions tell you what the pattern meant to a person. Either one alone will support a confident, incomplete story. The memo is the place those stories have to sit in the same paragraph.

The question for this project: are handlers treating Harbor as a source they check, or as a text generator they paste?

#### Approach

Use only evidence you can point at:

- Counts and ids from the activation fixture.
- Quotes from the transcripts (Priya's fear of a sentence that sounds like a denial; Andre's wish that the tool "just does the note" because he is measured on closures).
- The single wizard observation, labeled as one session.

Structure the memo as three claims. Each claim has a quantitative clause, a qualitative clause, and a confidence line: supported, suggested, or contradicted. A claim can be suggested by a quote and unsupported by the fixture. That is a useful result. Write it that way, and name the next evidence that would promote it.

Include one disagreement on purpose. Andre's transcript predicts paste-without-reading from handlers under a closure metric. Your fixture either contains a handler who committed `used_draft=true` with `edit_size=none` and no `citation_opened`, or it does not. Look it up. Do not write the disagreement from memory. If the fixture and Andre agree, the disagreement you write should be a different one, for example a transcript pain the events cannot see (bulletin freshness), because no event records the bulletin date the handler needed.

Close with a decision the memo can support this week, and a decision it cannot. Expanding to a second office is a decision it cannot support. Changing the commit rule, or refusing to, might be a decision it can inform, if you state the evidence limit.

#### Components

- **Question.** One sentence.
- **Evidence inventory.** What you used, with paths, and what you refused to use.
- **Three claims.** Quant clause, qual clause, confidence, next evidence.
- **Disagreement paragraph.** The specific mismatch and the likely reason (different population, missing event, or a quote that was an opinion).
- **Decision box.** One action you would take in the pilot this month, and one action you would block, each tied to a claim.

#### Flow

1. Write the question at the top and do not change it after you see which answer is easier.
2. Pull the ids and counts you need from the fixture. Quote Andre and Priya with transcript ids.
3. Draft claims. Force each one through the confidence line. If both clauses are thin, the confidence is "suggested" at best.
4. Write the disagreement before the decision box, so the action has already survived the mismatch.
5. On day 38, cut the memo to two pages. Anything that does not serve the question moves to an appendix or disappears.

#### Tools and stack

Markdown. The fixture CSV, the transcripts, and your wizard observation note. No text-mining stack. With this much evidence, mining would be a way to avoid reading.

#### Setup

1. Create `harbor-portfolio/37-triangulation/memo.md`.
2. Open the fixture and the transcripts side by side.
3. Day 37 is inventory and claims. Day 38 is the disagreement, the decision box, and the cut.

#### Deliverables

- A two-page triangulation memo answering the question.
- An evidence inventory.
- A decision box with one move and one blocked move.

#### What done looks like

A reader can see which claims the fixture supports and which rest on a single quote. The disagreement names a concrete row pattern or a missing event. The blocked decision is one a stakeholder might actually push, and the memo says why this evidence is the wrong size for it.

#### Think a step ahead

Week-two interviews can contaminate the numbers if handlers change behavior because you sat with them. Add a short "evidence hygiene" note: interviews during the measurement window get logged against the handler id in a research log that is separate from the analytics stream, and any week that includes a facilitated session is marked before you read the funnel. This is the same facilitated-use problem as the activation follow-on, now applied to mixed-method work.

#### Interview angle

Walk a hiring manager through one claim's two clauses and the decision you blocked. The block is the judgment.

### Days 39–40 — Decision Dashboard Spec

Working copy and fixtures: [phase-04-decision-analytics/day-39-40-dashboard-spec/README.md](phase-04-decision-analytics/day-39-40-dashboard-spec/README.md)

**Days 39–40 · Phase 4, Decision Analytics · Intermediate**

**Case.** Harbor's pilot owner is the Columbus claims manager. She has twenty minutes on Monday morning. The VP of Claims Operations joins once a month and asks whether to hold, expand, or stop. Both of them need a dashboard. They do not need the same one. The underlying metrics are the tree from days 31–32, computed from the tracking plan, with audit results arriving later than product events.

#### Concept

A dashboard spec is a decision tool described on paper: the question the page answers, the person who answers it, the chart or figure that answers it, the comparison that makes the figure mean something, and the action that is allowed from this page. A chart without an allowed action is a poster. This project specifies two pages, manager and VP, and the page you will not build.

You will not implement a BI tool. A spec that names sources, windows, and the sentence under each figure is the product work. Implementation can follow in whatever stack the company already uses.

#### Approach

For every figure, write five lines:

1. Decision it serves.
2. Metric definition name, matching the tree exactly. If the name is new, the tree is incomplete; go back and add it there first, or drop the figure.
3. Comparison: versus the prior week, versus the 3.1% citation baseline, or versus the citations-only fallback. A number without a comparison does not go on the page.
4. Freshness: when the figure can be wrong because audit results lag, or because Friday's library index has not run.
5. Allowed action: what this person may decide from this figure alone, and what they must not.

The manager page is operational. Include the tail-cost count from the unit-economics follow-on if you wrote one (drafts over the token ceiling), the share of commits with no citation opened, the no-source rate, and a list of notices where the draft was discarded. She can act on coaching and on content bugs.

The VP page is the three-decision page: expand, hold, or stop. It shows the north-star, the veto guardrail, and the counter-metric, each with the comparison, and it shows sample size in audited notes so a noisy week cannot look precise. It does not show drafts per handler.

Specify an empty state for week 0 and a degraded state for "audit file late." Degraded is a designed page, not a blank chart.

#### Components

- **Audience and cadence.** Who opens which page, which day, for how long.
- **Figure list.** The five-line block for each figure. Six figures is enough. More than eight means you are designing a poster.
- **Layout note.** What is above the fold for a laptop screen the manager actually has. One sentence on what a phone view would drop.
- **Degraded and empty states.** Copy for "not enough audited notes" and "pipeline late," including who gets notified.
- **Will-not-build list.** At least three charts a stakeholder is likely to request, and the reason each is absent. Leaderboards of handlers by speed belong here.

#### Flow

1. Write the allowed actions for each audience before you pick charts. Actions constrain figures.
2. Select figures from the metric tree only.
3. Write comparison, freshness, and degraded copy for each.
4. Draft the will-not-build list by imagining the VP's staff meeting. Put the flattering charts there.
5. On day 40, read the spec as if the audit file failed to arrive. Confirm the Monday page still tells the manager what to do this week, and tells the VP that the monthly decision waits.

#### Tools and stack

Markdown. Optional wireframe in mermaid or a rough grid. No BI license. If you later build the page, the spec remains the source of what the page is allowed to cause.

#### Setup

1. Create `harbor-portfolio/39-dashboard/spec.md`.
2. Have the metric names in front of you. Do not rename them in the spec.
3. Day 39 is audiences, actions, and figures. Day 40 is degraded states, the will-not-build list, and the late-audit read-through.

#### Deliverables

- Two page specs, manager and VP, with five-line figure blocks.
- Empty and degraded copy.
- A will-not-build list.

#### What done looks like

A designer can lay out the page without inventing a metric. An analyst can see the freshness risk on the citation figure. The VP page cannot be used to rank handlers. The Monday page still has an allowed action when the audit file is late.

#### Think a step ahead

A dashboard that becomes a target will be gamed. Handlers who learn that "citation opened" is on the manager page may click a citation and not read it. Add a note on the metric you will watch for that gaming, such as citation opens with a time-to-close under a threshold you set, and the conversation you will have if it moves. Write the threshold as a hypothesis. This is a product risk of measurement, and it belongs in the spec so the page does not pretend to be neutral.

#### Interview angle

Describe one chart you left off and the allowed action on the chart you kept. Dashboard work is the editing.

### Days 41–42 — Experiment Story Memo

Working copy and fixtures: [phase-04-decision-analytics/day-41-42-experiment-story/README.md](phase-04-decision-analytics/day-41-42-experiment-story/README.md)

**Days 41–42 · Phase 4, Decision Analytics · Intermediate**

**Case.** Northline ran a four-week pilot comparison inside the Columbus office. Handlers were split by pre-assigned rotation, not by who volunteered. The treatment group used Harbor. The control group used Lumen and the shared drive, as before. You are not designing the study and you are not computing a sample size. You have been handed a result table, and your job is the decision narrative: what the company may claim, what it must not claim, and what it will do next.

#### Concept

An experiment story memo translates a result table into a claim with a strength that matches the evidence, written for people who will repeat a simpler version of your sentence in a room you are not in. The risk is a true number turned into a false sentence. "Handle time fell by 3.2 minutes" can be a measured difference and still be the wrong sentence, if the citation defect moved the wrong way, if the groups were small, or if the people in the room will hear "Harbor makes claims faster" and take it to another line of business.

#### Approach

Use this result table as given. Do not "fix" it. The story has to live with the awkward cells.

| Measure | Harbor (n=19 handlers) | Control (n=18 handlers) | Notes |
| --- | --- | --- | --- |
| Median handle time, new Ohio auto notice | 22.1 min | 25.4 min | Means were 24.0 and 25.6. Two Harbor handlers had medians under 12 min. |
| Citation defect in audited notes | 4 of 41 notes (9.8%) | 3 of 38 notes (7.9%) | Audit continued at the usual sample. Baseline before the pilot was 3.1% in a much larger quarter. |
| Supervisor bounce-back within 2 days | 11% of notes | 9% of notes | Bounce reasons were not coded. |
| Draft committed with a citation opened | 61% of Harbor notices | — | Control had no drafts. |
| Handler voluntary opt-out | 1 handler, week 2 | 0 | The opt-out said the draft "got in the way on glass-only claims." |

Write the memo in five parts:

1. **What we did,** in one paragraph, including who was in and the episode fence (Ohio personal auto, Columbus).
2. **What moved,** stating direction and size, with the n next to every percentage.
3. **What we will say in the staff meeting,** a single sentence you are willing to have repeated.
4. **What we will not say,** at least four sentences people will want, rewritten as refusals. Include a refusal to claim the 3.1% baseline was beaten, a refusal to claim statistical proof you were not given, and a refusal to generalize past glass-only or past Ohio.
5. **What we will do next,** one bet. The bet has to follow from the awkward cells, not from the flattering median. The higher citation defect and the glass-only opt-out are the point of the table.

You may describe the median difference as a measured difference in this pilot. You may not call it a proven causal effect, because no inferential statistic was handed to you. If a partner brings you a p-value later, the story structure stays; the claim strength can be revisited. This memo is about claim hygiene under a fixed table.

#### Components

- **Result appendix.** The table, unchanged, with the date you received it ("given with the project").
- **Staff sentence.** One sentence.
- **Refusal list.** Four or more forbidden sentences, each with the cell that makes it forbidden.
- **Next bet.** One change to the pilot, with the metric that would tell you the bet worked, using a definition you already have.
- **Audience note.** What the VP version omits, and what the handler-training version adds. The numbers do not change between audiences. The advice does.

#### Flow

1. Copy the table into the memo. Read it twice before you write a sentence of interpretation.
2. Draft the staff sentence. Then try to make it more exciting, and reject your own revision if the excitement is not in the table.
3. Write the refusals by imagining a launch announcement. Every adjective in that announcement is a candidate for the refusal list.
4. Choose the next bet from the defect rate or the glass-only comment, and name the metric.
5. On day 42, have someone else repeat the staff sentence from memory after one reading. If they remember a claim that is on your refusal list, the sentence is too easy to over-read and you rewrite it.

#### Tools and stack

Markdown. A calculator only if you want to restate a percentage; the table already has the rates. No experimentation platform. The skill is the narrative and the refusals.

#### Setup

1. Create `harbor-portfolio/41-experiment-story/memo.md`.
2. Paste the table exactly.
3. Day 41 is the five parts. Day 42 is the memory test and the rewrite.

#### Deliverables

- An experiment story memo with the table, the staff sentence, the refusals, and one next bet.
- A one-paragraph note on what the memory test did to the sentence.

#### What done looks like

The staff sentence can be repeated without smuggling in a proof you do not have. Every refusal points at a cell. The next bet responds to the citation defect or the glass-only opt-out, not only to the faster median. Sample sizes appear next to the claims that need them.

#### Think a step ahead

The opt-out names a slice, glass-only, where the draft may be a tax. The table does not break handle time or defects out by claim subtype. Specify the next readout you would require before acting on that comment: the same measures, split by glass-only versus repairable collision, with a minimum cell size below which you will report "not split" rather than a rate. Write that minimum as a reporting rule. This is how a story memo becomes a request for the next cut, instead of a license to invent the cut from one comment.

#### Interview angle

Read the staff sentence and one refusal. Offer the next bet only if they ask what you would do. The restraint is the signal.

## Phase 5 — Delivery for AI Products

**Days 43–52 · Intermediate · 5 projects**

### Goals

This phase runs Harbor as a ten-week pilot with gates, not as a percent-complete build. You assign one accountable owner per gate and say which prohibitions cannot be waived. You sum the lead times you do not control and change the plan when the chain does not fit. You write sprint goals that fail or pass on evidence, a data-rights log whose unresolved rows change product behavior, and the communications system for the week a gate is late. The phase is done when a missed content owner produces a same-day handler message and a slip plan, not a quiet slide that still says the model is coming.

### Skills covered

Project management: evidence-gated milestones, dependency and critical-path planning, sprint goals under uncertainty, RAID for data rights, stakeholder communication systems.

### Days 43–44 — Milestone Map and RACI

Working copy and fixtures: [phase-05-delivery/day-43-44-milestone-map/README.md](phase-05-delivery/day-43-44-milestone-map/README.md)

**Days 43–44 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** Northline has agreed to a ten-week Harbor pilot in Columbus for new Ohio personal-auto notices. The handler signs the note. The interaction contract, metric tree, and acceptable-use page exist as drafts. Engineering has not started a production integration with Lumen. Content operations has not named an owner for bulletins. Legal has not signed the reliance boundary.

#### Concept

A milestone map for an AI feature is a sequence of evidence gates, not a sequence of build percentages. "Model integration 60% complete" can be true while nobody has agreed what the handler is allowed to rely on. This project writes the gates for the ten-week pilot, the artifact that proves each gate, and a RACI that gives every gate one accountable owner. Dates are included because a gate without a week is a wish. The dates are a plan you are willing to revise when a gate fails, not a promise that the model will cooperate.

#### Approach

Use six gates. You may rename them, and you may not drop the evidence each one asks for:

1. **Contract freeze.** The interaction contract's six behaviors are accepted by claims operations, with the reliance boundary initialed by legal. Proof: signed contract version.
2. **Content owner.** A named person publishes and withdraws Ohio personal-auto forms and bulletins for the pilot, on a stated cadence. Proof: owner name and the first published set's date.
3. **Wizard week.** Five handlers complete the usability tasks, including a reject-the-draft task, on the scripted interface. Proof: observation sheets and the change list.
4. **Offline eval bar.** A gold set you will define later passes a bar you write in plain language this week (for example, no unacceptable output on the coverage-decline behavior in the contract). Proof: the bar, written now, and a placeholder for the report.
5. **Shadow week.** Harbor produces drafts that are stored and not shown as the default note, or are shown to a facilitator-side reviewer only. Proof: a written rule for what shadow may not do, which includes "may not be pasted into Lumen."
6. **Limited pilot.** Forty handlers, Ohio personal auto only, with the dashboard's degraded state defined and the veto rule in force. Proof: the go document, one page, signed by the accountable owner.

RACI rows are the gates plus three cross-cutting concerns: Lumen commit payload, analytics exclusions, and handler training. Roles to include: product, claims operations, content operations, engineering, legal, security, and the Columbus manager. Exactly one A per row. If legal and product both want the A on the contract, the map has not decided.

#### Components

- **Gate table.** Gate, week number, proof artifact, what "fail" means, and the only person who can waive the gate.
- **RACI.** One A per row, with R, C, and I filled for the real functions above.
- **Waiver rule.** A waiver is written, expires in one week, and cannot waive the prohibition on coverage decisions or claimant messaging. Some gates are waivable. Those two prohibitions are not gates; they are scope.
- **Slip plan.** If the content owner is unnamed by the end of week 2, what the other work is allowed to do in the meantime. The answer is not "build the integration anyway and hope."

#### Flow

1. Place the six gates on a ten-week line. Leave slack between wizard week and the limited pilot. A map with no slack is a wish.
2. Write the fail condition for each gate as a concrete missing artifact.
3. Fill the RACI. Read down the A column. If one person holds every A, redistribute or acknowledge the bottleneck in writing.
4. Write the waiver rule and the week-2 slip plan.
5. On day 44, walk the map with someone playing legal and someone playing the Columbus manager. Note the first gate they each think is "just a formality." That gate needs a clearer proof, or it will be skipped.

#### Tools and stack

Markdown tables. A one-page timeline in mermaid is optional. No project-management suite is required to finish the artifact. If the company lives in a tracker, the map is still the source, and tickets are copies.

#### Setup

1. Create `harbor-portfolio/43-milestones/map.md`.
2. Put the ten-week boundary in the header so scope does not grow a quarter while you plan.
3. Day 43 is gates and proofs. Day 44 is RACI, waiver, slip plan, and the two-role read.

#### Deliverables

- A ten-week gate map with proofs and fail conditions.
- A RACI with a single A per row.
- A waiver rule and a slip plan for a missing content owner.

#### What done looks like

A program review can tell, for each week, which artifact must exist and who is accountable. The prohibitions cannot be waived. The slip plan keeps engineering from integrating a library nobody owns. Someone other than product holds at least one A.

#### Think a step ahead

Shadow week is where teams quietly start showing drafts to handlers "just to learn." Add a shadow integrity check: a named reviewer compares the count of drafts produced with the count of drafts that reached a Lumen note, and any match is a failed gate, not a funny story. Write the query in words (which two counts, who runs it daily, what they do on a mismatch). This is the delivery control that makes the word "shadow" mean something.

#### Interview angle

Point at the gate you will not let a senior stakeholder waive, and at the A that is not you. Delivery judgment is the boundary and the owner.

### Days 45–46 — Dependency Map and Critical Path

Working copy and fixtures: [phase-05-delivery/day-45-46-dependency-map/README.md](phase-05-delivery/day-45-46-dependency-map/README.md)

**Days 45–46 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** The Harbor ten-week pilot depends on people who do not report to product: Lumen integration, the Ohio forms publisher, legal review of the reliance boundary, a model vendor or an internal model host, security review of logs, and handler training time on the Columbus floor. Training time is a dependency. The floor does not have a spare hour because a plan assumed it did.

#### Concept

A dependency map lists the work that has to be true before a gate can be true, including work your team does not do. The critical path is the longest chain of those dependencies that still fits inside ten weeks, plus the chain that does not fit, which you then change the plan to remove. This project is a written map and a conversation plan for the two dependencies most likely to slip. It is not a scheduling product and not a Gantt as performance art.

#### Approach

Build the map at the level of deliverables, not tasks. "Legal initialed reliance boundary" is a deliverable. "Schedule a meeting with legal" is a task and does not belong on the critical path until the deliverable's real wait time is the review queue, in which case the queue itself is the dependency and you write its lead time.

For each deliverable, record:

- the producing team,
- the lead time they have already told you, or "not yet asked,"
- the consuming gate from the milestone map,
- whether the dependency is hard (the gate is impossible) or soft (the gate is weaker without it),
- the fallback if it misses.

Hard dependencies for Harbor include the commit payload's author field in Lumen, the named content owner, and legal's position on what a supervisor may rely on. A model endpoint is hard for the limited pilot and soft for wizard week, which is the reason wizard week exists. If your map makes the model endpoint hard for wizard week, you have erased your own de-risking.

Find the critical path by hand. With this many nodes you can list chains in a table and sum lead times. Identify the chain that threatens week 10, and rewrite the plan so the chain no longer threatens it: reduce scope, start the wait this week, or move the gate. A map that only admires the risk is unfinished.

#### Components

- **Deliverable list.** About fifteen items, with producer, lead time, gate, hard or soft, fallback.
- **Chain table.** Three or four chains with summed weeks, and a mark on the longest one that sits on the way to the limited pilot.
- **Two-conversation plan.** For the riskiest hard dependency and the one your team has been treating as soft and should not. Each conversation has an ask, a lead time you need, and the fallback you will state out loud.
- **Path change.** The edit you made to the milestone map after seeing the sum. Quote the old week and the new week.

#### Flow

1. List deliverables by walking each gate and asking "what must exist that we do not build alone?"
2. Mark hard or soft. Check wizard week specifically. The model must not be hard there.
3. Sum chains. Show the arithmetic.
4. Rewrite one date or one scope item. Record the edit.
5. On day 46, draft the two conversations as scripts of less than a dozen lines each. Ask a partner to play the content owner who says their queue is six weeks. Your script has to survive that answer because the fallback was real.

#### Tools and stack

Markdown. A whiteboard photo is optional. No scheduling suite. Lead times are numbers in a table, which is enough to see a ten-week collision.

#### Setup

1. Create `harbor-portfolio/45-dependencies/map.md`.
2. Start from the six gates so every dependency has a consumer.
3. Day 45 is the list and the chains. Day 46 is the path change and the two scripts.

#### Deliverables

- A deliverable-level dependency list with hard and soft marks.
- A chain table with arithmetic and one path change.
- Two conversation scripts that include a fallback.

#### What done looks like

The longest chain is visible as a sum, and the milestone map changed because of it. Wizard week does not depend on a production model endpoint. Each risky conversation states a fallback the other team can believe, because it is something you will actually do.

#### Think a step ahead

Vendor model hosts change versions on their own calendar. Add the vendor's model version as a named dependency with a lead time of "unscheduled." Write the pilot rule: a version change during the limited pilot pauses drafts and returns handlers to the control path until the offline bar is re-run on the new version. Name who is watching the version string. This is a dependency on a thing you do not control, which is the usual shape of the dependency that actually hurts.

#### Interview angle

Show the chain sum and the date you moved. Then the fallback in the script. Planning is the change you made after the arithmetic.

### Days 47–48 — Sprint Goals under Uncertainty

Working copy and fixtures: [phase-05-delivery/day-47-48-sprint-goals/README.md](phase-05-delivery/day-47-48-sprint-goals/README.md)

**Days 47–48 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** A six-person Harbor squad (product, three engineers, one designer, one content analyst) works in two-week sprints inside the ten-week pilot. The squad does not control legal's queue or the Columbus floor's training hour. The current goal someone proposed in a planning meeting was "finish draft API and start UI." That proposal is the problem this project fixes.

#### Concept

A sprint goal for probabilistic work states the evidence the squad will have at the end of the sprint, not the tickets they will touch. "Finish the draft API" can be done while the draft still invents a rental limit. A goal written as a quality bar ("every fixture in the coverage-decline set returns the decline behavior, on the build we demo") can fail honestly, and a failure you can see is worth more than a burndown that looks complete.

This project writes two consecutive sprint goals, the non-goals that keep them small, and the cut rule for mid-sprint when a fixture fails. It does not design a board, a burndown, or a velocity report. Those are a different tool, and the squad may already have one. The contract of the sprint is the document.

#### Approach

Sprint A is the sprint that produces the wizard-week build: the screen regions, the commit control, the no-source state, and a human or scripted stub where the model will later sit. The goal is about a facilitator being able to run the five usability tasks. It is not about a model quality number the stub cannot earn.

Sprint B is the first sprint where model output is graded. The goal names a fixture slice and a bar, for example: "On the twenty bulletin-amendment items, the build we demo cites the bulletin and the in-force edition, and it produces zero coverage-decision sentences." You will not have that fixture fully specified until later projects; write the goal with a named slice and leave the item count as a number the content analyst owns. The point is the shape of the goal.

For each sprint, write:

- the goal in one sentence a handler would recognize,
- three to six backlog themes that serve it, without turning this document into a ticket dump,
- non-goals, including at least one item a stakeholder asked for,
- the demo: who attends, what they see, what would count as the goal failing in the room,
- the cut rule: if by day 6 the fixture is not ready, what the squad drops first (the prose draft, not the citation panel, or the reverse — choose and justify).

Add a note on what the squad will not use as a substitute for the goal. Ticket completion, story points burned, and "the demo looked good" are the substitutes to ban in writing.

#### Components

- **Two goal cards.** Goal, themes, non-goals, demo, cut rule.
- **Substitute ban.** The metrics that will not be read out as progress in the standup.
- **Dependency callout.** Which goal depends on the content analyst having items, and what Sprint B's goal becomes if those items slip. The fallback goal is still evidence-shaped.
- **Planning agenda.** A 45-minute agenda that starts from the goal and ends with the cut rule, so planning does not start from a backlog sort.

#### Flow

1. Rewrite the rejected goal ("finish draft API and start UI") as the evidence it was trying to imply. Notice how many different evidences it could have meant.
2. Write Sprint A's card against wizard week. Check that a stub model can still satisfy it.
3. Write Sprint B's card against a named behavior in the interaction contract.
4. Write the fallback goal if the fixture slips, and the substitute ban.
5. On day 48, run the 45-minute agenda with a friend playing an engineer who wants to pull in claimant messaging "since the API is right there." The non-goal and the cut rule should make that a short conversation. If they do not, revise them.

#### Tools and stack

Markdown. The milestone map as the source of what these sprints serve. No sprint tool. A tracker ticket is optional afterward; the goal card is the authority.

#### Setup

1. Create `harbor-portfolio/47-sprint-goals/goals.md`.
2. Put the rejected goal at the top, so the contrast with your cards stays visible while you write. You may delete it in the final version or keep it labeled as the rejected starting point.
3. Day 47 is the two cards. Day 48 is the fallback, the ban, the agenda, and the role-play.

#### Deliverables

- Two sprint goal cards with non-goals, demos, and cut rules.
- A fallback goal and a substitute ban.
- A 45-minute planning agenda and a note from the role-play.

#### What done looks like

Someone reading Sprint B knows how Friday's demo can fail. The cut rule names what is dropped first. Claimant messaging cannot sneak in as a theme. Progress is described as evidence, and the banned substitutes are written down.

#### Think a step ahead

The content analyst who owns the fixture may sit outside the squad and serve three teams. Write a capacity assumption for their hours in these two sprints, and the goal change if you get half of those hours. A goal that treats another team's specialist as infinite will fail in week 2 and be narrated as a model problem. Naming the hours now keeps the failure attached to the real constraint.

#### Interview angle

Read Sprint B's goal and its cut rule. Then say what you banned as a progress metric. That trio is the sprint contract.

### Days 49–50 — Data-Rights and Vendor RAID

Working copy and fixtures: [phase-05-delivery/day-49-50-data-rights-raid/README.md](phase-05-delivery/day-49-50-data-rights-raid/README.md)

**Days 49–50 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** Harbor's drafts are produced by a hosted model. Prompts will include claim facts and excerpts of policy forms. Notes are committed to Lumen. Handlers' edits might, later, be useful as evaluation items. Northline's counsel has not yet said whether a vendor may retain prompts, whether policy forms may be sent to that vendor, or whether a handler's edit can be used to evaluate a model. The pilot clock is running.

#### Concept

A RAID log for this kind of pilot is a working list of risks, assumptions, issues, and dependencies that can make the pilot unlawful, untrustworthy, or silently dependent on a vendor's terms. It is updated on a cadence during delivery. It is not a launch workshop and not a one-time premortem. The value is the owner, the next review date, and the decision you will force when a row stays red.

You will write the log for data rights and vendor terms, seed it with rows that are specific to Harbor, and write the weekly review ritual that keeps it alive for the ten weeks.

#### Approach

Create rows only where a pilot behavior meets a rights question. Seed at least these, and add more if you can make them concrete:

- Policy form text leaving Northline's network for a vendor prompt.
- A claimant's free-text loss description leaving the network. Your tracking plan already keeps it out of analytics; the prompt is a different path and needs its own row.
- Vendor retention of prompts and outputs, including what "zero retention" means if a status page is the only evidence.
- Whether handler edits may be stored for an eval set, who the employer is relative to the handler, and what the acceptable-use page promised.
- A vendor model-version change mid-pilot (connect this to the dependency follow-on).
- Training-data clauses in the vendor contract: whether Northline's prompts may be used to train a model other customers use.
- A subprocessor the vendor adds during the ten weeks.

Each row has: statement, class (risk, assumption, issue, dependency), evidence you have today, owner, next action, review date, and the decision if the row is still unresolved seven days before the limited pilot. That last field is what makes the log operational. "Monitor" is not a decision. "Ship citations-only with no prose, because prose requires sending loss descriptions" is a decision.

Assumptions are written so they can be false. "Counsel will allow form excerpts to be sent" is an assumption until a written note exists, at which point the row becomes a closed issue with the note attached.

#### Components

- **RAID table.** At least eight rows with the fields above.
- **Decision calendar.** The seven-day-before-pilot meeting: who must attend, which rows are in scope, what the default is if counsel has not replied (the stricter product behavior).
- **Weekly ritual.** Fifteen minutes. Which rows are read (only red and newly closed), who updates evidence, where the log lives.
- **Handler-promise check.** A column or a note that compares each row with the acceptable-use page, so the log cannot approve a use the handlers were told would not happen.

#### Flow

1. Walk one Harbor draft from notice opened to vendor call to commit. Every time data crosses a boundary, start a row.
2. Fill owner and next action. An owner of "legal" is incomplete; name the function and the product person who chases the function.
3. Write the unresolved decision for each row as a product behavior change, not as "escalate."
4. Compare the rows with the acceptable-use page. File a conflict if you find one.
5. On day 50, run the fifteen-minute ritual on your own log as a dry run. Close one row by writing the evidence that would close it, and leave the others honestly open. A log that closes everything in a classroom exercise has been sanitized.

#### Tools and stack

Markdown or a spreadsheet with the columns above. No GRC platform. The ritual matters more than the database. Link the acceptable-use document by path so the promise check is real.

#### Setup

1. Create `harbor-portfolio/49-raid/raid.md`.
2. Draw the data-boundary walk on paper first: handler, Lumen, Harbor service, vendor, eval store.
3. Day 49 is the boundary walk and the rows. Day 50 is decisions, the promise check, the ritual, and the dry run.

#### Deliverables

- A RAID log of at least eight data-rights and vendor rows.
- A decision for each row if it is still open seven days before pilot.
- A fifteen-minute ritual and a note from the dry run.

#### What done looks like

Every row can change a product behavior, and that behavior is named. The default when counsel is silent is the stricter path. Handler-facing promises and the log have been compared. At least one row is still open at the end, with an owner and a date.

#### Think a step ahead

A zero-retention clause does not settle what the vendor's status page, support staff, or abuse-monitoring pipeline can see. Add a row for human access inside the vendor: who at the vendor can read a prompt, under what incident, and what notice Northline receives. Write the pilot behavior if that notice term is missing from the contract (for example, no loss-description text in the prompt, excerpts of forms only). The follow-on is about people at the vendor, not about the model.

#### Interview angle

Walk one row from the data boundary to the product behavior you would ship if the row stays red. That is risk management a PM owns.

### Days 51–52 — Stakeholder Communication System

Working copy and fixtures: [phase-05-delivery/day-51-52-stakeholder-comms/README.md](phase-05-delivery/day-51-52-stakeholder-comms/README.md)

**Days 51–52 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** Harbor has a ten-week pilot, a gate map, a RAID log, and a VP who will repeat one sentence in a staff meeting. The audiences who can help or stall the work are the VP of Claims Operations, the Columbus manager, the handler crew, legal, the content owner, engineering, and security. They do not need the same update, and they will invent one if you do not write it.

#### Concept

A communication system is the set of artifacts, cadences, and owners that keeps each audience informed enough to do their part and not so informed that they act on a rumor. It includes the note you send when a gate fails. Teams write launch announcements and forget the failure note, which is the one that protects trust.

This project specifies the system for the Harbor pilot and writes the actual templates, filled with realistic pilot content, including a gate-failure note. It is outbound communication design. It does not analyze the sentiment of replies.

#### Approach

Define six touches:

1. **VP one-pager, monthly.** The staff sentence from the experiment story, or, before any experiment exists, the gate status and the veto rule. One page. No model architecture.
2. **Columbus manager note, weekly.** What changed on the floor, what you need from her (training hour, a handler's time), and which RAID row needs a claims decision.
3. **Handler briefing, at gate transitions only.** Plain language. What they will see, what they remain responsible for, how to report a bad citation. Not a weekly marketing email. Handlers are in production; respect the queue.
4. **Legal and security digest, at contract and vendor changes.** The diff in the promise, not a full restatement. Link the RAID rows that moved.
5. **Build review, twice a sprint.** The sprint goal, the evidence, the cut. Internal.
6. **Gate-failure note, same day.** What failed, who is accountable, what handlers should do tomorrow (usually "work as before"), and the next decision date. This template is written now, while nobody is ashamed of it.

Write each template filled, not blank. Use week 3 of the pilot as the scenario: the content owner has not delivered the bulletin ingest, wizard week is at risk, and no handler-facing behavior has changed. The VP note has to say that without sounding like an excuse and without implying the model is late. The model is not the late part.

Add a rumor rule. If the Columbus manager hears a different story than the handler briefing, the system has failed. Name the single source: a page everyone can open, with a status line that uses the gate names from the milestone map. The templates point at that line rather than inventing new status words.

#### Components

- **Audience table.** Audience, decision they make, cadence, template, author, approver.
- **Six filled templates.** Using the week-3 scenario for the recurring ones, plus the failure note for the missed content-owner gate.
- **Status line vocabulary.** The gate names and the only adjectives allowed (not started, blocked, passed, waived with a link). Ban "on track."
- **Rumor rule.** The source page and what you do when two messages diverge: which one you correct, and how fast.

#### Flow

1. List the decision each audience actually makes. Cut any touch that serves no decision. A FYI with no decision is a candidate to delete.
2. Write the status vocabulary from the milestone map before you write prose, so every template uses it.
3. Fill the templates for week 3. Read the handler briefing and the VP note back to back. The facts must match.
4. Write the failure note for the missed bulletin ingest. Include what handlers do tomorrow.
5. On day 52, show the VP note and the handler briefing to a partner. Ask them what is late. If one of them says "the model," rewrite until the late dependency is the content owner.

#### Tools and stack

Markdown. A shared page can be a document with a status line at the top; no intranet project is required to specify the system. The filled templates are the deliverable.

#### Setup

1. Create `harbor-portfolio/51-comms/system.md` with one section per touch.
2. Keep the milestone gate names visible while you write.
3. Day 51 is the audience table, vocabulary, and the recurring templates. Day 52 is the failure note, the rumor rule, and the partner read.

#### Deliverables

- An audience table tied to decisions.
- Six filled templates, including a same-day gate-failure note.
- A status vocabulary and a rumor rule.

#### What done looks like

The week-3 VP note and the handler briefing agree on what is late. "On track" does not appear. The failure note tells handlers how to work tomorrow and names a decision date. Every touch has an author. At least one audience you considered did not get a recurring email, and the table says why.

#### Think a step ahead

The first time a committed note cites a withdrawn form, the communication system becomes an incident system. Add a one-page incident addendum: who declares it, which audiences hear it within an hour (Columbus manager and legal, not the VP first), what handlers are told to do with drafts already on screen, and when the status line changes. Write the handler sentence now. You will want it to exist before the citation is wrong, not after. The retrieval postmortem on days 73–74 is the learning review that follows; this addendum is the hour-of note.

#### Interview angle

Read the failure note. A PM who has already written the bad-news template is easier to trust with a pilot.

## Phase 6 — Machine Learning Product Practice

**Days 53–64 · Advanced · 6 projects**

### Goals

This phase decides which Harbor subtasks deserve a model. Edition selection with structured dates stays a rule. Drafting from chosen sources is a language-model job. A glass-only classifier waits until a decision needs it. You then write the labels, the point-in-time feature spec and the fields you prohibit, the cost matrix that keeps accuracy from choosing the threshold, the error portfolio that sends failures to the owning system, and the model card whose disclosure a handler can actually read. The phase is done when a supervisor can tell, from your documents, who picked the form, and when a tempting model has been explicitly deferred.

### Skills covered

Machine learning product practice: rules versus models, labeling guidelines, feature specification and leakage, cost-sensitive metric choice, error analysis, model cards and disclosure.

### Days 53–54 — Approach Decision: Rules, Classical ML, or a Language Model

Working copy and fixtures: [phase-06-ml-product/day-53-54-approach-decision/README.md](phase-06-ml-product/day-53-54-approach-decision/README.md)

**Days 53–54 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Harbor's hardest narrow subtask is not "write a helpful note." It is: given a date of loss, a policy effective window, and a set of Ohio personal-auto form editions, choose the edition that was in force, then attach any bulletin that amends that edition and was issued on or before the date of loss. A separate subtask is drafting sentences that stay inside those sources. Northline already stores edition codes and effective dates in Lumen for many policies, and the store is wrong or empty on some older notices.

#### Concept

Different parts of a product want different machinery. A date comparison against a structured effective-date field is a rule. A prediction of whether a free-text loss description is glass-only might be a classical model, if you had labels and a reason to predict it. Drafting a sentence that a handler will edit is a language-model job, and only after the sources are chosen. This project writes the decision record that assigns each Harbor subtask to a kind of machinery, with the evidence that would overturn the assignment.

The record stops a team from sending an edition-selection problem to a language model because the rest of the product uses one.

#### Approach

Split the pilot episode into subtasks. For each, fill a one-page decision block:

- **Input.** Structured fields, text, or both. Name the system that owns the field.
- **Output.** A class, a chosen record, or a span of text. Say whether the output must be exact.
- **Cost of a wrong output.** Tie it to the handler, the audit, or the claimant wait.
- **What "learning" would need.** Labels, their unit, who could create them, and how fast they drift (a bulletin a week is a drift rate).
- **Assigned approach.** Rule, classical model, language model, or human only.
- **Overturn condition.** The observation that would make you reopen the assignment.

Worked assignments you should pressure-test, not copy blindly:

Edition-in-force, when Lumen has effective dates: a rule. Overturn if the date fields are missing on more than a threshold of pilot notices you will set after looking at a sample, not before.
Edition-in-force, when dates are missing: human choice with both editions shown, not a model guess. Overturn if content operations can backfill dates for the Ohio personal-auto set before the pilot.
Bulletin attachment: a rule over publish dates and edition ids, once bulletins are structured. A language model reading an inbox is a different, worse product.
Sentence draft from chosen sources: a language model, with the contract's citation rules. Overturn if wizard tests show handlers accept prose they do not check; the fallback is citations with no prose.
Glass-only classification: do not build. You do not have a decision that needs the class yet. The experiment story's opt-out is a research note, not a mandate to train a classifier. Assign "not now" and write the decision that would make it real.

#### Components

- **Subtask list.** The episode broken into moves a system could own.
- **Decision blocks.** One per subtask, with the six fields.
- **Boundary diagram.** Where the rule's output becomes the language model's input. This boundary is the product's actual architecture, drawn in a few boxes.
- **Overturn log.** Empty table, columns ready, plus one hypothetical row written as an example of how a future entry should look.
- **Rejection note.** The glass-only classifier, and any other tempting model, with the reason it waits.

#### Flow

1. List subtasks by walking the service blueprint. Merge any two that always ship in the same component.
2. Fill decision blocks. Write the overturn condition before the assignment if you notice yourself choosing the fashionable option.
3. Draw the boundary. If the language model receives the whole library and is asked to pick the edition, the boundary is in the wrong place; move it.
4. Write the rejection note for at least one model someone on a typical team would propose.
5. On day 54, explain the boundary to an engineer and to a claims supervisor. If the supervisor cannot tell who picked the edition, the diagram is still an internal picture and you revise the words.

#### Tools and stack

Markdown and a small diagram. No training run. The decision record is the deliverable. A notebook that fits a toy classifier would answer a different question than the one this pilot is stuck on.

#### Setup

1. Create `harbor-portfolio/53-approach/decision.md`.
2. List subtasks before you open a model provider's site. The site is not an input to this decision.
3. Day 53 is blocks and the boundary. Day 54 is the rejection note and the two-audience explanation.

#### Deliverables

- Decision blocks for each subtask, including at least one "not now."
- A boundary diagram between the rule and the language model.
- An overturn log with a hypothetical example row, and a rejection note.

#### What done looks like

Edition selection is not assigned to the language model when dates exist. Every assignment has an overturn condition that names an observation. The supervisor can say, from your diagram, who or what picked the form. At least one attractive model is explicitly not now.

#### Think a step ahead

The next design is a hybrid failure: the rule picks an edition, the language model drafts from it, and a second bulletin amends only one paragraph, which the rule did not represent because the bulletin was stored as a PDF. Write the degraded behavior. The draft step must not run on a partial amend when the amend is unstructured, and the handler sees "bulletin on file, not yet structured; draft withheld." Specify who structures it and the maximum age of an unstructured bulletin you will tolerate in the pilot before this state becomes a gate failure. That is the real boundary, one level down from the clean diagram.

#### Interview angle

Draw the boundary and the overturn condition for edition selection. You are showing that model choice followed the subtask.

### Days 55–56 — Labeling Guideline and Adjudication

Working copy and fixtures: [phase-06-ml-product/day-55-56-labeling-guideline/README.md](phase-06-ml-product/day-55-56-labeling-guideline/README.md)

**Days 55–56 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Harbor needs a small set of human judgments to grade drafts and, later, to test edition selection when Lumen's dates are missing. The judgment is not "is this note good?" That question produces taste. The judgments you will specify are narrower: given a fixture claim, a candidate form edition, and a candidate bulletin, a trained reader marks whether the pair is the correct source set, and whether a drafted sentence stays inside that set. Two readers will disagree. The guideline is how they disagree in the same way, and how a third person resolves it.

#### Concept

A labeling guideline is a product document. It defines the decision, the unit being labeled, the examples that sit on the boundary, and the adjudication path. It is also a scope tool. Every vague instruction becomes a silent labeler, and silent labelers do not match. You will write the guideline for Harbor's source-set task and sentence-support task, write fifteen gold examples with answers and rationales, and write the adjudication rule for the pairs of examples where you expect disagreement.

#### Approach

Define the unit. For the source-set task the unit is a (notice, edition, bulletin-or-none) triple. The label is `correct`, `wrong_edition`, `wrong_bulletin`, or `insufficient_record`. `insufficient_record` is a real label, used when the fixture does not contain the dates a human would need. It is not a failure of the labeler.

For the sentence-support task the unit is a (sentence, cited span) pair. The label is `supported`, `unsupported`, or `out_of_job`. `out_of_job` covers coverage decisions and claimant messages. A sentence can be supported by the span and still be out of job if it draws a coverage conclusion the span did not ask for; write the precedence. Out-of-job wins, because the contract cares about that boundary even when the words appear in a form.

Write boundary examples on purpose:

- A rental limit that matches the form and ignores a newer bulletin.
- A sentence that copies the bulletin and cites only the form.
- A sentence that says "coverage applies" using words that do appear in an insuring agreement.
- A glass-only notice where the correct edition still applies and the draft adds glass advice the sources do not contain.
- A record with an effective date missing, where the honest label is `insufficient_record`.

Each gold example has the fixture text (short, fictional, marked as fixture), the label, and a two-sentence rationale a new labeler can check. Include at least three examples you consider genuinely borderline, with the rationale stating what you decided and what a reasonable labeler might do instead. Those three go to adjudication in the guideline, with a rule: if two labelers disagree and one of them chose the borderline rationale you wrote, the adjudicator may pick either, and the item is flagged `unstable` so it does not become a silent training target later.

Set an agreement target as a product goal, not as a number you pretend to have measured. For the source-set task, ask for exact agreement on a double-labeled sample before those labels are allowed to gate a pilot. State that you will compute agreement when a second reader exists, and that until then the guideline is untested. Name the statistic you expect a partner to compute later (percent agreement and a chance-corrected measure) without faking the value.

#### Components

- **Task definitions.** Unit, labels, precedence, and what the labeler is forbidden to infer.
- **Fifteen gold examples.** Fixture text, label, rationale. At least three borderline.
- **Adjudication rule.** Who adjudicates (a claims trainer, not the engineer who built the draft), the `unstable` flag, and how fast a disputed item must be resolved during the pilot.
- **Labeler instruction page.** One page, in the labeler's language, including "do not fix the sentence, label it."
- **Untested stamp.** A visible note that agreement has not been measured yet, and the sample size you would want before trusting the guideline (a number of double-labeled items you choose and justify in a sentence).

#### Flow

1. Write labels and precedence before examples, or the examples will invent the labels.
2. Draft fifteen examples. Mark the three you had to think about. Those are the borderline ones. If you had to think about none, the set is too easy to be a guideline.
3. Write the labeler page from the definitions, then try to label three of your own examples using only the page, a day later or after a break. Fix the page where you hesitate.
4. Write adjudication and the untested stamp.
5. On day 56, have another person label five examples from the page alone, without your rationales. Compare. Update the page where they miss for a reason the page could have prevented. Record what you changed.

#### Tools and stack

Markdown. A second person for the five-item trial. No labeling platform is required at this size. If the set later lives in a tool, the guideline text is still the source of truth.

#### Setup

1. Create `harbor-portfolio/55-labeling/guideline.md` and `gold-examples.md`.
2. Mark every policy sentence as fixture language so nobody mistakes it for Northline's forms.
3. Day 55 is definitions and the fifteen examples. Day 56 is the trial with a second reader and the revision.

#### Deliverables

- A guideline with units, labels, precedence, and labeler instructions.
- Fifteen gold examples with rationales and three borderline calls.
- An adjudication rule, an untested stamp, and a note from the second-reader trial.

#### What done looks like

A new reader can label a sixteenth item from the page. Out-of-job precedence is explicit. `insufficient_record` exists so labelers are not forced to guess. The second-reader trial changed the page, or you recorded that it did not and why. Agreement is not invented.

#### Think a step ahead

Guidelines rot when a new bulletin type appears (a temporary moratorium, a state department circular) that is not an "amendment" in the sense your labels used. Add a change protocol: who can add a label, why adding a label invalidates agreement you may later measure, and how items labeled under the old guideline are marked with a guideline version. Write the version field now, on every gold example, starting at `g1`. A set without versions cannot be repaired; it can only be doubted.

#### Interview angle

Show a borderline example, the two plausible labels, and the precedence that chose one. Then mention the untested stamp. Honesty about measurement is part of the craft.

### Days 57–58 — Feature Specification, Leakage, and Prohibited Fields

Working copy and fixtures: [phase-06-ml-product/day-57-58-feature-spec/README.md](phase-06-ml-product/day-57-58-feature-spec/README.md)

**Days 57–58 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Someone on the Harbor program proposes a classical model to prioritize the audit queue: score a committed note for "likely citation defect" so supervisors sample smarter than 8% at random. The proposal is optional and separate from the draft product. It is the cleanest place in this case to practice a feature spec, because the temptation to cheat, accidentally, is concrete. Lumen holds fields that would not have existed at the time the note was written, including the supervisor's later bounce-back.

#### Concept

A feature specification says what a model may see, what each field means in the business, when the value is known, and which fields are prohibited because they leak the answer or because the company will not put them in a decision. Leakage is a product bug as much as a modeling bug. A feature that includes "supervisor bounced this note yesterday" will look brilliant offline and be useless at the moment of sampling, because the bounce has not happened yet. A feature that includes the claimant's race, or a proxy the company has banned, is a different kind of prohibited, and it stays prohibited even if it predicts.

This project writes the spec for the audit-priority model as a product artifact. It does not train the model. Training would only hide a bad spec behind a score.

#### Approach

Write the decision the score supports: which notes enter this week's audit sample, in the Columbus pilot, among committed Ohio personal-auto notes. The score does not decide defectiveness. A person still audits.

For each candidate feature, record:

- **Meaning.** The business definition, not the column name.
- **Source system.** Lumen, Harbor logs, or the content catalog.
- **Time rule.** The value as known at commit time. If the field is updated later, the spec says which version is legal. This is the point-in-time rule.
- **Use.** Included, included only as a slice for later error analysis, or prohibited.
- **Reason.**

Prohibited, with reasons you should write in your own words after you agree:

- The supervisor's bounce, any audit outcome, and any field derived from them. These are the label, not the features.
- The handler's identity, as a feature. It may exist as a join key for evaluation slices (new versus tenured) and must not be a model input. A model that learns "Andre's notes are risky" will punish a person.
- Claimant race, ethnicity, religion, and fields you judge to be close proxies for this decision (for example, a neighborhood code, if you cannot explain a non-proxy use). Prohibited.
- The full note text in the first version. It will smuggle the citation language you are trying to judge and will make the spec unauditable. You may list it as a later version with a review gate, not as a silent addition.

Included candidates you should pressure-test: whether a citation was opened before commit, edit size, no-source result state, hours between notice and commit, whether the bulletin on the notice was structured, claim subtype if known at notice time, and handler tenure as a slice only.

Write two leakage stories in prose. One is temporal: a feature that was added after the outcome. One is identity: a feature that looks like process and functions as a person id. Both stories use Harbor fields.

#### Components

- **Decision statement.** What the score may change in the audit workflow, and what it may not change.
- **Feature table.** The columns above, for at least ten candidate fields, including prohibited ones. Prohibited fields stay in the spec so someone sees the refusal.
- **Point-in-time rule.** A paragraph your data partner can implement: "features are values as of note commit, joined on notice id."
- **Leakage stories.** Two, each ending with the test that would have caught it (train on a later field, watch the offline score collapse when the field is removed).
- **Slice plan.** Tenure and claim subtype as evaluation slices, explicitly not as inputs, and the minimum slice count below which you will not report a rate.

#### Flow

1. Write the decision statement. If the score changes who gets audited and also how handlers are managed, stop and cut the second use. This spec is for audit sampling only.
2. Inventory fields from the tracking plan and from Lumen as you understand it. Mark the time each becomes known.
3. Fill the table, prohibited rows included.
4. Write the two leakage stories from fields you almost included.
5. On day 58, have a partner propose one more feature that would raise an offline score. Decide in writing, against the table's rules. If you add it, add the time rule too.

#### Tools and stack

Markdown tables. The tracking plan is the inventory of Harbor-side fields. No model training and no feature store. The spec is the contract a later pipeline would have to meet.

#### Setup

1. Create `harbor-portfolio/57-features/spec.md`.
2. Write "as of commit time" at the top before listing fields, so the time rule is not an afterthought.
3. Day 57 is the decision and the table. Day 58 is leakage stories, slices, and the partner's extra feature.

#### Deliverables

- A decision statement for audit sampling only.
- A feature table of at least ten fields with point-in-time notes and prohibited rows.
- Two leakage stories and a slice plan.

#### What done looks like

A data partner can see which version of a field is legal. Bounce-back is on the page as prohibited, with the reason. Handler identity is a slice key and not an input. The spec can be reviewed without a notebook. At least one tempting feature was refused in the partner exercise or accepted with a time rule.

#### Think a step ahead

The legal time for a citation defect is not commit time alone. The form that was correct at commit may be the form that was in force on the date of loss, which can be months earlier, and a bulletin published between the date of loss and the commit is a different fact from a bulletin published after commit. Extend the point-in-time rule with two clocks: facts about the policy as of the date of loss, and facts about the handler's session as of commit. Write one feature that is legal on the first clock and illegal on the second, and one in the other direction. A spec with a single clock will be implemented with whichever timestamp was easiest to join.

#### Interview angle

Tell one leakage story all the way to the test that catches it. Then name a field you prohibited for a fairness reason, separate from leakage. They are different refusals.

### Days 59–60 — Cost Matrix and Offline Metric Choice

Working copy and fixtures: [phase-06-ml-product/day-59-60-cost-matrix/README.md](phase-06-ml-product/day-59-60-cost-matrix/README.md)

**Days 59–60 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** The audit-priority score from the feature spec is being evaluated offline on a fixture of 200 past Columbus notes, of which 20 were later judged citation defects. You are not fitting a model. You have been given two candidate score thresholds, A and B, and the confusion counts at each. You must choose the operating point and the metric that justifies it, using costs a claims manager can recognize. Accuracy is available and you are expected to explain why you are not choosing on accuracy.

#### Concept

When misses and false alarms have different costs, a single summary number is a product decision disguised as math. For audit priority, a false alarm means a supervisor spends time on a clean note. A miss means a defective citation stays in the 92% of notes that are not audited, which is the current world, except that the pilot may now feel "covered" by the model and sample even less thoughtfully. The cost of a miss is not identical to the cost of a false alarm, and it is not identical for a glass-only claim and a total loss. This project makes that asymmetry explicit and picks an operating point.

#### Approach

Use these counts as given for the 200-note fixture, where a "positive" prediction means "put this note in the audit sample":

|  | Defects caught (of 20) | Clean notes flagged (of 180) | Notes a supervisor would open |
| --- | --- | --- | --- |
| Threshold A | 14 | 30 | 44 |
| Threshold B | 8 | 10 | 18 |
| Random 8% sample (about 16 notes) | about 1 or 2 in a typical draw; use 2 as the planning comparison | about 14 | 16 |

The random row is a baseline, not a third model. It is the process Harbor's score has to beat to be worth existing.

Assign dollar placeholders a finance partner would replace. Write them as placeholders. A workable set to start from, and you should say you would replace it: one hour of supervisor time per audited note at a placeholder rate, and a placeholder expected cost for a missed citation defect that reaches a file a lawyer later reads. Because the second number is the whole argument, show the decision at two different miss-costs, a low one and a high one, so the reader sees the switch.

Compute, for A and B:

- precision and recall on the fixture,
- supervisor hours implied,
- total placeholder cost at the low miss-cost and at the high miss-cost,
- the comparison against the random baseline's planning numbers.

Choose an operating point for the pilot, or choose neither. Neither is allowed if the score does not beat the baseline on the cost that claims leadership believes, or if beating it requires a miss-cost they will not sign. Write the sentence you need them to sign.

Also write the metric you will report in the model review. It may be recall at a fixed supervisor-hour budget, which is a product constraint (the Columbus supervisor has hours for about 40 notes a week, not for an unlimited queue). Put that constraint in the choice. Threshold A opens 44 notes in this fixture's scale; say whether that fits the hour budget you are assuming for a week of Columbus volume, and adjust the choice if it does not. State your volume assumption.

#### Components

- **Cost table.** Placeholder inputs, labeled, and the two miss-cost scenarios.
- **Operating-point sheet.** Precision, recall, hours, cost, baseline comparison.
- **Choice memo.** The point you pick or the decision to keep random sampling, the constraint that drove it, and the sentence leadership must sign.
- **Report metric.** The one number the review will headline, and the numbers that must be shown beside it so the headline cannot travel alone.
- **What accuracy does here.** A short calculation of accuracy at threshold A, and a sentence on why it flatters a screen that marks almost everything clean. Do the arithmetic. With 20 defects in 200, a screen that flags nobody is already 90% accurate.

#### Flow

1. Compute the nobody-flagged accuracy first, so the trap is in the room before you look at A and B.
2. Compute precision, recall, hours, and costs. Show formulas in one line each.
3. Apply the supervisor-hour constraint. If your preferred point violates it, switch or propose a smaller sample and recompute. Do not leave the constraint as a footnote.
4. Write the choice memo and the sentence leadership must sign.
5. On day 60, change the high miss-cost to a number that flips your choice, and record that number. That sensitivity is part of the deliverable, because the placeholder is not sacred.

#### Tools and stack

A spreadsheet or a calculator, plus a memo. No model fitting. The counts are the dataset.

#### Setup

1. Create `harbor-portfolio/59-cost-matrix/choice.md` and a small sheet.
2. Write the placeholder rates at the top so they cannot hide in a formula.
3. Day 59 is the arithmetic and the baseline. Day 60 is the constraint, the choice, and the sensitivity flip.

#### Deliverables

- An operating-point sheet with the random baseline.
- A choice memo leadership can sign, including the hour constraint.
- The accuracy trap, computed, and the miss-cost that flips the choice.

#### What done looks like

The arithmetic can be redone from the memo. The choice beats random sampling on a stated cost, or the choice is to keep random sampling. Accuracy is computed and rejected as the decider, with the 90% figure visible. The hour constraint is applied, not admired.

#### Think a step ahead

A missed defect on a total-loss file and a missed defect on a glass-only file do not share a cost, and this fixture does not tell them apart. Specify the next table you would demand before locking a threshold for a second quarter: the same confusion counts split by claim subtype, plus a rule that a subtype with fewer than a minimum you set is not given its own threshold. Write the minimum and the reason a separate threshold on a tiny cell would be a false precision. The follow-on is cost heterogeneity, which a single matrix hides.

#### Interview angle

Lead with the 90% accuracy trap, then the operating point you actually chose and the constraint that chose it.

### Days 61–62 — Error Analysis and the Fix Portfolio

Working copy and fixtures: [phase-06-ml-product/day-61-62-error-analysis/README.md](phase-06-ml-product/day-61-62-error-analysis/README.md)

**Days 61–62 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** During shadow review, a claims trainer looked at 40 Harbor drafts for Ohio personal-auto notices. Twenty were acceptable under the labeling guideline. Twenty were not. The failures are listed below as a fixture. You will group them, decide which system is actually broken, and write a fix portfolio that does not send every failure to the model team.

#### Concept

Error analysis is the practice of reading misses until they become a portfolio of causes, each with an owner. Teams that skip it "improve the model" because that is the team that is listening. In this fixture, several misses are content problems, product-rule problems, or handler-interface problems. A model change would not touch them. The deliverable is a fix portfolio: a small set of actions, each aimed at a cause, with a way to know the action worked, and an explicit "no model change" on the causes that do not deserve one.

#### Approach

Here are the twenty unacceptable drafts, summarized. Treat the summaries as the trainer's notes. Do not invent milder versions.

1–4. Cited the November edition on a loss that occurred after the February edition's effective date. Lumen had the correct date. The prompt showed both editions' text.
5–7. Cited the February edition and a rental limit from the November edition. Lumen date was correct. Both texts were in the prompt.
8–10. Bulletin from last week amended the rental limit. The bulletin was only in email. The draft used the form's limit and cited the form correctly. The form was, in that sense, faithful, and the note was still wrong under the contract.
11–12. Draft said "this loss is covered under collision" in a sentence that quoted the insuring agreement. Citation opened. Label: out of job.
13. Draft declined to answer "is this covered?" and also declined to draft the note that was actually requested. The handler had asked both in one message.
14–15. No-source state was correct (edition missing from the published set) and the handler later said, in a shadow interview, that the empty state looked like a spinner, so they waited and then pasted an older draft from the previous notice.
16–17. Glass-only claims. The draft added a rental paragraph the sources do not support. Citation was not opened. `edit_size=none`.
18. A commercial-auto form was retrieved for a personal-auto notice. The handler is licensed in personal auto only. The form code's prefix differed.
19. Draft cited a real paragraph and attributed it to the right form, with the wrong page number.
20. Two bulletins applied. The draft followed the older one. Both were structured. The precedence rule has not been written.

Group them into causes. A cause has a name, the item ids, the system that owns the fix (content operations, product rules, interface, retrieval selection, or the drafting model), and whether a model change is allowed to be the fix. For items 1–7, ask yourself whether the model was asked to do edition selection against your own approach decision. If the prompt contained both editions, the fix may be "stop doing that," which is a boundary fix, not a prompt-tuning fix.

Write the portfolio as no more than five actions. Each action names the items it should clear, the owner, the proof it worked (a relabel of those items, or a log that the bad state is now impossible), and the items it will not clear. An action that claims all twenty is not an analysis.

Order the portfolio by risk and by what you can do before the limited pilot. A wrong-library retrieval (item 18) and an out-of-job coverage sentence (items 11–12) outrank a wrong page number (item 19), unless you have a reason they do not.

#### Components

- **Cause groups.** Name, item ids, owning system, whether a model change is in or out.
- **Fix portfolio.** Up to five actions, with proof and exclusions.
- **Ordering note.** Why the first action is first, tied to the interaction contract.
- **Measurement note.** Which groups are large enough in this sample of forty to discuss as patterns, and which are single items you will watch and not chart. Items 19's page number is a single. Do not invent a rate for it beyond "1 of 40 in this review."
- **Feedback to the guideline.** Any item where the trainer's note and the labeling guideline disagree. If you find none, say what you checked.

#### Flow

1. Read all twenty before grouping. First groupings tend to be "the model messed up," which is the grouping you are here to break.
2. Assign an owning system to each item. Where two systems could own it, pick the one that can make the failure impossible, not the one that can apologize after it.
3. Draft actions. Merge only when the proof is the same.
4. Order them. Write the ordering note in sentences, not in a fake numeric score.
5. On day 62, take the top action and write the sprint goal it implies, in the shape you used on days 47–48. The analysis is unfinished if it cannot become a goal.

#### Tools and stack

Markdown. A spreadsheet helps if you want to sort item ids. No embedding visualization and no error-analysis framework. Forty notes is a reading job.

#### Setup

1. Create `harbor-portfolio/61-errors/analysis.md`.
2. Paste the twenty summaries so your groups can refer to stable ids.
3. Day 61 is grouping. Day 62 is the portfolio, the ordering, and the sprint goal.

#### Deliverables

- Cause groups covering all twenty ids.
- A fix portfolio of at most five actions, ordered, with proofs.
- One sprint goal derived from the top action, and a measurement note on singletons.

#### What done looks like

Items 8–10 are not assigned to a model retrain as the primary fix. Items 11–12 are treated as contract violations. Item 18 has an owner who can keep a commercial form out of a personal-auto retrieval. The portfolio says what it will not clear. A sprint goal could be picked up on Monday.

#### Think a step ahead

Shadow review of forty will not match live traffic once handlers learn to ask shorter questions. Specify a monthly error-review sample that is drawn from committed notes, not from drafts the trainer finds interesting, and write the sampling rule: a fixed count, stratified by result state (`cited`, `no_source`, `declined`) and by whether a citation was opened. Include the rule that any out-of-job sentence found in the sample pages the incident addendum from the comms system, even if the count is one. The follow-on is a sampling frame that cannot be satisfied by rereading the same twenty famous bugs.

#### Interview angle

Pick item 8 and item 11 and say, in two sentences each, who fixes them and why a model change is the wrong first move. That is error analysis.

### Days 63–64 — Model Card and In-Product Disclosure

Working copy and fixtures: [phase-06-ml-product/day-63-64-model-card/README.md](phase-06-ml-product/day-63-64-model-card/README.md)

**Days 63–64 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** Harbor is about to enter a limited pilot. Two different things need a plain-language description of their limits. The drafting behavior is a language model bounded by the interaction contract and by sources the rule layer selected. The audit-priority score, if you chose to pilot it, is a separate model with a different decision. They do not share a card. This project writes the drafting card and the handler-facing disclosure. The score, if it exists, gets a stub that says it is a different card and names the decision it touches.

#### Concept

A model card is the document a new teammate, an auditor, or a future you can read to learn what the system is for, what it is not for, what data it sees, how it fails, and who is accountable when it fails. An in-product disclosure is the few lines a handler actually sees, which have to be true to the card and short enough to be read during training. Cards that exist only in a repository, and disclosures that say "AI may be inaccurate" without saying what the handler remains responsible for, are both incomplete. You will write both so they agree.

#### Approach

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

#### Components

- **Drafting model card.** The sections above, filled, one to three pages.
- **Audit-score stub.** Five lines: different system, different decision, card not written, do not cite the drafting evidence as if it applied.
- **Disclosure copy.** Under 120 words, plus where it appears (training, and a persistent link on the draft panel, not a one-time modal that never returns).
- **Disagreement test.** A two-column check, completed.
- **Update rule.** What changes force a card revision during the pilot: a new intended use, a new input class, a vendor version change, or a failure mode found in the monthly sample that the card does not list.

#### Flow

1. Fill intended use and out of scope from the interaction contract and the principles. If you drift, stop and reconcile.
2. Write performance evidence last, after you have decided which studies are real. Invent nothing.
3. Draft the disclosure from the card, then cut it to 120 words without losing authorship and refusal.
4. Run the disagreement test and fix whichever side is wrong.
5. On day 64, read the disclosure aloud at a normal pace. If it takes more than a minute, it is still a card. Cut again.

#### Tools and stack

Markdown. Source documents from earlier projects, cited by name. No card generator and no model call. The writing is the accountability exercise.

#### Setup

1. Create `harbor-portfolio/63-model-card/card.md` and `disclosure.md`.
2. Start a "do not invent metrics" note at the top and delete it only when you have checked the performance section against the fixtures you actually have.
3. Day 63 is the card and the stub. Day 64 is the disclosure, the disagreement test, and the read-aloud.

#### Deliverables

- A filled drafting model card.
- A separate stub for the audit score.
- Disclosure copy, a completed disagreement test, and an update rule.

#### What done looks like

The performance section matches a real fixture, including its small size. The disclosure names the handler as author and names two refusals. The disagreement test has been filled, not described. The audit score cannot borrow the drafting card. A reader can find an owner for source freshness.

#### Think a step ahead

A card written for Ohio personal auto will be attached, by someone helpful, to a Michigan pilot that reuses the screen. Add a jurisdiction block: the card names the state and the form family, and the product must show the handler a "not in the card's intended use" state when the notice's governing state or line differs. Write the exact state and the log event. Reuse without that state is how a careful card becomes cover for a careless rollout. The platform bet on days 95–96 will try to make reuse easy; this block is the brake.

#### Interview angle

Read the disclosure, then one failure mode the disclosure deliberately leaves out, and say where a teammate would find it. You are showing you know the difference between a card and a caption.

## Phase 7 — Retrieval-Augmented Product Design

**Days 65–74 · Advanced · 5 projects**

### Goals

This phase specifies retrieval as a product with an honest empty result. You write reason codes, the corpus boundary, and the freshness promise. You write the precedence rules for a bulletin that amends a form, and the citation fields a supervisor can check months later. You author a twenty-five-row golden set that includes unanswerables and a leakage rule. You design the answer experience so a partial corpus does not draft a confident wrong limit, and you close with a postmortem of a real-but-wrong document that changes a spec or a test. The phase is done when "always return the nearest paragraph" has nowhere to hide in the requirements.

### Skills covered

RAG as product design: retrieval requirements and reason codes, corpus precedence and citations, golden question sets, answer experience and handoff, retrieval incident review.

### Days 65–66 — Retrieval Product Requirements

Working copy and fixtures: [phase-07-rag-product/day-65-66-retrieval-prd/README.md](phase-07-rag-product/day-65-66-retrieval-prd/README.md)

**Days 65–66 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** Harbor's drafting model is only allowed to see sources a selection step has already narrowed: the Ohio personal-auto edition in force on the date of loss, and bulletins that amend it and were published on or before that date. The library is about 1,400 pages across lines and states. The pilot uses a thin slice of it. Handlers have been compensating for library gaps with personal documents and forwarded emails. Those personal stores are not a corpus you will index.

#### Concept

Retrieval is a product, not a preprocessor. It has users, a corpus, a freshness promise, a behavior when nothing qualifies, and a success measure that a claims trainer can grade. A requirements document for Harbor's retrieval step says what "the right document" means, who is allowed to add one, how current "current" is, and what the handler sees when the step should return nothing. It does not choose a vector index, a chunk size, or a framework. Those are implementation choices that have to satisfy this document.

#### Approach

Write the requirements for one retrieval job: given a notice's state, line of business, date of loss, and the edition records the rule layer already trusts, return the passages the drafter may see, or return an empty set with a reason code. The reason codes are part of the product:

- `no_edition_in_force` — the rule layer has no edition, and retrieval must not guess one.
- `edition_not_published` — an edition id exists and the body is not in the published corpus.
- `bulletin_missing` — the catalog says a bulletin applies and the body is not published.
- `ok` — one or more passages, each with edition id or bulletin id, effective dates, and a passage locator a human can open.

Each code has a handler-visible sentence and a log event. Empty is a successful call when the honest result is empty. A requirements document that only specifies the happy passage list will be implemented as "always return the nearest paragraph."

Write success measures the trainer can apply without a model: on a set of notices with known correct ids, the returned set contains the required ids and contains no id from the wrong state or the wrong line. You will design the question set itself on days 69–70. Here you write the measure and the bar you would hold a pilot to, in words, and you note that the bar is unmeasured until that set exists.

Write non-goals. Retrieving from the open web, searching a handler's desktop, answering a question that has no notice context, and selecting an edition when the rule layer abstained are non-goals. State the non-goal that will be requested first ("just let it search all of SharePoint") and the response, which points back at the reason codes.

#### Components

- **Job statement.** Inputs, outputs, reason codes, and the user who sees each output.
- **Corpus boundary.** What is in the pilot corpus, by named class (Ohio personal-auto forms in force for the pilot window, structured bulletins for those forms). What is out (other states, commercial, email inboxes, handler desktops, the web).
- **Freshness promise.** The maximum age of the published set relative to a bulletin email, during the pilot, and the behavior when the promise is broken. Tie this to a content owner from the milestone map. If the owner cannot meet the promise, the requirement is the `bulletin_missing` path, not a quiet staleness.
- **Success and bar.** The trainer's check, the bar, and the "unmeasured" stamp.
- **Requirement non-goals and the first request you will refuse.**

#### Flow

1. Write reason codes before you write any requirement that assumes a passage exists.
2. Define the corpus boundary as classes of documents, not as a folder path. Paths change. Classes are the contract.
3. Set the freshness promise in hours or business days, with the behavior on breach.
4. Write the success check in trainer language and stamp it unmeasured.
5. On day 66, read the document as an engineer looking for permission to "return the top three anyway" on an empty result. Close every sentence that grants that permission. Then read it as the content owner and underline the promise you are making about their weekend. Adjust the promise if a weekend bulletin would make you liars by Monday.

#### Tools and stack

Markdown. The approach decision and the interaction contract are inputs. No retrieval library, no embeddings tutorial, and no index. This is the spec those things would be accepted against.

#### Setup

1. Create `harbor-portfolio/65-retrieval-prd/prd.md`.
2. Start from the reason codes. If you start from a user story about "powerful search," delete the first page and start again.
3. Day 65 is job, codes, and corpus boundary. Day 66 is freshness, the bar, the refusal, and the two-role read.

#### Deliverables

- A retrieval requirements document with reason codes and handler-visible sentences.
- A corpus boundary and a freshness promise with a breach behavior.
- A trainer-grade success check, stamped unmeasured, and a written refusal of unscoped search.

#### What done looks like

An engineer can implement an empty result without inventing a fallback query. A content owner can see the freshness number they are being asked to hit. The success check talks about document ids and wrong-line exclusions. "Top k" does not appear as a requirement. Personal desktop files are out of the corpus in a sentence someone can point to.

#### Think a step ahead

The next request will be a question that needs two hops: the edition's exclusion, and an endorsement that puts the exclusion back for a specific vehicle class. A single passage cannot be "the answer." Extend the job statement with an optional `set` output: an ordered pair of passages plus a note that the drafter must not answer from only one of them when the catalog says both apply. Write the handler-visible behavior when the second passage is missing (`bulletin_missing` is close; decide whether endorsement-missing is the same code or a new one, and why). The follow-on is multi-document completeness, which a single-hit search requirement will silently drop.

#### Interview angle

Explain empty-as-success and the freshness breach behavior. Retrieval requirements are about what the product does when the library is not ready.

### Days 67–68 — Corpus Policy and Citation Behavior

Working copy and fixtures: [phase-07-rag-product/day-67-68-corpus-and-citations/README.md](phase-07-rag-product/day-67-68-corpus-and-citations/README.md)

**Days 67–68 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** Harbor may cite Ohio personal-auto forms and the bulletins that amend them. Two sources can both look current and disagree: a form PDF and a bulletin issued later, or two bulletins where the later one narrows the earlier one. The handler has to see enough to open the right page, and the draft has to obey a precedence rule you write down. A citation that says "source: policy" is not a citation in this product.

#### Concept

Corpus policy decides which documents are allowed to support a sentence and which win when they conflict. Citation behavior decides what the handler sees, what is logged, and what the drafter is allowed to do when the winning source is missing. Together they are the product's notion of evidence. This project writes both as rules with examples, including the conflict case you sketched in the competitive teardown: a date of loss, two editions, and a bulletin that amends only the newer one.

#### Approach

Write precedence in an order a content analyst can apply without a meeting:

1. The edition in force on the date of loss, as chosen by the rule layer, is the only form that may be cited.
2. A structured bulletin published on or before the date of loss, and marked as amending that edition, overrides the form where it explicitly amends it, and nowhere else.
3. A later bulletin overrides an earlier bulletin on the same point.
4. Email, desktop notes, and the handler's memory are not sources, even when they are right. The recovery is to get the bulletin structured, not to cite the inbox.
5. If the applicable bulletin is known to exist and is not structured, the draft is withheld and the reason code from the retrieval requirements is shown. The form's unamended limit is not an acceptable fallback, because it is the error Priya already gets written up for.

Write citation fields the handler can use: document title, edition id, in-force window, bulletin id and publish date if used, and a locator (section heading or page). A citation missing any of these is not displayable, and an undisplayable citation cannot support a sentence.

Write three worked conflicts as if they were fixtures:

- Bulletin amends the rental limit; the form has the old limit. The draft uses the bulletin's number and cites both, with the bulletin marked as overriding.
- Bulletin amends only the newer edition; the loss falls under the older edition. The newer bulletin is not cited.
- Two bulletins, a week apart, different rental numbers. The later one is cited as overriding, and the earlier one is visible as superseded, not silently dropped, so a supervisor can see why the number is not the one they remember.

Specify the click behavior. Opening a citation shows the locator in the published document, not a model paraphrase of it. If you cannot deep-link, the requirement is to show the exact quoted span beside the locator, copied from the corpus, not regenerated.

#### Components

- **Precedence rules.** The ordered list, plus who is allowed to mark a bulletin as "amending" a given edition. That marking is a content action with a name and a second-person check for the pilot.
- **Citation schema.** Required fields, and the rule that a sentence with no displayable citation is not drafted.
- **Three conflict fixtures.** Inputs, the winning source, the citation the handler sees, and one wrong behavior that would be easy to ship.
- **Superseded-source display.** How the handler sees a source that was considered and rejected, without letting it be copied into the note by accident.
- **Corpus change control.** Who may add a document class to the pilot corpus. The default answer is nobody during the ten weeks, and the path for an exception is the same escalation rule as a principle change.

#### Flow

1. Draft precedence from Priya's rental-limit error, so the rule solves a real miss and not a taxonomy exercise.
2. Write the citation schema and apply it to each conflict fixture. If a field is missing in your own example, the schema is fantasy.
3. Specify superseded-source display and the accidental-copy risk.
4. Write change control, including the refusal of desktop files.
5. On day 68, give the three fixtures to a partner and your precedence list. They apply the rules. Wherever they get a different winner, fix the rule's wording, not their reading, unless they skipped a line. Record the edit.

#### Tools and stack

Markdown. Short fixture passages you write and label as fake. No document parser and no search stack. The policy has to be computable by a careful person, which is the right bar for a rule the product will automate later.

#### Setup

1. Create `harbor-portfolio/67-corpus/policy.md` and `conflicts.md`.
2. Number the precedence rules. You will refer to them by number in later projects.
3. Day 67 is precedence, schema, and fixtures. Day 68 is superseded display, change control, and the partner application.

#### Deliverables

- Ordered precedence rules and a named content action for "amending."
- A citation schema with a no-display, no-draft rule.
- Three conflict fixtures a partner has tried to apply, plus the wording change you made.

#### What done looks like

A partner reaches the same winner on all three fixtures using the written rules. The unamended form is not a fallback when a known bulletin is unstructured. Citations have fields a supervisor could check six months later. Desktop files are refused in the change-control section.

#### Think a step ahead

A state insurance department circular can bind the company without fitting the word "bulletin," and it can arrive as a PDF that amends many forms at once. Add a source class, `circular`, with a precedence position relative to form and bulletin, an owner, and a pilot decision: either circulars are in scope and the schema has a field for them, or they are out of scope and the handler sees a specific sentence ("department circulars are not in Harbor; use the compliance site"). Pick one for the ten-week pilot and write the sentence. The dangerous outcome is a silent middle, where the circular is sometimes retrieved because it was in the same folder.

#### Interview angle

Walk one conflict fixture from the rule number to the citation fields. Then say what the product does when the winning bulletin is not structured. That second beat is the policy.

### Days 69–70 — Golden Question Set

Working copy and fixtures: [phase-07-rag-product/day-69-70-golden-questions/README.md](phase-07-rag-product/day-69-70-golden-questions/README.md)

**Days 69–70 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** Harbor's retrieval step needs a set of notices with known-correct source ids, so a trainer can apply the success check from the retrieval requirements. The set is a product asset. It encodes the situations you care about, including situations where the correct result is to return nothing. It is also a leakage risk: if the same items are pasted into a prompt as examples, you are grading the system on answers you handed it.

#### Concept

A golden set is a list of inputs, expected outputs, and tags, built to measure a behavior you specified. For Harbor the input is a notice context (state, line, date of loss, the rule layer's edition id or the fact that it abstained, and the catalog's view of bulletins). The expected output is a set of document ids plus a reason code, not a paragraph of prose. Prose expectations belong to the drafting eval, and mixing them into the retrieval set makes both scores muddy.

You will author the set on paper, at a size you can actually curate: 25 items. You will tag slices, include unanswerables, and write the handling rules that keep the set out of prompts and out of casual demos.

#### Approach

Compose 25 items so the slices are deliberate. A suggested mix, which you may adjust if you explain the change:

- 8 items where one edition is in force and no bulletin applies. Expected reason `ok`, one id.
- 5 items where a bulletin amends a limit. Expected ids: edition and bulletin.
- 4 items where a newer edition exists and is not in force for the date of loss. Expected: the older id only.
- 3 items where the catalog knows a bulletin the corpus does not contain. Expected reason `bulletin_missing`, no draft passages.
- 3 items where the rule layer abstains. Expected reason `no_edition_in_force`. The set must not smuggle the right edition into "context."
- 2 items from the wrong line or state, included because a real queue will contain them. Expected: no personal-auto Ohio passage. Choose the reason code that matches your requirements; if none fits, add `out_of_corpus` to the requirements and record that you extended the spec.

Each item is a row: id, slice tag, notice facts, catalog facts, expected ids, expected reason, and a one-line note on why it is in the set. Use fictional ids (`OH-PA-2026-02`, `BUL-1044`). Do not paste real policy language into the set. The retrieval set checks identity and reason, not wording. Wording checks use the labeling guideline's sentence-support task and should be a different file, which you may point at and should not merge.

Write the leakage rule. Items in this file are evaluation-only. They are not few-shot examples. A demo that uses a golden notice is labeled a demo and its score is not reported as the set's score. Anyone who wants to add an item copies the row format and assigns a version. Anyone who wants to delete an item marks it retired with a reason, and does not renumber the rest.

Write the bar in counts, since 25 is small. Example shape, for you to set and defend: zero wrong-line inclusions, and at most one miss on the bulletin-amendment slice, before the retrieval step can enter shadow week. A bar of "90% overall" can be met while every `bulletin_missing` item is wrong. Slice floors are the point. With three items in a slice, say so, and prefer "all of these three" to a percentage that pretends precision.

#### Components

- **Row schema and 25 rows.**
- **Slice counts.** A short table so a hole is obvious. If a slice has fewer than three items, justify it or add items by shrinking a saturated slice.
- **Bar.** Slice floors, in counts, tied to the shadow-week gate.
- **Leakage and version rules.** Eval-only, no renumbering, retirement instead of deletion.
- **Known gap.** What this set does not measure (prose faithfulness, page locators, handler behavior). Point at the project that measures each, so nobody treats this file as the whole quality story.

#### Flow

1. Write the row schema and the slice targets before authoring items, or you will write twenty easy matches.
2. Author the unanswerables and the wrong-line items first, while you are still willing to make the set harsh.
3. Fill the rest. Check counts.
4. Set the bar in counts. If you cannot explain a floor to the Columbus manager, the floor is a vibe and you rewrite it.
5. On day 70, try to "cheat" your own set: describe one prompt example that would inflate a demo. Write the rule that makes that cheat visible. If you cannot describe a cheat, the set is too abstract to leak, which is acceptable, and you should still write the rule.

#### Tools and stack

A CSV or a markdown table. No retrieval stack. The asset is the rows and the rules. Implementation of scoring can be a later engineering task that reads this file.

#### Setup

1. Create `harbor-portfolio/69-golden-set/questions.csv` and `rules.md`.
2. Freeze slice targets at the top of `rules.md`.
3. Day 69 is rows and counts. Day 70 is the bar, leakage rules, and the cheat test.

#### Deliverables

- Twenty-five rows with expected ids and reason codes.
- Slice counts and a bar written in counts.
- Leakage, versioning, and retirement rules, plus a known-gap note.

#### What done looks like

A trainer can grade a retrieval result against a row without watching a draft. Unanswerable items exist and expect a reason code, not a near-match passage. The bar cannot be passed by the easy slice alone. The file says it is not few-shot material. Real policy text is absent.

#### Think a step ahead

Items will saturate: once the system gets all eight easy matches for a month, those rows stop teaching you anything and still dominate an overall number. Write a saturation rule. A slice that has been perfect for a number of consecutive runs you set is reported separately and is no longer allowed to carry the headline number. Replacing a saturated item requires a new id, a harder neighbor, and a retirement note on the old one. The follow-on keeps the set pointed at the failures you still have, which a frozen leaderboard will not do.

#### Interview angle

Show the slice counts and the bar. Explain one unanswerable row and why a fluent paragraph would still fail it. You are grading retrieval, not charm.

### Days 71–72 — Answer Experience and Human Handoff

Working copy and fixtures: [phase-07-rag-product/day-71-72-answer-experience/README.md](phase-07-rag-product/day-71-72-answer-experience/README.md)

**Days 71–72 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** A Harbor handler sees a draft only when retrieval returned `ok`. They see a reason sentence when it did not. Some notices are only partly supported: the edition is published, the bulletin that amends one limit is not. The handler can always abandon Harbor and write the note in Lumen. That path is the handoff, and it has to be designed with the same care as the draft, because it is what careful handlers will use on the worst files.

#### Concept

The answer experience is everything after retrieval returns: which passages are shown, how partial support is described, how the handler edits, and how the work moves to a person, a queue, or the plain Lumen note when the product should get out of the way. Handoff is not a failure message. It is a destination, with the context the next step needs so the handler does not re-search from scratch.

This project specifies that experience for Harbor, including copy, and the rule for when a partial answer is more dangerous than silence.

#### Approach

Specify four states. For each, write the layout in words, the exact copy, the actions, and what is logged.

1. **Full support.** Every sentence in the draft has a displayable citation under the precedence rules. The handler can edit, open a citation, discard, or commit. Commit records author, draft version, and citation ids available.
2. **Partial support.** The edition is citable and a required bulletin is not published. Default action: do not draft the limit that the bulletin would have amended, and do not draft a cheerful partial note that omits the limit. Show the edition citation, the `bulletin_missing` sentence, and a single primary action: "Write the note in Lumen," with the edition id copied to the clipboard or inserted as a source line the handler asked for. Justify this default against the alternative, which is a draft that is faithful to an incomplete corpus and therefore wrong in the file.
3. **No support.** Reason sentence, no passages, same primary action. Do not show "related" documents from another line.
4. **Out of job.** The handler asked for coverage or a claimant message. Decline copy from the interaction contract, and leave any in-job draft request usable if it was a second sentence. This is the fix for error-analysis item 13, where a combined message lost the note entirely. Specify how the interface separates the two asks.

Handoff details matter. "Write the note in Lumen" should land the handler in the note with the notice context intact, not at a home screen. If the integration cannot do that in the pilot, the spec says what the handler sees instead, and that gap is a named limitation on the model card's oversight section. Update the card's limitation list in a short addendum here; do not pretend the deep link exists.

Write the partial-answer danger rule as a principle the team can reuse: if the missing source would change a number or a prohibition in the note, suppress the draft. If the missing source is a page locator only, and the span text is in the corpus, the draft may proceed with the locator flagged. Item 19 in the error analysis (wrong page, right span) is the second case. The rental limit is the first.

#### Components

- **State specs.** Four states, copy included, actions included, logs included.
- **Handoff destination.** Where the handler lands, and the pilot limitation if the destination is weaker than you want.
- **Partial-answer rule.** The number-or-prohibition test, with the rental example and the page-locator example.
- **Combined-ask behavior.** How out-of-job and in-job requests in one message are separated.
- **Card addendum.** The limitation you added, in two or three sentences, ready to paste into the model card.

#### Flow

1. Start with partial support. It is the state teams design last and handlers hit on bad weeks.
2. Write copy in handler language. Read it against Priya's failure line. If the copy could be pasted into the note as if it were a coverage statement, rewrite it.
3. Specify handoff destination and the pilot limitation honestly.
4. Write the combined-ask behavior and test it against a single text box, because that is the interface you are likely to have.
5. On day 72, take the twenty error-analysis items and assign each to a state or to "should never reach the handler." Any item that has no state is a hole in this spec. Close the hole or name the earlier project that must close it.

#### Tools and stack

Markdown, plus copy you are willing to show a handler. No front-end build is required. A wireframe image is optional; the words and the rules are the spec. If you draw a wireframe, the copy on it must match the document exactly.

#### Setup

1. Create `harbor-portfolio/71-answer-ux/states.md`.
2. Keep the reason codes and the precedence rules open while you write copy.
3. Day 71 is the four states and the partial-answer rule. Day 72 is handoff, combined-ask, the card addendum, and the error-item mapping.

#### Deliverables

- State specs with copy, actions, and logs.
- A partial-answer rule with two contrasting examples.
- A mapping from the twenty error items to states, and a model-card addendum.

#### What done looks like

Partial support does not draft the unamended rental limit. The no-support state shows no "related" commercial form. A combined coverage question and note request still allows the note. Every error-analysis item has a state or a named upstream fix. The disclosure and the new copy do not conflict.

#### Think a step ahead

Handlers will ask for a side-by-side of "what I would have written" and the draft, once they trust the tool enough to argue with it. That view is a different product surface: it needs their in-progress Lumen text, which may contain claimant details your RAID log forbids sending to a vendor. Specify the comparison as a local view that never leaves the workstation: both texts rendered on the client, no new model call, no logging of the note body to the analytics stream. Write what you will refuse (a cloud "diff explanation" that uploads the note). The follow-on is a useful surface that would quietly break the data-rights row if you built the obvious version.

#### Interview angle

Read the partial-support copy and the reason a faithful-but-incomplete draft is worse than silence. Then mention the combined-ask fix. Experience design here is a safety choice.

### Days 73–74 — Retrieval Failure Postmortem

Working copy and fixtures: [phase-07-rag-product/day-73-74-retrieval-postmortem/README.md](phase-07-rag-product/day-73-74-retrieval-postmortem/README.md)

**Days 73–74 · Phase 7, Retrieval-Augmented Product Design · Advanced**

**Case.** In week 6 of the limited pilot, a Columbus handler committed a note for an Ohio personal-auto notice. The draft cited a rental limit of $40 per day from a document titled "PP 00 01." The document was a commercial-auto form that shared a short title with the personal-auto form. The handler opened the citation, saw familiar rental language, and committed. A supervisor caught it two days later because the form code prefix was wrong. No claimant decision had been sent. The limit on the correct personal-auto form, as amended, was $30. This postmortem is fictional and is the practice case.

#### Concept

A postmortem after a bad citation is a product review of how several layers agreed to be wrong together: corpus boundary, retrieval, citation display, handler training, and the commit step. Its output is a set of changes to requirements, specs, and gates, with owners and dates. A narrative that ends in "the model hallucinated" is not finished, and in this scenario it is also inaccurate. The commercial form was a real document. It was the wrong document. That distinction changes the fix.

#### Approach

Write the postmortem in a structure a claims organization can accept:

- **Facts.** Timeline from retrieval to supervisor catch, using only the scenario above plus behaviors you already specified. When you need a fact the scenario does not give (how the commercial form entered the index), write it as an unknown and list the question, rather than inventing a comforting cause.
- **Impact.** What reached the file, what did not (no claimant message), and what the residual risk is (the note is still in Lumen until someone corrects it).
- **What each layer allowed.** Corpus policy, reason codes, citation schema, answer experience, training, commit. For each, say whether the layer behaved as specified and the spec was weak, or the implementation violated the spec. You do not have an implementation; do this as "if we had built exactly the specs so far, would this have been possible?" That question is the value of the exercise. For example, your corpus boundary excluded commercial forms. A retrieval that returned one means either the spec was not testable, or this scenario assumes a violation. Pick the reading that matches your actual documents, and if your golden set's two wrong-line items would have caught a commercial form only when the notice was commercial, say that. The hole may be "a commercial form returned on a personal notice," which your set might already cover. Look at your rows. If it covers them, the postmortem's question becomes detection speed and the handler's ability to see the prefix, not set coverage.
- **Detection.** The supervisor caught it in the ordinary sample. The product did not catch it. Write the detection gap in one sentence.
- **Actions.** Each action changes a spec, a golden-set row, a citation field, a training line, or a gate. Each has an owner and a date inside the remaining pilot, or an explicit "next pilot" mark. Include the correction of the committed note as an operational action, not only a product action.
- **What we are not doing.** A model retrain as the primary action, unless your layer analysis says the drafter invented the $40 rather than quoting the wrong real form. In this scenario it quoted a real form. Write the refusal.

Use the incident addendum from the comms system for the hour-of note, and check that the postmortem's facts match the note a handler would have been sent. If the addendum's handler sentence is wrong for this incident ("stop using Harbor" versus "open the form prefix before you commit"), revise the sentence and record the revision. The postmortem that does not update the incident copy leaves the next incident on the old words.

#### Components

- **Timeline and unknowns.**
- **Layer analysis.** Spec-weak versus spec-violated, for each layer, grounded in your documents.
- **Action list.** Owner, date, artifact changed. Include the file correction.
- **Refusal.** The primary action you will not take, and why.
- **Comms revision.** The handler sentence, updated if needed.

#### Flow

1. Write the timeline. Mark unknowns in a separate list so they do not become fake facts by the last page.
2. Walk each spec. Quote the line that would have prevented the miss, or write that there is no such line.
3. Draft actions from the holes only. An action that does not cite a hole is extra credit the pilot cannot afford.
4. Write the refusal and the file-correction action.
5. On day 74, read the postmortem next to the golden set. Add or retire a row if the set would still pass while this bug lives. Record the row id.

#### Tools and stack

Markdown. Your own earlier specs as the system under review. No log platform. The discipline is holding the scenario against the documents you wrote.

#### Setup

1. Create `harbor-portfolio/73-postmortem/postmortem.md`.
2. Have the corpus policy, golden-set rules, and answer-experience states available.
3. Day 73 is timeline, layers, and unknowns. Day 74 is actions, the refusal, the comms revision, and the golden-set edit.

#### Deliverables

- A postmortem with unknowns separated from facts.
- Layer analysis quoting your specs.
- Actions with owners, a refused action, a comms revision if needed, and any golden-set row change.

#### What done looks like

The write-up does not blame "hallucination" for a wrong real document. At least one action changes a spec or a test row, not only a prompt. The committed note has a correction action. Unknowns are listed. A reader can see whether the specs you have today would have made the incident possible.

#### Think a step ahead

The commercial form was the wrong product in the right company. The next incident is the right product in the wrong tenancy: a passage from another carrier's form, or another Northline customer's policy packet, retrieved because it was embedded in a shared index. Write the product requirement that would make that incident a failed gate rather than a surprise. Passages must carry a tenant and a corpus-class marker, retrieval must filter on both before any passage reaches the drafter, and a golden-set row must try to retrieve across that boundary and expect zero hits. State the pilot behavior if the marker is missing on even one document: that document is not retrievable, and the reason is logged. The follow-on is isolation, which content similarity will never give you.

#### Interview angle

Tell the story in four sentences ending in the action that changes a test, not a prompt. The refused retrain is the judgment.

## Phase 8 — Evaluation and Harness Practice

**Days 75–86 · Advanced · 6 projects**

### Goals

This phase decides what evidence is allowed to block a release. You bind behaviors to methods and gates, and you keep contract probes from being averaged into a blended score. You write rubric anchors a second grader can apply, a charter that declines a single general-quality set, and a ship note on a fixture report that tempts you to ship a style win over a missing probe run. You specify a harness by the strings it must refuse to print, and you install the weekly meeting that can continue, restrict, or pause the pilot. The phase is done when a runner cannot recommend shipping and a single bad committed sentence has a same-day path.

### Skills covered

Evals, AI evals, and harnesses: evaluation strategy, anchored rubrics, gold-set governance, ship notes, harness requirements, production quality rituals.

### Days 75–76 — Evaluation Strategy

Working copy and fixtures: [phase-08-evals-harnesses/day-75-76-eval-strategy/README.md](phase-08-evals-harnesses/day-75-76-eval-strategy/README.md)

**Days 75–76 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Harbor has several behaviors a reasonable person might "evaluate": edition selection, bulletin precedence, retrieval reason codes, sentence support, out-of-job refusals, citation display, and the audit-priority score. They do not belong in one score. The pilot has a shadow-week gate and a limited-pilot gate. The strategy says which evidence must exist at each gate, who looks at it, and which fashionable evaluations you are not running.

#### Concept

An evaluation strategy is the map from decisions to evidence. It chooses a small number of checks, assigns each a method and an owner, and states what the check is allowed to block. A single "quality score" that averages a refusal task with a rental-limit task will move when either moves, and the gate will become a negotiation. The strategy exists to prevent that negotiation from being improvised.

This project writes the strategy for Harbor. It does not build a harness. The harness requirements on days 83–84 have to serve this document, so this one comes first.

#### Approach

Make a table of behaviors. For each: the decision it informs, the method, the artifact that already holds the expected answers, the gate it can block, and the person who can waive it. Methods to use, and to keep distinct:

- **Rule check.** Edition id and bulletin id against the catalog. Exact. Can block shadow week.
- **Set grading.** The golden question set's reason codes and ids. Can block shadow week. Slice floors from that project, not a blended accuracy.
- **Rubric grading.** Sentence support and tone, on items a trainer scores with the labeling guideline. Can block the limited pilot's prose drafts. Cannot, by itself, block citation-only mode if you have a fallback.
- **Contract probes.** A handful of scripted asks for coverage and claimant messaging. A single failure blocks. These are not averaged.
- **Human spot review.** The monthly sample from the error-analysis follow-on. Informs the card's failure-mode list. Does not by itself expand the pilot to another state.
- **Online proxies.** Citation opened before commit, discard rate, no-source rate. These watch the pilot. They are not offline "evals," and the strategy says so, because they measure handler behavior and product fit together.

Explicitly out of this pilot's strategy, with a reason: a public benchmark score, a preference-model leaderboard, a single overall grade from an automated judge, and a vendor's self-reported accuracy. You may revisit an automated judge after a person has graded a sample large enough to see whether you agree with it. Until that agreement is measured, a judge does not gate. Write that as a sequencing rule, not as a permanent ban.

Write the waiver path. A slice floor can be waived only by the claims operations A on the offline-eval gate, in writing, for one week, and a waived floor is reported as waived on the VP page. A failed contract probe cannot be waived.

#### Components

- **Behavior table.** The columns above. Every behavior you have specified in earlier projects should appear or be consciously omitted with a reason.
- **Gate binding.** Which rows block shadow week, which block prose in the limited pilot, which only inform.
- **Out-of-strategy list.** With reasons and the sequencing rule for automated judges.
- **Waiver path.** Who, how long, how it shows up on the VP page.
- **Owner load.** Hours per week the trainer and the content analyst are actually spending on evals during the pilot, checked against the capacity assumption in the sprint-goal follow-on. If the strategy needs more hours than they have, cut a row. A strategy that cannot be staffed is a poster.

#### Flow

1. Inventory behaviors from the interaction contract, the retrieval requirements, and the labeling guideline. This is a coverage check on your own work.
2. Assign methods. If two methods are guarding the same decision, keep the one that can fail clearly and demote the other to informational.
3. Bind rows to gates. Bind the contract probes to a non-waivable fail.
4. Write the out-of-strategy list before anyone asks for a leaderboard in the review.
5. On day 76, staff the strategy. Cut or defer a row if the hours do not fit, and record the cut as a risk, not as a silent omission.

#### Tools and stack

Markdown. Earlier specs as the inventory. No eval framework. The table is the strategy. A framework that appears later is acceptable only if it implements a row in the table.

#### Setup

1. Create `harbor-portfolio/75-eval-strategy/strategy.md`.
2. Start with the inventory so beloved metrics cannot crowd out contract probes.
3. Day 75 is the table and gate binding. Day 76 is waivers, the out-list, and the staffing cut.

#### Deliverables

- A behavior table bound to gates.
- A non-waivable probe rule and a waiver path for slice floors.
- An out-of-strategy list and a staffing note that cuts or confirms the plan.

#### What done looks like

No blended quality score gates the pilot. Contract probes can fail the gate on a single item. Automated judges are sequenced behind an agreement check you have not pretended to complete. The trainer's hours are a constraint you applied. Every row points at an artifact that holds the expected answer, or the row says the artifact is still missing.

#### Think a step ahead

Online proxies arrive while you are still changing the product, so a week-over-week move mixes product changes with model changes. Add a calendar rule: any week that contains a corpus publish, a prompt or model version change, or a new handler cohort is marked "confounded" in the review, and the online proxy is reported as a watch item rather than as evidence for a gate. Write the three confounders and who marks the week. The follow-on is interpretive discipline, which a clean dashboard will not apply for you.

#### Interview angle

Explain why a single quality score does not gate Harbor, and which failure cannot be waived. Strategy is the binding, not the catalog of metrics.

### Days 77–78 — Anchored Quality Rubric

Working copy and fixtures: [phase-08-evals-harnesses/day-77-78-anchored-rubric/README.md](phase-08-evals-harnesses/day-77-78-anchored-rubric/README.md)

**Days 77–78 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Prose drafts that survive retrieval need a grader's rubric. The labeling guideline already covers two crisp judgments: whether the source set is correct, and whether a sentence is supported or out of job. What remains is the judgment a trainer makes when the sentence is supported and still a bad note: it buries the limit, it adds advice, it sounds like a denial, or it is so long the handler will not read it. Those judgments need anchors, or two trainers will produce two pilots.

#### Concept

An anchored rubric is a scale where each score point has an example, so a grader matches the draft to an anchor instead of reaching for an adjective. For Harbor you will write a short rubric with three criteria, anchors at three levels, and a precedence order for when criteria conflict. You will also write the instruction that keeps this rubric from quietly replacing the contract probes. A draft can score well on tone and still be a failed contract probe. The probe wins, and the rubric does not get to average that away.

#### Approach

Use three criteria:

1. **Faithfulness.** The draft stays inside the cited spans and the precedence rules. This overlaps the sentence-support label on purpose at the low end. The rubric's job at the high end is partial faithfulness: a limit is right and a harmless extra sentence is not in any source.
2. **Task fit.** The draft is a note a supervisor can audit: it includes the edition and the amended limit when one applies, and it omits coverage conclusions and claimant messages.
3. **Usability.** A handler can check it during the handle time you are willing to spend. Concrete and short. A faithful note that pastes an entire form fails usability.

Levels for each criterion: `fail`, `meet`, `exceed`. Write an anchor paragraph or sentence for each level, using fixture language marked as fake. Anchors are specific. "Somewhat faithful" is not an anchor. A `fail` faithfulness anchor quotes a $40 limit when the fixture span says $30. A `meet` quotes $30 and cites the bulletin. An `exceed` does that and flags the superseded bulletin without letting it be copied by accident, matching your citation behavior.

Write conflict precedence. Faithfulness and task fit outrank usability. A short coverage denial is a `fail` on task fit even if it is short, polite, and confident. Usability never rescues it. Between faithfulness and task fit, a contract violation (coverage, claimant message) is a task-fit fail even if the words appear in a cited insuring agreement. That matches the labeling precedence. State it again here so the rubric cannot drift.

Write grader instructions: grade the draft the handler would see, not the draft you can tell the model "meant"; do not fix the draft in the margin and then grade your fix; if the retrieval reason was not `ok`, do not grade prose, because there should not be prose. A rubric applied to a no-source state will invent scores.

Include a disagreement example. Two graders differ by one level on usability for a draft that includes a correct rental limit plus a redundant sentence. Show how your anchors resolve it, or revise the anchors until they do. If they cannot, mark usability as a criterion that needs a second pass before it is allowed to block anything. The strategy already says rubric grading can block prose. A criterion that cannot be anchored should be informational only. Update the strategy table in a short note if you demote one.

#### Components

- **Rubric.** Three criteria, three levels, anchors in fixture language.
- **Precedence.** Including the contract-probe override.
- **Grader instructions.** One page.
- **Disagreement example.** Resolved, or a demotion note.
- **Score form.** The actual row a trainer fills: item id, retrieval reason, three levels, probe fail (yes/no), comments. No overall average column. Leave it off on purpose and say why.

#### Flow

1. Draft anchors before definitions. If you cannot write the `fail` example, you do not yet know the criterion.
2. Add precedence and the probe override.
3. Build the score form without an average. Notice the urge to add one, and write the sentence that resists it.
4. Run the disagreement example yourself, then with a partner if you can.
5. On day 78, grade three imaginary drafts you write to the anchors: an obvious fail, a meet, and a sneaky fail that is usable and unfaithful. If the sneaky one can score `meet` on every criterion, the anchors are too loose and you tighten them.

#### Tools and stack

Markdown. The labeling guideline and the interaction contract as constraints. No judge model. A rubric that has not been applied by a person should not be handed to a model to apply at scale. That sequencing matches the eval strategy.

#### Setup

1. Create `harbor-portfolio/77-rubric/rubric.md` and `score-form.md`.
2. Ban the overall average at the top of the score form so it does not creep into a column "for convenience."
3. Day 77 is anchors and precedence. Day 78 is the disagreement, the three practice grades, and any demotion.

#### Deliverables

- An anchored rubric with precedence and grader instructions.
- A score form without an average.
- Three practice grades, including a sneaky fail, and a note if a criterion was demoted.

#### What done looks like

A second grader can match your level on the sneaky fail using the anchors alone. Contract failures cannot be averaged into a pass. The no-source state is not scored as prose. The form a trainer fills matches the strategy's refusal of a blended score.

#### Think a step ahead

Anchors written this week describe this month's bulletin style. When a new circular class enters the corpus, graders will stretch "faithfulness" to cover it. Add a rubric version and a rule: new source classes require a new `fail` anchor before graders score those items, and scores from the old rubric version cannot be compared to scores from the new one in the same table. Write `rubric-v1` on the form. The follow-on is comparability, which a team will destroy the moment the corpus grows if you have not forbidden the comparison.

#### Interview angle

Read the sneaky fail and the level you gave it. Then point at the missing average column and say why it is missing.

### Days 79–80 — Gold-Set Charter

Working copy and fixtures: [phase-08-evals-harnesses/day-79-80-gold-set-charter/README.md](phase-08-evals-harnesses/day-79-80-gold-set-charter/README.md)

**Days 79–80 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Harbor now has more than one curated set: 25 retrieval rows, 15 labeling examples, contract probes, and rubric anchors that quote fixture spans. They will be copied into slides, pasted into prompts, extended by whoever is online, and used to claim a gate passed. A charter is the rulebook that keeps a set from becoming a prop.

#### Concept

A gold-set charter names each set, its purpose, its owner, what it is allowed to gate, how items are added and retired, how leakage is prevented, and what must be true before a number from that set is spoken in a VP review. It is governance for a small pile of files. The pile is small enough that governance feels like overhead, which is why the charter has to be short enough to be kept.

This project writes the charter for the sets you already have and for the one set you do not have yet and will be asked for: a "general quality" set that blends everything. The charter declines that set.

#### Approach

One section per existing set, plus a declined section. For each living set:

- **Purpose.** The decision it supports, copied from the eval strategy, not reinvented.
- **Unit and schema.** Point at the file. Do not fork a second schema in the charter.
- **Owner and editor.** One owner. Editors may propose rows; the owner accepts. For the retrieval set the owner is the content analyst. For contract probes the owner is product, with legal consulted when a probe's expected behavior changes.
- **Gate use.** What it may block, matching the strategy. If this project and the strategy disagree, fix one of them in this pass and say which you changed.
- **Change control.** New ids, no renumbering, retirement notes, version on every row. You already wrote pieces of this. The charter is where they become one policy.
- **Leakage controls.** Not used as few-shot examples. Demo runs that use set items are tagged `demo` and excluded from gate reports. A set file does not live in the same repository directory as prompt text. Write the directory rule even if both are just folders in a portfolio; the habit is the point.
- **Reporting minimum.** Below a stated count, or below a slice floor, the report says "not reported" rather than a percent. Reuse the floors you already set. Where you never set one, set it here.

The declined "general quality" set gets a short section: the reason a blended set invites a blended score, the stakeholder sentence you expect ("we need one number"), and the alternative you will offer (the VP page's three separate figures). Do not create the set "just so we have it."

Add a sampling rule for growth. When a set grows past a size you choose (for example, 100 retrieval rows), gate reports move from "full set" to "full set on contract probes, stratified sample on the rest," and the charter names who draws the sample. Until that size, you run the full set, because 25 rows that are sampled into 10 are theater.

#### Components

- **Set sections.** Purpose, owner, gate, change control, leakage, reporting minimum.
- **Declined set.** The blend, with the alternative offer.
- **Directory and demo rules.** Where files live relative to prompts, how a demo is tagged.
- **Disagreement log.** Any place you changed the eval strategy or a set's earlier rules to match the charter.
- **Growth rule.** The size at which you stop implying that every row runs every day, and what replaces it.

#### Flow

1. List the sets you actually have files for. A set that exists only as a paragraph in an earlier README is marked "not chartered until the file exists."
2. Fill owners. If the content analyst owns every set, say so and cut the gate scope until the hours from the strategy still hold.
3. Write the declined blend and the sentence you will say in the meeting.
4. Reconcile with the strategy. Record every edit.
5. On day 80, simulate a helpful engineer pasting three golden notices into a prompt "as examples of good behavior." Write the review comment you leave, citing the charter section. The comment is a deliverable. It shows the charter can be applied.

#### Tools and stack

Markdown. The set files and the eval strategy. No annotation platform. Governance at this scale is a short document people can find.

#### Setup

1. Create `harbor-portfolio/79-charter/charter.md` and `review-comment.md`.
2. Inventory files first so you do not charter ghosts.
3. Day 79 is set sections and the declined blend. Day 80 is reconciliation, the growth rule, and the review comment.

#### Deliverables

- A charter covering the living sets and declining the blended set.
- A disagreement log of reconciliations.
- A review comment that applies the leakage rule to a concrete paste.

#### What done looks like

Each living set has one owner and a gate that matches the strategy. The blended set does not exist. The review comment cites a section and tells the engineer where examples may come from instead (a separate, non-gating example file, which you may create as an empty file with a header that says it is not a gold set). Reporting minimums are in counts. Growth has a rule before the set is large.

#### Think a step ahead

Sets that gate releases become targets. A team will write drafts that pass the 25 retrieval ids and fail the notice that arrives on Thursday. Add a holdout rule. A fraction of new items you choose (for example, one in five, with a minimum of five items once the set is large enough) is marked `holdout`, excluded from any prompt-development loop, and reported separately. Developers do not get the holdout expected answers in the everyday file; the owner runs that slice. Write how small Harbor's current set is and the size at which the holdout rule turns on. Turning it on at 25 may be too early; leaving it off forever guarantees a set that has been memorized. Pick the threshold and the reason.

#### Interview angle

Explain the declined set and the review comment. You are showing you can govern an eval asset, not only author one.

### Days 81–82 — Eval Ship Note

Working copy and fixtures: [phase-08-evals-harnesses/day-81-82-eval-ship-note/README.md](phase-08-evals-harnesses/day-81-82-eval-ship-note/README.md)

**Days 81–82 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** A new drafting build, `draft-19`, is proposed to replace `draft-18` during the Columbus pilot. You have a fixture report, not a harness and not a leaderboard account. Your job is the ship note: the recommendation, the claims you will allow in the release meeting, and the slice that blocks the change. The note is the product decision. The report is the evidence.

#### Concept

A ship note answers whether a specific change is allowed to reach handlers, given an eval strategy you already wrote. It quotes the strategy's gates rather than inventing a new bar in the meeting. It treats small slices as small, and it treats a regression on a non-waivable behavior as blocking even when the headline number improved. Most release arguments do the reverse. This project practices the harder reading.

#### Approach

Read [`fixtures/eval_report.md`](fixtures/eval_report.md) before you write a recommendation. The report is the only evidence you may use for this decision. Where it is silent, the note says "not in the report," and that silence is itself an input. In particular, check whether contract-probe results are present, whether slice sizes are present, and whether a confounded week (a corpus publish in the same window) is flagged.

Write the note in a fixed shape:

1. **Change.** What `draft-19` is, in one sentence, taken from the report's header. Do not add hoped-for benefits the header does not claim.
2. **Strategy reminder.** Which rows of your eval strategy this report can speak to, and which it cannot. If the report has no contract-probe section, it cannot clear the non-waivable probe, and prose cannot ship on this report alone.
3. **What improved.** Direction, size, and n, for slices large enough that your charter allows a number.
4. **What regressed.** Same discipline. A regression on a slice below the reporting minimum is described as a watch item with the count, not as a rate you then treat like a precise regression.
5. **Recommendation.** Ship, ship behind a restriction, or do not ship. A restriction has to be a behavior you can actually enforce with the specs you have, such as "citations-only for glass-only notices" or "do not ship; probes missing." "Ship but watch closely" is not a recommendation unless you name the watch, the threshold, and the person who will pull it.
6. **Allowed sentence and refusals.** One sentence for the release meeting, and at least three sentences you will not say. One of them is about overall quality moving in a blended way.

If your recommendation depends on a fact the report omits, the recommendation is "not yet," and the note ends with the smallest addition that would let you decide. That addition is a request to the set owner, not a request for a more flattering chart.

#### Components

- **Ship note.** The six parts, no longer than two pages.
- **Trace.** A short list mapping each claim in the note to a row in the fixture report.
- **Restriction or request.** Either an enforceable restriction or the smallest missing evidence. Not both as a hedge. Pick the one your recommendation actually uses.
- **Strategy conflict.** If the report invites a decision your strategy forbids, quote both and follow the strategy. Record whether the strategy should change after this, as a separate question you will not answer inside the ship meeting.

#### Flow

1. Read the report and annotate regressions and missing sections before you form a recommendation. Write the annotations in the margin of your note.
2. Check the charter's reporting minimums against every percent in the report. Mark percents you are not allowed to repeat.
3. Draft the recommendation. Then try to weaken it into "ship with monitoring," and reject that weakening unless the watch is real.
4. Write the allowed sentence last, from the recommendation, not from the best cell in the table.
5. On day 82, have a partner argue for shipping because the largest slice improved. Answer from the note. If the answer is not in the note, the note is missing a refusal. Add it.

#### Tools and stack

Markdown. The fixture report, your eval strategy, and the charter. No scoring code. If a percent and a count in the report disagree, trust the count, note the inconsistency, and do not "clean it up" by editing the fixture. The ability to notice a bad row is part of reading a report.

#### Setup

1. Create `harbor-portfolio/81-ship-note/note.md`.
2. Open [`fixtures/eval_report.md`](fixtures/eval_report.md) and do not modify it. It is the evidence as received.
3. Day 81 is annotation, trace, and recommendation. Day 82 is the partner argument and the final refusals.

#### Deliverables

- A ship note with a recommendation and a trace back to the fixture.
- An allowed sentence and at least three refusals.
- Either an enforceable restriction or a request for the smallest missing evidence.

#### What done looks like

The recommendation follows the strategy when the report tempts you off it. Slice sizes are respected. A blended improvement cannot carry a regression the strategy treats as blocking, if the report contains one; if it does not, you say so and you do not invent one. The partner's "largest slice" argument has a refusal written down. Every number in the note appears in the trace.

#### Think a step ahead

Suppose the note's recommendation is to ship behind a restriction for one line of business or one claim subtype. The next problem is ending the restriction. Write the exit condition now: which slice floors must be met, on which set version, for how many consecutive runs, and who removes the restriction. A restriction without an exit becomes either a permanent shadow product or a restriction everyone ignores in week two. Pick the condition that matches your actual recommendation, or write the exit condition you would have used if you had restricted, and label it hypothetical if your recommendation was a flat no.

#### Interview angle

Give the recommendation in one sentence and the cell that drove it. Then one refusal. Ship notes are credibility documents.

### Days 83–84 — Harness Requirements Brief

Working copy and fixtures: [phase-08-evals-harnesses/day-83-84-harness-brief/README.md](phase-08-evals-harnesses/day-83-84-harness-brief/README.md)

**Days 83–84 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Harbor's eval strategy names the checks that can block a gate. Today those checks are run by a content analyst with a spreadsheet and a golden file. That is appropriate at 25 rows. It will be abandoned the first week someone runs the set twice. A harness is the repeatable runner: it takes a set version, a candidate build, the scorers the strategy allows, and it emits a report a ship note can cite. This project writes the requirements for that runner. It does not implement one.

#### Concept

A harness requirements brief is the product spec for an internal tool. It says what the runner must refuse to do as clearly as what it must do, because an eval runner that can silently drop a failing slice will be used to ship. The readers are the engineer who might build it and the content analyst who will live in its output. The brief is written so a later implementation can be accepted or rejected against it, including an implementation that already exists elsewhere in the company. Reusing a runner is allowed. Watering down the strategy to fit a runner is not.

#### Approach

Specify the harness as a job, the way you specified retrieval.

**Inputs.** A set file with a version, a candidate build id (prompt version, model version, corpus version, rule-layer version), and a scorer configuration that is an allow-list. The allow-list for Harbor is: exact match on retrieval ids and reason codes, contract-probe pass/fail, and rubric levels entered by a named grader or imported from a grader's form. A mean of mapped rubric points is not on the allow-list. The fixture ship report included one. The brief exists so the next report cannot.

**Run record.** Every run stores the set version, the build id, the time, the person or job that started it, and whether the run is tagged `demo`. Demo runs cannot be selected as evidence in a ship note. The report header shows the tag in the first line, not the footer.

**Scorers.** Exact-match scoring for the retrieval set must fail a row when extra ids are returned, not only when an expected id is missing. The commercial-form incident is an extra-id failure. A scorer that only checks recall of the expected id would have passed a run that also returned the wrong form.

**Slice reporting.** The report shows every slice in the charter, including slices with zero misses, and it shows counts beside any rate. Slices under the reporting minimum display the count and the words "not reported," and the runner does not print a percent the charter forbids. The runner does not print an overall percent for the retrieval set. It may print "all slice floors met" or "floors missed," listing which.

**Contract probes.** If the candidate is a drafting change and the probe file was not executed, the report's recommendation field is `incomplete`, and the harness must not emit the runner's prose opinion. The fixture report's "ship it" line is a behavior the harness is required to make impossible. People can still write a ship note. The runner does not get a vote.

**Human rubric import.** The harness accepts a score form and checks that the rubric version matches `rubric-v1`, that an overall average column is absent, and that prose rows with a non-`ok` retrieval reason have no rubric score. It stores the grader's name. One grader is allowed and must be visible. The report cannot say "the rubric passed" without the grader.

**What the harness is not.** It is not a place to edit expected answers. Edits happen in the set file under the charter, and the next run picks up the new version. It is not a prompt playground. It is not a dashboard for executives. The ship note remains the decision document; the harness report is the evidence the note traces to.

Write acceptance tests for the brief itself, in plain language, so an implementation can be rejected:

1. A retrieval row that returns the expected id plus a commercial-form id fails the row.
2. A drafting run with no probe results emits `incomplete` and no ship recommendation.
3. A slice of n=2 has no percent in the output.
4. A demo-tagged run cannot be attached to a ship note template the harness generates. The harness may generate a blank ship-note skeleton with the build id filled in and the recommendation left blank. It does not fill in "ship."

#### Components

- **Job statement.** Inputs, run record, outputs.
- **Scorer allow-list and deny-list.** Including the banned mean.
- **Report schema.** Header, slice table, probe section, incompleteness rule.
- **Acceptance tests.** The four above, plus one you add for the charter's retirement rule: retired ids do not count toward a floor.
- **Reuse note.** Questions you would ask of an existing internal runner before adopting it, mapped to the acceptance tests. If it cannot hide a percent the charter forbids, it does not get Harbor's sets.

#### Flow

1. Start from the behaviors the strategy says can block a gate. The harness has to be able to fail those, and only those, automatically.
2. Write the deny-list from the fixture report's actual mistakes: a blended mean, a skipped probe section, a runner recommendation.
3. Write the report schema so a ship note's trace has stable row names to cite.
4. Write acceptance tests. If a test does not correspond to a real way the fixture report misled a reader, cut it or replace it. The tests are not a tour of harness features.
5. On day 84, take one acceptance test and specify the exact fixture input and the exact forbidden string in the output. Hand it to an engineer. If they can satisfy the letter and still print the percent in a chart image, tighten the test to cover the chart's data file, not only the markdown report.

#### Tools and stack

Markdown. The eval strategy, the charter, and the fixture eval report as the failure examples. No test framework and no runner code. A later implementation that needs a repository, a command, and a locked set version should be able to start from this brief without a second product discovery pass.

#### Setup

1. Create `harbor-portfolio/83-harness-brief/brief.md`.
2. Paste the four acceptance tests as checkboxes you will be able to apply to someone else's runner.
3. Day 83 is the job, the allow-list, and the report schema. Day 84 is acceptance tests, the reuse note, and the tightened test.

#### Deliverables

- A harness requirements brief with an allow-list, a deny-list, and a report schema.
- At least five acceptance tests, one of them tightened against a loophole.
- A reuse note for an existing runner.

#### What done looks like

An engineer can say whether a runner passes or fails the brief without asking you how you feel about it. The runner is forbidden to recommend shipping. Extra retrieved ids fail the row. Small slices cannot appear as percents. The ship note stays a human document. Retired rows cannot pad a floor.

#### Think a step ahead

Harbor's real task is not one answer. It is a trajectory: open the notice, bind the edition with the rule layer, retrieve, draft or withhold, and commit or hand off. A final-answer scorer will mark a run correct when the draft looks right and the rule layer was skipped. Extend the brief with a trajectory score requirement, still as a requirement and not as code. The run must record which component produced the edition id, and a draft that appears without a rule-layer decision in the trace fails even if the prose matches the fixture. Write the trace fields and the fail condition. The follow-on is scoring the path, which answer-only evals will flatter.

#### Interview angle

Describe one thing the harness is forbidden to output, and the fixture report habit that made the ban necessary. You are specifying a tool by the mistake it must not repeat.

### Days 85–86 — Production Quality Ritual

Working copy and fixtures: [phase-08-evals-harnesses/day-85-86-quality-ritual/README.md](phase-08-evals-harnesses/day-85-86-quality-ritual/README.md)

**Days 85–86 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** The limited pilot is live for forty Columbus handlers. Offline gates have already done their job or been explicitly waived. What remains is a weekly hour in which a small group looks at production signals and decides whether the pilot continues unchanged, restricts a slice, or pauses drafts. Nobody in that hour is allowed to discover the agenda from scratch. This project writes the ritual: who sits down, which numbers are on the table, which numbers are banned from the table, how a single bad note becomes an incident, and what "pause" actually does to a handler at 9:00 a.m.

#### Concept

A production quality ritual is an operating cadence with a pre-committed decision set. It is not a dashboard and not a model monitor. Dashboards show figures. Monitors page people. The ritual is where a person decides, using the eval strategy's rule that online proxies are watch items unless the week is unconfounded, and using the interaction contract's rule that one out-of-job sentence in a committed note is an incident even when the rate is flattering.

You will write the agenda, the packet that must exist before the meeting starts, the three decisions the meeting is allowed to make, and the handler-facing consequence of each decision.

#### Approach

The meeting is 45 minutes, weekly, on a morning the Columbus manager can attend. Attendees: product (runs the agenda), the content analyst (set owner), the Columbus manager, and engineering only when a pause or a corpus action is on the table. Legal is informed the same day if the decision is a pause caused by a data-rights row, and is not required for a routine week.

**Packet, due the evening before.** One page:

- North-star and guardrail from the metric tree, with the comparison the dashboard spec requires, or "audit file late" in the degraded copy.
- Online proxies: share of commits with a citation opened, no-source rate, discard rate, drafts over the token ceiling. Each with n.
- Week marks: confounded or not, per the strategy follow-on (corpus publish, model or prompt version, new cohort).
- Incident count: committed notes where an out-of-job sentence was found, including zero.
- Open RAID rows that changed state.
- The packet does not include drafts per handler, a blended quality mean, or a handler leaderboard.

**Decisions the meeting may make.**

1. **Continue.** The default. Allowed when no incident is open, no non-waivable probe is known failed on the current build, and the guardrail is not in its veto state. Continue does not require the north-star to have moved. A quiet week is a result.
2. **Restrict.** Remove prose for a named slice (glass-only, or any notice with `bulletin_missing`) and leave citations or the Lumen-only path. The restriction uses the exit condition pattern from the ship-note follow-on: slice, set version, consecutive clean runs, owner who removes it.
3. **Pause drafts.** Harbor stops showing drafts. Handlers write notes in Lumen as before. Citations may remain only if the failure is in prose, not in retrieval. If the failure is a wrong document class, citations pause too. The pause is a gate failure, communicated with the same-day note from the comms system.

**Decisions the meeting may not make.** Expand to another state. Change a principle. Add a document class to the corpus. Those have their own forums. Write this negative list on the agenda so the meeting does not become the easiest place to widen scope.

**Single-note rule.** Any committed out-of-job sentence, or any confirmed wrong-library citation, opens the incident addendum the same day. It does not wait for Thursday's ritual. The ritual's job on that week is to confirm the incident action and to decide continue, restrict, or pause for everyone else.

Write the first three weekly packets as filled examples: a quiet week, a confounded week, and an incident week. Use numbers you label as illustrative, or use counts from the activation fixture scaled honestly as "too small to be the pilot." Do not present illustrative numbers as pilot results. The point of filling the packet is to see whether the decision rules fire.

#### Components

- **Agenda and roles.** 45 minutes, timed blocks, including a five-minute block for "decisions we are not making."
- **Packet template.** With the banned fields listed at the top.
- **Decision rules.** Continue, restrict, pause, each with the handler-facing consequence and the comms template to use.
- **Three filled packets.** Quiet, confounded, incident, each ending in the decision the rule requires.
- **Pause mechanics.** What a handler sees the next morning, who flips the switch, and how a paused week is marked so it is not later used as an activation rate.

#### Flow

1. Write the decision rules before the packet. The packet is only the evidence those rules need.
2. Ban fields by naming the behavior they create. A leaderboard creates speed pressure of the kind Andre described.
3. Fill the three packets and apply the rules. If two packets lead to the same decision for mushy reasons, tighten the rule.
4. Write pause mechanics as a handler-visible state, not as an internal flag.
5. On day 86, run the 45-minute agenda alone with the incident packet, out loud, with a timer. Cut agenda items you skipped. An agenda that does not survive its worst week is the wrong agenda.

#### Tools and stack

Markdown. The dashboard spec, the eval strategy, the comms templates, and the metric tree. No monitoring vendor. The ritual has to be runnable with a one-page packet assembled by a person, because the pilot is forty handlers and the first missed Thursday will be a Thursday when the warehouse is late.

#### Setup

1. Create `harbor-portfolio/85-ritual/ritual.md` and three packet files, or one file with three sections.
2. Put the negative decision list in the agenda before you write welcoming prose.
3. Day 85 is rules, packet template, and banned fields. Day 86 is the three packets, pause mechanics, and the timed run-through.

#### Deliverables

- A 45-minute agenda with a negative decision list.
- A packet template and three filled packets that each produce a required decision.
- Pause mechanics a handler would notice the next morning.

#### What done looks like

A quiet week can end in "continue" without anyone hunting for a win. A confounded week cannot be used as expansion evidence, and expansion is not even on the menu. One bad committed sentence triggers the incident path the same day, not at the ritual. The pause state tells the handler what to do at 9:00 a.m. Banned fields are written down.

#### Think a step ahead

The same week can contain a real model regression and a real product change, and the confounder flag will correctly stop you from using the proxy while also stopping you from acting on the regression. Add a separation note. When the week is confounded, the ritual may still order a targeted offline rerun of the golden set and the contract probes on the current build, and that rerun — not the online proxy — is what can justify a pause. Write who kicks off the rerun, the maximum hours you will wait for it, and the default if it is late (restrict prose, because waiting without a decision is a decision). The follow-on keeps a confounded week from becoming a week in which nobody is allowed to act.

#### Interview angle

Walk the incident week from the single note to the handler's next morning. The ritual is real if the floor can feel the decision.

## Phase 9 — Data Pipelines and Trust

**Days 87–94 · Advanced · 4 projects**

### Goals

This phase designs the pipelines that keep the earlier promises true after launch week. Human feedback can become a reviewed evaluation candidate and cannot become a training set by configuration. Analytics numbers can be withheld when a bot, a missing build, a late audit file, or a bad join produced them. The corpus moves from intake to published to withdrawn on a clock, fail-closed. Any future training row carries lineage, and a deletion that arrives after a model consumed the row has a real choice rather than a slogan. The phase is done when each pipeline has an owner, a stop, and a behavior the handler or the Monday packet can feel.

### Skills covered

Pipelines and data analytics operations: human-feedback flow, analytics trust, knowledge publishing, training-data lineage and deletion.

### Days 87–88 — Human Feedback Pipeline

Working copy and fixtures: [phase-09-pipelines/day-87-88-feedback-pipeline/README.md](phase-09-pipelines/day-87-88-feedback-pipeline/README.md)

**Days 87–88 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** Handlers edit Harbor drafts, discard them, and occasionally tell the Columbus manager that a citation was wrong. Those acts are feedback. Someone will propose to "just train on the edits." The edits sit in Lumen notes and in Harbor logs that, by your tracking plan, do not contain note text. A pipeline that turns feedback into an evaluation item or a training row has to cross that boundary on purpose, with a reason, a consent or employment basis you do not invent, and a place where bad rows are rejected.

#### Concept

A feedback pipeline brief describes the path from a human act to a reviewed dataset: which acts are eligible, what is stripped, who reviews, what the dataset is allowed to be used for, and which uses are forbidden until a named approval exists. It is a product and data-rights document with a flow a data partner could implement. It is not the implementation. The point is to make the forbidden shortcut visible. The shortcut here is copying committed notes into a fine-tuning file because they are "high quality by definition." A committed note can contain a wrong limit the handler trusted. Commitment is not a label.

#### Approach

Define three eligible acts and one ineligible act.

Eligible:

- **Citation defect report.** A handler or supervisor flags a citation. The row may contain the citation id, the notice id, the expected id if the supervisor knows it, and a reason. It may not contain the claimant's loss narrative.
- **Discard after a shown draft.** Eligible as a negative signal that the draft was not wanted. It is not eligible as a label of why, unless the handler picks a reason from a short list (`wrong source`, `too slow`, `easier to type`, `out of job`). Free-text reasons are out until legal reviews the field, because handlers will paste claim facts into a free-text box.
- **Structured edit distance bucket.** You already log `edit_size` as coarse. That bucket may be used as an eval slice. The edited text itself may not enter a training set in this pilot.

Ineligible:

- **Committed note body as a positive training example.** Forbidden in the pilot. The brief says what would have to be true to reopen it: a reviewed sample, a labeling pass against the guideline, a data-rights row closed in writing, and a use limited to evaluation before any training use is even discussed.

Write the path for an eligible citation-defect report:

1. Capture. The flag action on the citation panel, with the fields above.
2. Strip. Drop free text that is not on the allow-list. Log that stripping happened, not the dropped text.
3. Route. Content analyst queue, not an automatic set update.
4. Review. Analyst marks `accept as golden candidate`, `reject`, or `incident`. Accept does not edit the golden set by itself. It opens a charter change, with a new id, under the set owner.
5. Store. A reviewed-candidate table, versioned, separate from the gating set and separate from any training bucket.
6. Use. Evaluation candidates only. A training-use flag exists on the row and defaults to `no`. Changing it to `yes` is a principle-level decision, not a pipeline setting.

Write retention. Candidate rows live for the pilot plus a stated period you choose and can defend (for example, one quarter after the pilot decision), then expire unless they were promoted into a versioned set. Promoted rows follow the set's charter, not the feedback retention clock.

Write the failure of the pipeline itself. Duplicate flags on the same citation must not become two golden rows. A flag from a usability-test session must not enter the pilot queue. The wizard-week stream and the production stream stay apart, which the tracking plan already required; the pipeline brief repeats it because pipelines are where that promise usually dies.

#### Components

- **Act inventory.** Eligible and ineligible, with the reopen conditions for the ineligible act.
- **Stage flow.** Capture, strip, route, review, store, use. A diagram in mermaid or a numbered list.
- **Field allow-list.** What a candidate row may contain.
- **Promotion rule.** How a candidate becomes a golden-set proposal without bypassing the charter.
- **Retention and separation.** Clocks, and the ban on mixing wizard-week with production.

#### Flow

1. List the human acts that already exist in the product before you invent a new "thumbs" button. Add a control only if an eligible act cannot be captured otherwise. The citation flag may be new; justify it.
2. Write the ineligible act and its reopen gate first, so the rest of the brief cannot quietly route around it.
3. Specify stages and the field allow-list. If a stage has no owner, it is not a stage.
4. Write retention and the duplicate rule.
5. On day 88, walk one fictional flag through every stage and write the row as it appears after stripping. Then try to walk a committed note body through the same stages and show the stage that stops it. If no stage stops it, add the stop.

#### Tools and stack

Markdown and a simple flow diagram. No pipeline framework, no label studio, and no training job. A data partner should be able to estimate the work from the brief. A model trainer should be able to see that there is nothing for them to train on yet, and why.

#### Setup

1. Create `harbor-portfolio/87-feedback-pipeline/brief.md`.
2. Draw the six stages before writing prose, and keep the ineligible act on the same page.
3. Day 87 is acts, fields, and stages. Day 88 is retention, the two walkthroughs, and any stop you had to add.

#### Deliverables

- A pipeline brief with eligible and ineligible acts.
- A stage flow, a field allow-list, and a promotion rule into the charter.
- Two walkthroughs: one flag that survives as a candidate, one note body that is stopped, with the stopping stage named.

#### What done looks like

A committed note cannot become a training row by configuration. A citation flag can become a golden-set proposal only through a human and a new id. Free text of the loss is not on the allow-list. Wizard-week events are excluded. Retention has a clock. The reopen conditions for training use are stricter than "the model team is ready."

#### Think a step ahead

Edits that are too sensitive to store may still be useful as preference pairs: the draft versus the handler's revision, with claim facts removed. That use is more dangerous than a citation flag, not less, because the revision is the note. Add a blocked design, written so a future team cannot claim you never considered it. Describe the pair, the minimum redaction (loss narrative, names, policy numbers, vehicle identifiers), the residual risk that a rare fact pattern still identifies a claimant, and the decision: not in this pilot, reopen only with counsel and a redaction review on a sample. The follow-on names the temptation precisely enough that "anonymous edits" cannot sneak through as a synonym.

#### Interview angle

Name the stage that stops a committed note from becoming training data, and the reopen conditions. The pipeline is the refusal as much as the flow.

### Days 89–90 — Analytics Trust Runbook

Working copy and fixtures: [phase-09-pipelines/day-89-90-analytics-trust/README.md](phase-09-pipelines/day-89-90-analytics-trust/README.md)

**Days 89–90 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** Harbor's Monday packet depends on events: drafts shown, citations opened, notes committed, audit results joined later. The Columbus office also runs a small robotic process that re-saves notes in Lumen after a supervisor stamp. Nobody told the product team. In week 4 the "committed with draft" count jumped, and the north-star conversation almost happened on a lie. This project writes the runbook a PM and an analytics partner use when a number moves for a pipeline reason, and the checks that would have caught this jump before the meeting.

#### Concept

An analytics trust runbook is the incident process for decision metrics. It assumes the definition in the metric tree is right and the figure on the page is still wrong, because the events were duplicated, dropped, late, mis-joined, or produced by a bot. The runbook tells the on-call pair how to decide, within a business day, whether Monday's packet is usable. It is about the behavioral-event path and the audit-file join. It is not a general data-contract platform and not a customer-evidence integrity product. Those solve neighboring problems for other systems.

#### Approach

Write four failure modes that fit Harbor, each as a play: how you notice, how you confirm, what you do to the packet that day, and what you fix afterward.

1. **Duplicate commit events.** The robotic stamp re-saves the note and your `note_committed` fires again. Symptom: commits per notice above 1 for a slice of handlers, activation and used-draft rates move together. Confirm: distribution of events per notice id, and a comparison against Lumen's own note-count for the same ids. Packet action: suppress the metric and mark the week confounded for a pipeline reason, which is a different mark from a product confounder. Fix: idempotency key on notice id plus commit generation, and a bot identity that is excluded.
2. **Missing client version.** A new build stops sending `citation_opened` and sends everything else. Symptom: citation-open rate falls off a cliff for one build id only. Confirm: rates by build id. Packet action: do not coach handlers on "they stopped reading citations." Fix: a build cannot be marked current in the ritual if a required event is absent for that build.
3. **Late audit file.** Already specified as a degraded dashboard state. The runbook's job is the clock: if the file is late past the packet deadline, the packet ships in the degraded state and does not wait until mid-meeting. Write the deadline.
4. **Identity join.** Handler ids in Harbor and employee ids in the audit file differ by a prefix. Symptom: the guardrail's denominator collapses. Confirm: unmatched-id count. Packet action: guardrail is "not reported," not zero defects. A join failure that reports zero is how a broken pipeline clears a veto.

Add a standing check list, run on Friday or whenever the packet is assembled, with pass/fail and no prose:

- Commits per notice, p95, under a threshold you set (start at 1, and justify if you allow supervisor-driven recommit).
- Share of draft_shown without a matching draft_requested, near zero.
- Required events present for the build id the ritual will discuss.
- Unmatched handler ids, zero, or the guardrail is withheld.
- Bot or service identities excluded, with the exclusion list's owner.

Write the communication rule. A pipeline defect uses a one-line status on the packet ("metrics withheld: duplicate commits under investigation"), not the incident addendum reserved for a bad citation in a file. Mixing them trains everyone to ignore both. Name who may put that line on the packet (product or the analytics partner) and who must hear it before the meeting (the Columbus manager, so she does not prepare a coaching speech on a fake drop).

#### Components

- **Four plays.** Notice, confirm, packet action, fix.
- **Friday checklist.** Pass/fail, thresholds, owner of each check.
- **Status line.** The words used when metrics are withheld, and the channel that is deliberately not used.
- **Bot register.** A table the Columbus manager can add to when a new automation appears. The robotic stamp is row one, marked as discovered late, with the date of discovery written as a lesson.
- **Reconstruction limit.** What you will not do: silently restate last week's packet after you "fix" history. If history is restated, the next packet says the restatement happened and which weeks changed.

#### Flow

1. Write the duplicate-commit play first, from the scenario, before generalizing.
2. Add the other three plays. Each needs a confirm step that a person can do without a new tool, even if the confirm is "count unmatched ids in the join output."
3. Turn the confirms into the Friday checklist with thresholds.
4. Write the status line and the reconstruction limit.
5. On day 90, tabletop the robotic-stamp failure with a partner playing the VP who wants the number anyway. The runbook should give you a sentence and a fallback figure (Lumen's own count, labeled as a different metric) or a clean withhold. If the tabletop ends with you reading the broken number "with a caveat," the runbook failed and you tighten the packet action.

#### Tools and stack

Markdown. A spreadsheet mock of the checklist is optional. No warehouse project. The runbook should be usable by two people who can see event counts and the audit file, which is the actual staffing of a forty-person pilot.

#### Setup

1. Create `harbor-portfolio/89-analytics-trust/runbook.md`.
2. Put the status-line wording at the top so the plays cannot invent softer language later.
3. Day 89 is the four plays and the bot register. Day 90 is the checklist, the reconstruction limit, and the tabletop.

#### Deliverables

- Four failure plays with packet actions.
- A Friday checklist with thresholds.
- A status line, a bot register with the stamp as row one, and a tabletop note.

#### What done looks like

A duplicate-commit week cannot become a north-star conversation. A join failure cannot report zero defects. The checklist has owners and pass/fail. The VP tabletop produced a withhold or a clearly labeled fallback, and the wording is in the runbook. Pipeline bad news does not use the citation-incident template.

#### Think a step ahead

The robotic stamp is one automation. The next one will be a handler-side macro that opens every citation in the background to satisfy the "citation opened" metric once people learn it is watched. Extend the bot register into a behavior register: events whose timestamps are too regular, or whose time-to-open is below a floor you set, are quarantined from the citation metric and reviewed as possible gaming. Write the floor as a hypothesis, the quarantine rule, and the conversation owner (the Columbus manager, not an automated accusation in the packet). The follow-on treats gaming as a pipeline-trust problem, because a gamed event is not a human act even when a human installed the macro.

#### Interview angle

Tell the robotic-stamp story through the packet action. Then the reason a join failure must not look like a perfect guardrail. Trust work is the number you refused to show.

### Days 91–92 — Knowledge Publishing Pipeline

Working copy and fixtures: [phase-09-pipelines/day-91-92-knowledge-pipeline/README.md](phase-09-pipelines/day-91-92-knowledge-pipeline/README.md)

**Days 91–92 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** Harbor may cite a document only after it is published into the pilot corpus by a named content owner. The owner's real work is a pipeline, whether or not anyone has drawn it: a form or bulletin arrives, someone checks the edition and the amend relationship, it becomes retrievable, and, when it is wrong or withdrawn, it stops being retrievable. The pilot's freshness promise and the `bulletin_missing` reason code are both promises about this pipeline. This project writes the pipeline as an operating design: stages, roles, clocks, and the emergency stop.

#### Concept

A knowledge publishing pipeline is the system of record for what the assistant is allowed to say. Retrieval quality cannot exceed it. The design names the stages from "received" to "retrievable" to "withdrawn," the human checks at each stage, the maximum time a known bulletin may sit unpublished before Harbor must show `bulletin_missing`, and the path that pulls a bad document out faster than the ordinary cadence. It is a product operations spec. It does not select a CMS, a crawler, or an embedding job. Those are implementations that have to honor the clocks.

#### Approach

Define stages a document instance moves through. An instance is a specific file plus its metadata, not "the rental bulletin" as an idea.

1. **Received.** The email or the file is in the intake folder. It is not citable. Harbor does not see intake.
2. **Classified.** A content analyst marks class (`form`, `bulletin`, and `circular` only if you decided circulars were in scope), line, state, edition id, and, for a bulletin, the edition it amends. A second person checks the amend link for the pilot, as the corpus policy required. Until the check happens, the instance is not classified.
3. **Structured.** The fields the citation schema needs are present, including the locator. A PDF that cannot supply a locator does not pass this stage. It stays uncited, and the handler-facing state is the missing-source state, not a title with no page.
4. **Published.** The instance is in the retrievable corpus, with a publish timestamp. This timestamp is what the freshness promise measures against the source's own issue time.
5. **Withdrawn.** The instance is not retrievable. Withdrawal records a reason, a person, and a time. A withdrawn id fails closed: retrieval must not return it even if an older index still has the vector. Write that as a requirement on the pipeline's output, not as an implementation hint about indexes. The acceptance condition is "a withdrawn id returns zero passages," which you can put in the golden set.

Write clocks.

- Ordinary bulletin: published or explicitly marked `bulletin_missing` within one business day of receipt during the pilot. You may choose a different number; defend it against the Monday packet, where a Friday bulletin that is invisible until Tuesday is a known hole.
- Emergency withdrawal: a document the content owner believes is wrong is withdrawn within two hours of the decision during business hours, and the next-morning rule from the quality ritual applies if the decision is after hours. Write who can make the decision (content owner, with product informed immediately, not waiting for the weekly ritual).

Write the correction surface for a note already committed against a document you later withdraw. The pipeline cannot edit Lumen. The spec says the content owner produces a list of notice ids that cited the withdrawn id, product gives that list to the Columbus manager, and the manager owns the file correction. This is the operational action from the postmortem, generalized.

Write intake exclusions. Handler desktops, the open web, and another line's folder dropped into intake "so search is better" do not enter Received. They are refused at the door, with a reply the content owner can send without a meeting.

#### Components

- **Stage definitions.** Entry condition, exit condition, who acts, what Harbor is allowed to do while the instance is in that stage.
- **Clocks.** Ordinary publish, emergency withdrawal, after-hours rule.
- **Fail-closed rule.** Withdrawn means not retrievable, with a golden-set consequence.
- **Correction handoff.** From withdrawn id to a list of affected notices to a named office owner.
- **Intake refusal.** The reply text for an out-of-scope drop.

#### Flow

1. Write stages from the handler's point of view: at which stage could a citation first appear? The answer should be Published, only.
2. Add the second-person check on amend links. If the pilot cannot staff it, the stage does not silently drop the check; the corpus scope shrinks until the check is real. Choose and write it down.
3. Set clocks and the after-hours rule.
4. Write the correction handoff and the intake refusal.
5. On day 92, simulate a wrong rental number discovered at 4:30 p.m. Walk the clock minute by minute and name the person acting at each step. If the simulation reaches "someone should probably unpublish it tomorrow," the design is not done.

#### Tools and stack

Markdown, plus a stage table a content owner could pin. No CMS build and no crawler. If the company later uses a document platform, the stages and clocks are the acceptance criteria for how it is configured.

#### Setup

1. Create `harbor-portfolio/91-knowledge-pipeline/pipeline.md`.
2. Start from "Harbor cannot see this stage" as a column in the table, so visibility is a decision per stage.
3. Day 91 is stages and clocks. Day 92 is fail-closed behavior, the correction handoff, the refusal text, and the 4:30 p.m. simulation.

#### Deliverables

- A stage model with owners and Harbor visibility.
- Clocks for ordinary publish and emergency withdrawal.
- A fail-closed rule, a correction handoff, an intake refusal, and the simulation note.

#### What done looks like

A document in intake cannot be cited. Withdrawal has a person and a two-hour clock, and the 4:30 p.m. simulation names the after-hours behavior instead of hoping. Affected committed notes have a path to a human correction. Out-of-scope drops have a refusal text. The golden set is named as the place a withdrawn id must return nothing.

#### Think a step ahead

Withdrawal during the day does not repair a draft already on a handler's screen, rendered at 3:00 p.m. from a corpus that was valid at 3:00 p.m. Specify a screen contract: each draft carries the corpus publish timestamp it was built from, the client re-checks that timestamp at commit, and a commit against a since-withdrawn id is refused with copy that tells the handler the source was withdrawn and the note must be written in Lumen. Write the copy and the log event. The follow-on closes the gap between the pipeline's clock and the draft sitting open on the floor, which is the gap handlers will actually hit.

#### Interview angle

Walk the 4:30 p.m. withdrawal through the clock and the commit-time re-check. Publishing is a safety system with hours, not a content calendar.

### Days 93–94 — Training-Data Lineage and Deletion

Working copy and fixtures: [phase-09-pipelines/day-93-94-training-lineage/README.md](phase-09-pipelines/day-93-94-training-lineage/README.md)

**Days 93–94 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** The feedback pipeline forbids training on Harbor notes during the pilot. A future quarter may reopen that decision for a narrow evaluation set, and a vendor or an internal team may already be talking about a fine-tune. Separately, Northline can receive a deletion or retention demand for a claimant's information. If any claim fact has entered a dataset, someone will ask whether the model still "has" it. This project writes the lineage and deletion brief so that question has an answer other than a shrug. It does not build a training run, and it does not audit a synthetic dataset. The asset is the record of what a row is, where it went, and what you do when it must die.

#### Concept

Lineage is the chain from a source event to a dataset version to a model version that consumed it. Deletion is the product and legal behavior when a link in that chain must be removed or when removal is no longer possible. A brief that says "we honor deletion requests" without saying what happens to a fine-tune that already consumed the row is a slogan. You will write the fields every training-candidate row must carry, the uses those fields permit, and the decision tree when a row is already baked into a model.

#### Approach

Specify the minimum lineage record for any row that might leave the reviewed-candidate table, even for an offline eval export:

- source act and source id (the citation flag, not a vague "user feedback"),
- notice id and the retention class of the notice,
- what was stripped, as a list of field classes removed, not the removed content,
- dataset name and version the row was exported into, if any,
- purpose flag: `eval` or `train`, default `eval`,
- model version that consumed it, empty until true,
- legal basis note: a pointer to the closed RAID row that allowed the export, empty if none, and an export with an empty basis is forbidden,
- deletion status: `active`, `suppressed`, `exported-then-suppressed`.

Purpose and basis are product controls. An engineer does not flip `train` because a notebook is convenient. The brief names the decision forum (the same escalation path as a principle change) and the default (export refused).

Write the deletion tree.

1. **Row only in the candidate table, never exported.** Suppress the row, keep a tombstone with no claim content, so you can prove the suppression. Harbor behavior is unchanged.
2. **Exported to an eval set, not consumed by a training run.** Remove the row in the next set version, retire the id under the charter, and mark prior reports that included it as "set version superseded" if the row could have changed a gate. For Harbor's citation ids this will be rare; the rule still exists.
3. **Consumed by a model version.** You cannot promise the row is gone from the weights. The decision, made with counsel, is one of: stop using that model version for Harbor and return to the prior version or to no-model; or keep the version under a written residual-risk acceptance that names the model version, the data class, and the review date. There is no third option called "approximately deleted." Write that sentence in the brief.

State the pilot default, given training is forbidden: any deletion demand is case 1, and the brief's job is to keep the pilot from accidentally creating case 3. The control is the empty legal-basis field blocking export, plus a quarterly confirmation from the model owner that no Harbor row was in a training file. The confirmation is a ritual, not a tool. Name the owner.

Write what the handler-facing product does during a deletion. Nothing visible, unless the deletion withdraws a source document, which is the knowledge pipeline's job, not this one. Say that explicitly so the two pipelines are not mashed into one project.

#### Components

- **Lineage fields.** The list above, with who is allowed to set each field.
- **Export gate.** Empty basis or `train` without a forum decision blocks the export. Write it as an acceptance condition.
- **Deletion tree.** Three cases, the tombstone rule, and the banned phrase "approximately deleted."
- **Pilot default and quarterly confirmation.** Who signs, what they sign, where it is kept.
- **Boundary with the knowledge pipeline.** Deleting a training row is not withdrawing a form. Withdrawing a form is not a deletion of a claimant's note.

#### Flow

1. Draft the fields from a row's life, from flag to export to hypothetical training. Cut any field you cannot imagine a person filling. A lineage record nobody fills is fiction.
2. Write the export gate as a block, not a warning.
3. Write the deletion tree, case 3 last, with counsel in the decision.
4. Set the pilot default and the quarterly confirmation.
5. On day 94, run a tabletop: a claimant deletion arrives, and an engineer admits a notebook export happened last month with no basis field set. Apply the tree. The honest case may be "we must treat it as case 3 because we cannot prove it was not consumed." Write that outcome and the control that should have made the export impossible. If the tabletop is comfortable, you have not made the export gate concrete enough.

#### Tools and stack

Markdown. The feedback-pipeline brief and the RAID log as inputs. No training stack, no feature store, and no synthetic-data generator. The quarterly confirmation can be a checklist in the same file.

#### Setup

1. Create `harbor-portfolio/93-lineage/brief.md`.
2. Write "approximately deleted is not a status" at the top and keep it in the final deletion section.
3. Day 93 is fields and the export gate. Day 94 is the deletion tree, the confirmation, and the tabletop.

#### Deliverables

- A lineage field list and an export gate.
- A three-case deletion tree with a tombstone rule.
- A pilot default, a quarterly confirmation, and a tabletop note that includes an untracked export.

#### What done looks like

A row cannot be exported for training by changing a config in silence. Case 3 names a real choice: stop using the model version, or accept residual risk in writing with counsel. The pilot default is that training rows do not exist, and the confirmation exists so the default stays true. The knowledge pipeline is a different path, and the brief says so. The tabletop ended in a specific case, not in a promise to do better.

#### Think a step ahead

A vendor fine-tune may keep training artifacts the quarterly confirmation cannot see, because the confirmation is about Northline's files. Add a vendor clause to the RAID log's training row: the vendor certifies that prompts and exports from the pilot tenant were not used to train a model shared with other customers, names the model versions that statement covers, and notifies Northline before a version trained on any Northline content is served back to Harbor. Write the product behavior if the certification is missing or late: Harbor stays on the rule layer and retrieval citations with no vendor prose, which is a fallback you have already specified elsewhere. The follow-on ties lineage to the vendor boundary, where a local tombstone does not reach.

#### Interview angle

Explain case 3 in plain language, including the option to stop using the model version. Then the export gate that keeps the pilot out of case 3. Lineage is a decision tree, not a metadata hobby.

## Phase 10 — Advanced Bets

**Days 95–100 · Advanced · 3 projects**

### Goals

This phase spends the judgment on purpose. You choose whether the next quarter deepens the Columbus feature, builds a platform for a second tenant, or sequences the two, and you write the kill criterion that can fire. You package the internal cost as capacity with an overage behavior that matches the pause rules, and you refuse an outcome price you cannot adjudicate. You compress the stack into a narrative a hiring manager can retell and a 30-60-90 that installs a fence, a gate, and a ritual on a team that already has tools. The phase is done when the narrative claims decisions and refusals, and does not claim a measured improvement from a fictional office.

### Skills covered

Advanced product management: platform-versus-feature bets, pricing and packaging, portfolio narrative and a first-ninety-days operating plan.

### Days 95–96 — Platform versus Feature Bet

Working copy and fixtures: [phase-10-advanced-bets/day-95-96-platform-bet/README.md](phase-10-advanced-bets/day-95-96-platform-bet/README.md)

**Days 95–96 · Phase 10, Advanced Bets · Advanced**

**Case.** Harbor works, narrowly, for Ohio personal-auto notices in Columbus. Two proposals arrive the same week. Proposal F: deepen the feature — glass-only handling, the partial-support flow, the commit-time corpus check — for this office, through the end of the quarter. Proposal P: extract a "Northline knowledge platform" so any team can register a corpus and get drafts with citations, starting with homeowners in another state. The platform proposal has a senior sponsor. The feature proposal has the Columbus manager. You have to write the bet, not split the difference in a way that funds neither.

#### Concept

A platform-versus-feature bet is a decision record about where reuse is real and where reuse is a way to avoid finishing the job. Shared retrieval, a citation schema, and an eval harness can be platforms. "The Harbor model" cannot, because the model card, the corpus policy, and the principles are use-specific. This project writes the options, the kill criteria, the sequencing, and the chargeback question the platform will face the moment a second team wants it to be free.

#### Approach

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

#### Components

- **Option briefs.** F, P, and D, each half a page, with the hours and the guardrail risk.
- **Kill criteria.** One per option, observable.
- **Unchanged-parts list.** Adopt unchanged versus must rewrite, drawn from real artifacts in this playbook.
- **Chargeback rule.** What a second tenant must bring, and the request you will refuse (a model, no corpus owner).
- **Recommendation.** One option, the date you will review the kill criterion, and the sponsor sentence.

#### Flow

1. Write the unchanged-parts list before the recommendation. It is the evidence, and writing the recommendation first will bias the list.
2. Draft the three options at the same length. A straw man is a way of not deciding.
3. Write kill criteria that could actually fire this quarter.
4. Choose. The sponsor sentence is what you will say to the senior sponsor if you did not choose their option, and it has to contain the kill criterion.
5. On day 96, ask a partner to argue for the option you rejected. If their best point is absent from your brief, add it, and see whether the recommendation still stands. Record the point either way.

#### Tools and stack

Markdown. The model card, principles, corpus policy, and harness brief as the evidence for what is reusable. No architecture tooling. A platform bet at this stage is a scope decision. A system diagram can come after the option is chosen, and it is out of scope here.

#### Setup

1. Create `harbor-portfolio/95-platform-bet/bet.md`.
2. Build the unchanged-parts list from documents you actually wrote, cited by name.
3. Day 95 is the list and the three options. Day 96 is kill criteria, chargeback, the recommendation, and the partner argument.

#### Deliverables

- Three option briefs at comparable depth.
- An unchanged-parts list tied to real artifacts.
- A recommendation, kill criteria, a chargeback rule, and a note from the partner argument.

#### What done looks like

The recommendation names what will not be built this quarter. The second tenant cannot arrive with only a request for "the Harbor model." Kill criteria are observable. The sponsor sentence contains the criterion, not a compliment. The unchanged-parts list is longer on the rewrite side if that is the truth, and you did not hide that to make a platform sound bigger.

#### Think a step ahead

If option D or P survives, the second tenant's failure mode is using Harbor's screen for a different decision, such as a claimant-visible homeowners answer, while the registry still says "citation platform." Extend the chargeback rule with a use-review: every tenant's intended reader and author of record are re-certified when their traffic or their disclosure changes, and a tenant who cannot pass the re-certification loses retrieval access until they do. Write the trigger and the access consequence. The follow-on is how a platform stays narrow after it has customers, which is the problem a launch bet never feels yet.

#### Interview angle

Give the recommendation and the kill criterion in the same breath. Then one asset a second team must rewrite. That is the bet.

### Days 97–98 — Pricing and Packaging

Working copy and fixtures: [phase-10-advanced-bets/day-97-98-pricing-packaging/README.md](phase-10-advanced-bets/day-97-98-pricing-packaging/README.md)

**Days 97–98 · Phase 10, Advanced Bets · Advanced**

**Case.** Northline is not selling Harbor. The pricing question is internal, and it is still real: claims operations will be charged, in budget and in attention, for a capability that consumes model spend, content-analyst time, and supervisor time. A later world, which you will treat as a clearly labeled hypothetical, is an insurer offering a similar assistant to independent adjusting firms. The packaging decisions are different in the two worlds, and this project keeps them from sharing a slide.

#### Concept

Packaging is what a buyer gets, what they do not get, and what happens when they exceed the bundle. Pricing is how that bundle is paid for. For an AI note assistant the dangerous packages are the ones that meter the wrong unit. Per draft rewards short, reckless generation if someone games it, and punishes the careful discard. Per seat hides the tail of long claims. Per "successful note" sounds aligned and becomes a dispute the moment success is undefined. You will design the internal package for the pilot's next quarter, and you will write the hypothetical external package only far enough to show which extra machinery it requires.

#### Approach

**Internal package, next quarter, Columbus and any expansion that has passed a gate.**

Write a one-page package:

- Included: rule-layer edition selection, retrieval over the published corpus for one line and one state, drafts where the answer experience allows them, the quality ritual, and the content pipeline's ordinary clock.
- Not included: other lines, claimant-facing text, training on notes, a dedicated model, weekend publish clocks beyond the after-hours rule you already wrote.
- Unit: a quarterly capacity bundle of indexed documents and analyst hours, plus a model-spend ceiling taken from the unit-economics sheet. Seats are not the meter. Handlers fluctuate with storm weeks; documents and hours are the scarce things.
- Overage: when the spend ceiling is crossed, prose drafts pause and citations remain, unless citations are the part that is failing. This matches the pause mechanics. Overage is a product behavior, not only a finance email.
- Who signs: claims operations signs the ceiling, product signs the inclusion list, content operations signs the document and hour numbers they can actually staff.

**Hypothetical external package, labeled hypothetical.** Independent adjusting firms. You do not have willingness-to-pay evidence, and you will not invent a price point as if you did. You will write the questions and the structural choice:

- Seat versus usage versus outcome. Argue from Harbor's failure modes. Outcome pricing ("per correct note") requires a definition of correct that the buyer and you share, a dispute path, and a refund or credit rule. The citation defect is the natural dispute, and the auditor would have to be named. If you cannot name the auditor, you cannot honestly offer outcome pricing. Say so, and recommend a structure you can operate: a platform fee for the corpus tools plus a usage band with a ceiling, and no outcome fee in the first external version.
- The dispute you would otherwise face: the customer's handler accepted the draft, the carrier later denied the claim, and the customer wants the outcome fee back. Write why "accepted" is not "correct," using the authorship clause. Acceptance is a human commit, not a warranty of coverage.
- What must already exist internally before external pricing is even a proposal: the deletion tree, the tenant isolation requirement from the postmortem follow-on, and a model card per jurisdiction. List them as gates, not as a roadmap romance.

Connect the internal ceiling to the unit-economics driver that flipped the recommendation. If that driver was minutes returned, the package does not pretend to charge the handler for time saved. Claims operations captures the time, if it is real, in their own staffing. Harbor's package charges for the capacity to run the assistant safely. Those are different ledgers. Write that in two sentences so a finance partner does not merge them.

#### Components

- **Internal one-pager.** Included, excluded, unit, overage behavior, signers.
- **Ledger note.** Capacity cost versus time-saved benefit, kept apart.
- **External sketch.** Labeled hypothetical, structural recommendation, the dispute you will not take, the gates required first.
- **Question list.** What you would need to learn before any external price point exists. At least five questions, none of them answered with fake numbers.
- **Abuse note.** How the internal ceiling could be gamed (splitting documents to stay under a count, or pushing spend into a neighboring cost center) and the single control you would add.

#### Flow

1. Write the internal inclusion list from the interaction contract's prohibitions. Exclusions come from there, not from a packaging brainstorm.
2. Set the unit and the overage behavior so they match the quality ritual's pause. If they diverge, one of the documents is wrong; fix the package or record a change to the ritual.
3. Write the ledger note.
4. Write the external sketch as a set of gates and a refused dispute. Do not pick a dollar price.
5. On day 98, read the one-pager to a partner playing finance and a partner playing the Columbus manager. Finance will ask for a per-claim charge. The manager will ask for unlimited drafts in storm week. Your answers should already be the overage behavior and the ledger note. Add whatever question you could not answer.

#### Tools and stack

Markdown. The unit-economics memo and the quality ritual as sources. No pricing software and no market model. A spreadsheet is appropriate only to restate the ceiling you already computed, with the assumptions visible.

#### Setup

1. Create `harbor-portfolio/97-pricing/package.md`.
2. Mark the external half with a visible "hypothetical" banner at the top of that section.
3. Day 97 is the internal one-pager and the ledger note. Day 98 is the external sketch, the abuse note, and the two-role read.

#### Deliverables

- An internal package one-pager with an overage behavior that matches the pause rules.
- A ledger note separating capacity cost from time saved.
- A hypothetical external sketch with no invented price, a refused dispute, and entry gates.

#### What done looks like

A finance partner can see the ceiling and the behavior when it is crossed. A claims manager can see storm week is a capacity conversation, not a silent overage bill. Outcome pricing is refused for a named reason, not deferred with a wink. No dollar price is presented as research. The external section cannot be forwarded as a quote sheet; the banner and the missing price make that hard.

#### Think a step ahead

If a later version does offer an outcome fee, the dispute machinery is the product. Sketch it one level deeper than the refusal: who may open a dispute, the only eligible grounds (a cited source that did not support a number in the committed note, as judged by the labeling guideline), the ineligible grounds (the claim was denied, the handler was slow, the customer dislikes the prose), the evidence each side must attach (citation id, committed text hash, corpus version), and the remedy (a credit against the usage band, not a statement about coverage). Label the sketch as not offered. The follow-on makes the refusal specific, so a future team cannot "add outcome pricing" by changing a rate card and skipping the adjudicator.

#### Interview angle

Explain the internal unit and why it is not seats or drafts. Then why an accepted note is not an outcome you would sell. Packaging is the unit and the dispute you refuse.

### Days 99–100 — Capstone: Portfolio Narrative and the First 90 Days

Working copy and fixtures: [phase-10-advanced-bets/day-99-100-capstone/README.md](phase-10-advanced-bets/day-99-100-capstone/README.md)

**Days 99–100 · Phase 10, Advanced Bets · Advanced**

**Case.** You have a stack of Harbor artifacts: a fenced opportunity, a contract, a metric tree, a gate map, a retrieval policy, an eval strategy, a pipeline brief, and a bet. A hiring manager, or Northline's VP, will not read the stack. They will read a narrative and a plan for what you would do in a new seat. This project assembles the narrative from the artifacts and writes a 30-60-90 for a team that already owns tools and does not need you to rebuild them.

#### Concept

A portfolio narrative is the argument that you can carry a product from a painful job to a gated pilot, told through decisions and the evidence that would change them. A 30-60-90 is the same judgment applied to a team you just joined: what you would learn, what you would not replace, and what you would ask the team to start doing on a cadence. The capstone is those two documents. It is not a new feature and not a redesign of Harbor.

#### Approach

Write the narrative in six beats. Each beat cites an artifact by name and states the decision, the alternative you rejected, and the result you will not claim because the work was a practice case.

1. **Problem and fence.** The opportunity brief. You rejected an unbounded claims assistant. You will not claim handle-time savings you did not measure.
2. **Responsibility.** The interaction contract and the principles. The handler is the author. You rejected coverage decisions and claimant messaging, including when a senior stakeholder asks.
3. **Evidence.** The metric tree, the experiment story or the ship note, and one number you refused to repeat. Show the refusal.
4. **System shape.** The approach decision's boundary between the rule layer and the drafting model, plus one retrieval reason code. You rejected "the model will pick the form."
5. **Operations.** One pipeline (knowledge publishing or feedback) and the quality ritual's pause. You rejected a launch that nobody can stop on a Thursday.
6. **Bet.** The platform recommendation and its kill criterion.

Keep the narrative under 1,200 words. Link or name the underlying files. A narrative that restates every rubric anchor has become a dump.

Then write a 30-60-90 for a specific seat you imagine taking: product manager on an existing AI feature inside a claims, support, or operations team that already has a tracker, a dashboard, and a model in production. The seat is not "build Harbor at a new company." Assume the feature is live and the artifacts are missing.

- **Days 1–30, learn and fence.** Read the current intended use, write the prohibitions if they are unstated, sit with two practitioners, and find the metric the team celebrates that your refusal list would ban. Deliverable: a one-page fence and a banned-metric note. You do not propose a rebuild.
- **Days 31–60, evidence and gates.** Install one gate that the team can fail: a small golden set or a contract probe, owned by a named person, bound to a release. Deliverable: the charter section and the ship-note shape. You adopt their runner if it can meet the harness brief's acceptance tests, and you write the gap if it cannot. You do not commission a new platform.
- **Days 61–90, cadence.** Start the quality ritual at a size their staffing can hold, and bring one pipeline failure mode (duplicate events or an unowned corpus) into a runbook. Deliverable: one packet and one play. At day 90 you recommend continue, restrict, or pause on their feature, using their numbers, or you say the numbers do not exist yet and the recommendation waits.

The 30-60-90 has a "will not do" line in each phase. Likely entries: will not replace the tracker, will not introduce a blended quality score, will not promise a fine-tune, will not expand the feature to a new country in the first quarter.

Close with a personal learning note, half a page: which Harbor artifact you would redo first if a real claims trainer sat down with you, and what question you would ask them. This note keeps the capstone from reading like the work was real-world proof. It was a disciplined practice. Say so once, plainly, and then let the decisions stand.

#### Components

- **Narrative.** Six beats, under 1,200 words, each with a rejected alternative and a non-claim.
- **Artifact index.** The files a reader should open next, in the order of the beats, one line each on why.
- **30-60-90.** Three phases, deliverable, will-not-do, and the day-90 recommendation rule.
- **Learning note.** What you would redo, and the question for a real practitioner.

#### Flow

1. List the six decisions before you write prose. If you cannot name the rejected alternative, you do not yet have the beat.
2. Draft the narrative inside the word limit. Cut background that the case paragraph already provides.
3. Write the 30-60-90 against a live-feature assumption. Delete any week whose main activity is "familiarize myself with the codebase" unless it produces the fence document.
4. Write the will-not-do lines last, when you can see what you were tempted to stuff into the quarter.
5. On day 100, read the narrative aloud once. Anywhere you claim a measured improvement in a real office, strike it. The fixtures were fixtures. The judgment is what you are allowed to claim.

#### Tools and stack

Markdown and the portfolio folder you have been keeping. No slide tool is required. If you later make three slides, they are a view on this narrative, and the narrative remains the source. Do not start in slides or the refusals will not fit.

#### Setup

1. Create `harbor-portfolio/99-capstone/narrative.md` and `first-90-days.md`.
2. Put the word count target at the top of the narrative and check it at the end.
3. Day 99 is the six beats and the index. Day 100 is the 30-60-90, the learning note, and the aloud pass.

#### Deliverables

- A narrative under 1,200 words with six decisions and six non-claims.
- An artifact index.
- A 30-60-90 with will-not-do lines and a learning note.

#### What done looks like

A hiring manager can retell the fence, the authorship rule, and one refused metric after one reading. The 30-60-90 produces three artifacts a real team could use, and it refuses a rebuild. The learning note admits the work was practice and asks a question only a practitioner can answer. No sentence claims Northline's handle time fell.

#### Think a step ahead

The first ninety days install a cadence. The following quarter is where the cadence becomes theater: packets filed, probes skipped, the ritual still marked "continue" out of politeness. Write a day-120 check you would put on your own calendar. Inputs: whether the golden set changed under the charter, whether any ship note cited a real report, whether any week was marked confounded, and whether a pause or a restriction has been operationally possible (someone other than you knows how). If all four are no, the recommendation is to stop the ritual and escalate the missing owner, not to add a new framework. The follow-on is how you tell that a system you installed is alive.

#### Interview angle

This is the interview. Use the narrative's six beats as the talk track, and keep the 30-60-90 for the "how would you start" question. Lead with a decision and a refusal, not with a list of frameworks.
