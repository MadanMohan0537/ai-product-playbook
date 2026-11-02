# Knowledge Publishing Pipeline

**Days 91–92 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** Harbor may cite a document only after it is published into the pilot corpus by a named content owner. The owner's real work is a pipeline, whether or not anyone has drawn it: a form or bulletin arrives, someone checks the edition and the amend relationship, it becomes retrievable, and, when it is wrong or withdrawn, it stops being retrievable. The pilot's freshness promise and the `bulletin_missing` reason code are both promises about this pipeline. This project writes the pipeline as an operating design: stages, roles, clocks, and the emergency stop.

## Concept

A knowledge publishing pipeline is the system of record for what the assistant is allowed to say. Retrieval quality cannot exceed it. The design names the stages from "received" to "retrievable" to "withdrawn," the human checks at each stage, the maximum time a known bulletin may sit unpublished before Harbor must show `bulletin_missing`, and the path that pulls a bad document out faster than the ordinary cadence. It is a product operations spec. It does not select a CMS, a crawler, or an embedding job. Those are implementations that have to honor the clocks.

## Approach

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

## Components

- **Stage definitions.** Entry condition, exit condition, who acts, what Harbor is allowed to do while the instance is in that stage.
- **Clocks.** Ordinary publish, emergency withdrawal, after-hours rule.
- **Fail-closed rule.** Withdrawn means not retrievable, with a golden-set consequence.
- **Correction handoff.** From withdrawn id to a list of affected notices to a named office owner.
- **Intake refusal.** The reply text for an out-of-scope drop.

## Flow

1. Write stages from the handler's point of view: at which stage could a citation first appear? The answer should be Published, only.
2. Add the second-person check on amend links. If the pilot cannot staff it, the stage does not silently drop the check; the corpus scope shrinks until the check is real. Choose and write it down.
3. Set clocks and the after-hours rule.
4. Write the correction handoff and the intake refusal.
5. On day 92, simulate a wrong rental number discovered at 4:30 p.m. Walk the clock minute by minute and name the person acting at each step. If the simulation reaches "someone should probably unpublish it tomorrow," the design is not done.

## Tools and stack

Markdown, plus a stage table a content owner could pin. No CMS build and no crawler. If the company later uses a document platform, the stages and clocks are the acceptance criteria for how it is configured.

## Setup

1. Create `harbor-portfolio/91-knowledge-pipeline/pipeline.md`.
2. Start from "Harbor cannot see this stage" as a column in the table, so visibility is a decision per stage.
3. Day 91 is stages and clocks. Day 92 is fail-closed behavior, the correction handoff, the refusal text, and the 4:30 p.m. simulation.

## Deliverables

- A stage model with owners and Harbor visibility.
- Clocks for ordinary publish and emergency withdrawal.
- A fail-closed rule, a correction handoff, an intake refusal, and the simulation note.

## What done looks like

A document in intake cannot be cited. Withdrawal has a person and a two-hour clock, and the 4:30 p.m. simulation names the after-hours behavior instead of hoping. Affected committed notes have a path to a human correction. Out-of-scope drops have a refusal text. The golden set is named as the place a withdrawn id must return nothing.

## Think a step ahead

Withdrawal during the day does not repair a draft already on a handler's screen, rendered at 3:00 p.m. from a corpus that was valid at 3:00 p.m. Specify a screen contract: each draft carries the corpus publish timestamp it was built from, the client re-checks that timestamp at commit, and a commit against a since-withdrawn id is refused with copy that tells the handler the source was withdrawn and the note must be written in Lumen. Write the copy and the log event. The follow-on closes the gap between the pipeline's clock and the draft sitting open on the floor, which is the gap handlers will actually hit.

## Interview angle

Walk the 4:30 p.m. withdrawal through the clock and the commit-time re-check. Publishing is a safety system with hours, not a content calendar.
