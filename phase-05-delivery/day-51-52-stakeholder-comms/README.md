# Stakeholder Communication System

**Days 51–52 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** Harbor has a ten-week pilot, a gate map, a RAID log, and a VP who will repeat one sentence in a staff meeting. The audiences who can help or stall the work are the VP of Claims Operations, the Columbus manager, the handler crew, legal, the content owner, engineering, and security. They do not need the same update, and they will invent one if you do not write it.

## Concept

A communication system is the set of artifacts, cadences, and owners that keeps each audience informed enough to do their part and not so informed that they act on a rumor. It includes the note you send when a gate fails. Teams write launch announcements and forget the failure note, which is the one that protects trust.

This project specifies the system for the Harbor pilot and writes the actual templates, filled with realistic pilot content, including a gate-failure note. It is outbound communication design. It does not analyze the sentiment of replies.

## Approach

Define six touches:

1. **VP one-pager, monthly.** The staff sentence from the experiment story, or, before any experiment exists, the gate status and the veto rule. One page. No model architecture.
2. **Columbus manager note, weekly.** What changed on the floor, what you need from her (training hour, a handler's time), and which RAID row needs a claims decision.
3. **Handler briefing, at gate transitions only.** Plain language. What they will see, what they remain responsible for, how to report a bad citation. Not a weekly marketing email. Handlers are in production; respect the queue.
4. **Legal and security digest, at contract and vendor changes.** The diff in the promise, not a full restatement. Link the RAID rows that moved.
5. **Build review, twice a sprint.** The sprint goal, the evidence, the cut. Internal.
6. **Gate-failure note, same day.** What failed, who is accountable, what handlers should do tomorrow (usually "work as before"), and the next decision date. This template is written now, while nobody is ashamed of it.

Write each template filled, not blank. Use week 3 of the pilot as the scenario: the content owner has not delivered the bulletin ingest, wizard week is at risk, and no handler-facing behavior has changed. The VP note has to say that without sounding like an excuse and without implying the model is late. The model is not the late part.

Add a rumor rule. If the Columbus manager hears a different story than the handler briefing, the system has failed. Name the single source: a page everyone can open, with a status line that uses the gate names from the milestone map. The templates point at that line rather than inventing new status words.

## Components

- **Audience table.** Audience, decision they make, cadence, template, author, approver.
- **Six filled templates.** Using the week-3 scenario for the recurring ones, plus the failure note for the missed content-owner gate.
- **Status line vocabulary.** The gate names and the only adjectives allowed (not started, blocked, passed, waived with a link). Ban "on track."
- **Rumor rule.** The source page and what you do when two messages diverge: which one you correct, and how fast.

## Flow

1. List the decision each audience actually makes. Cut any touch that serves no decision. A FYI with no decision is a candidate to delete.
2. Write the status vocabulary from the milestone map before you write prose, so every template uses it.
3. Fill the templates for week 3. Read the handler briefing and the VP note back to back. The facts must match.
4. Write the failure note for the missed bulletin ingest. Include what handlers do tomorrow.
5. On day 52, show the VP note and the handler briefing to a partner. Ask them what is late. If one of them says "the model," rewrite until the late dependency is the content owner.

## Tools and stack

Markdown. A shared page can be a document with a status line at the top; no intranet project is required to specify the system. The filled templates are the deliverable.

## Setup

1. Create `harbor-portfolio/51-comms/system.md` with one section per touch.
2. Keep the milestone gate names visible while you write.
3. Day 51 is the audience table, vocabulary, and the recurring templates. Day 52 is the failure note, the rumor rule, and the partner read.

## Deliverables

- An audience table tied to decisions.
- Six filled templates, including a same-day gate-failure note.
- A status vocabulary and a rumor rule.

## What done looks like

The week-3 VP note and the handler briefing agree on what is late. "On track" does not appear. The failure note tells handlers how to work tomorrow and names a decision date. Every touch has an author. At least one audience you considered did not get a recurring email, and the table says why.

## Think a step ahead

The first time a committed note cites a withdrawn form, the communication system becomes an incident system. Add a one-page incident addendum: who declares it, which audiences hear it within an hour (Columbus manager and legal, not the VP first), what handlers are told to do with drafts already on screen, and when the status line changes. Write the handler sentence now. You will want it to exist before the citation is wrong, not after. The retrieval postmortem on days 73–74 is the learning review that follows; this addendum is the hour-of note.

## Interview angle

Read the failure note. A PM who has already written the bad-news template is easier to trust with a pilot.
