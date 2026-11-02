# Wizard-of-Oz Interaction Script

**Days 17–18 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. The pilot episode is a new Ohio personal-auto physical-damage notice: cite the form in force on the date of loss, apply the latest bulletin, commit the note. Harbor does not decide coverage, set reserves, or message the claimant.

## Concept

A wizard-of-oz prototype tests the interaction while a human supplies the intelligence behind the curtain. You learn whether the handler can understand, edit, and responsibly commit a draft before you learn whether a model can produce one. For Harbor this is the right order. A fluent draft that handlers paste without reading would be a failed test, even if the draft were correct.

You will write the script a human wizard follows, the screen the handler thinks they are using, and the test protocol for five handlers. You will also write the latency budget. If the wizard is faster than any model you could deploy, the test has lied to you about pacing, so the script includes a deliberate wait.

## Approach

Specify the interaction as a script with two roles, Handler and Wizard, plus a Facilitator who does not help. The wizard may use the real policy PDFs and the bulletin. The wizard may not invent policy language. If the wizard cannot find a citation in sixty seconds, the scripted behavior is the product's "I do not have a published source" state, not a best guess.

The handler's screen, described in words and a rough layout, shows three regions: the claim facts already in Lumen (read-only), the proposed note with citations under each paragraph, and a commit control that stays disabled until the handler has expanded at least one citation or typed an edit. That last rule is a hypothesis you are testing, not a law. The protocol asks whether the forced expand feels like safety or like nagging.

Write a latency budget in the script: after the handler asks for a draft, the wizard waits eight seconds even if they are ready sooner, then reveals the draft in one piece. Handlers should feel a pause. You will record whether they use the pause to keep reading the first notice or whether they context-switch away.

## Components

- **Screen description.** Regions, what is read-only, the commit control and its disabled rule, the empty and error states.
- **Wizard script.** What the wizard may open, the sixty-second citation rule, the eight-second floor, and the exact text of the no-source state.
- **Task set.** Three tasks: a clean match, a bulletin-amends-PDF case, and a no-source case. Claim facts may be fictional; policy sentences the wizard pastes must come from a document you actually provide as a fixture.
- **Observation sheet.** Time to commit, whether the citation was opened, edits made, and any sentence the handler committed that the wizard did not support.
- **Debrief.** Four questions that ask about the episode, not about whether the prototype was "cool."

## Flow

1. Write the screen description. Mark the commit rule as a hypothesis.
2. Write the wizard script, including the behaviors the wizard is forbidden to do (no coverage language, no extra helpfulness).
3. Author three tiny fictional claim facts and a one-page fixture excerpt the wizard is allowed to cite. Keep the fixture obviously fake if you do not have a real public form; label it "fixture language, not Northline policy."
4. Run the script once with a friend as handler, you as wizard. Fill the observation sheet.
5. On day 18, revise the one moment that confused the handler. Write what you will measure if you later run all five sessions. Running all five is ideal and not required to finish this project.

## Tools and stack

Markdown script, a printed or on-screen mock laid out with plain text or a simple diagram, and a stopwatch. A slide is enough of a screen. No Figma requirement and no model in the loop. The human wizard is the method.

## Setup

1. Create `harbor-portfolio/17-wizard/` with `script.md`, `fixture-excerpt.md`, and `observation.md`.
2. Recruit one colleague who is not a PM to play the handler. Brief them with the case in five lines and no more.
3. Day 17 is the script and the fixture. Day 18 is the live run and the revision.

## Deliverables

- Wizard script with latency floor, citation deadline, and forbidden moves.
- Screen description and three tasks.
- One completed observation sheet and a revision note.

## What done looks like

A second facilitator could run session two from the script without you. The observation sheet says whether the handler opened a citation before committing. The no-source task has a written state, and the wizard did not improvise a paragraph when the fixture had no answer.

## Think a step ahead

A wizard who knows the fixture will unconsciously write clearer citations than a retrieval system will. Add a "degraded wizard" pass: on one task, the wizard must include one irrelevant sentence and one citation that points at the right document and the wrong paragraph. Record whether the handler catches each. That pass is a preview of the error-analysis workshop on days 61–62, and it tells you how much checking the commit step really buys.

## Interview angle

Describe what the handler did during the eight seconds, and whether they caught the planted bad citation. Interaction tests are about behavior under a realistic flaw.
