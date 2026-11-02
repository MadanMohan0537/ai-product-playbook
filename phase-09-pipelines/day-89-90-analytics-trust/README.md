# Analytics Trust Runbook

**Days 89–90 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** Harbor's Monday packet depends on events: drafts shown, citations opened, notes committed, audit results joined later. The Columbus office also runs a small robotic process that re-saves notes in Lumen after a supervisor stamp. Nobody told the product team. In week 4 the "committed with draft" count jumped, and the north-star conversation almost happened on a lie. This project writes the runbook a PM and an analytics partner use when a number moves for a pipeline reason, and the checks that would have caught this jump before the meeting.

## Concept

An analytics trust runbook is the incident process for decision metrics. It assumes the definition in the metric tree is right and the figure on the page is still wrong, because the events were duplicated, dropped, late, mis-joined, or produced by a bot. The runbook tells the on-call pair how to decide, within a business day, whether Monday's packet is usable. It is about the behavioral-event path and the audit-file join. It is not a general data-contract platform and not a customer-evidence integrity product. Those solve neighboring problems for other systems.

## Approach

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

## Components

- **Four plays.** Notice, confirm, packet action, fix.
- **Friday checklist.** Pass/fail, thresholds, owner of each check.
- **Status line.** The words used when metrics are withheld, and the channel that is deliberately not used.
- **Bot register.** A table the Columbus manager can add to when a new automation appears. The robotic stamp is row one, marked as discovered late, with the date of discovery written as a lesson.
- **Reconstruction limit.** What you will not do: silently restate last week's packet after you "fix" history. If history is restated, the next packet says the restatement happened and which weeks changed.

## Flow

1. Write the duplicate-commit play first, from the scenario, before generalizing.
2. Add the other three plays. Each needs a confirm step that a person can do without a new tool, even if the confirm is "count unmatched ids in the join output."
3. Turn the confirms into the Friday checklist with thresholds.
4. Write the status line and the reconstruction limit.
5. On day 90, tabletop the robotic-stamp failure with a partner playing the VP who wants the number anyway. The runbook should give you a sentence and a fallback figure (Lumen's own count, labeled as a different metric) or a clean withhold. If the tabletop ends with you reading the broken number "with a caveat," the runbook failed and you tighten the packet action.

## Tools and stack

Markdown. A spreadsheet mock of the checklist is optional. No warehouse project. The runbook should be usable by two people who can see event counts and the audit file, which is the actual staffing of a forty-person pilot.

## Setup

1. Create `harbor-portfolio/89-analytics-trust/runbook.md`.
2. Put the status-line wording at the top so the plays cannot invent softer language later.
3. Day 89 is the four plays and the bot register. Day 90 is the checklist, the reconstruction limit, and the tabletop.

## Deliverables

- Four failure plays with packet actions.
- A Friday checklist with thresholds.
- A status line, a bot register with the stamp as row one, and a tabletop note.

## What done looks like

A duplicate-commit week cannot become a north-star conversation. A join failure cannot report zero defects. The checklist has owners and pass/fail. The VP tabletop produced a withhold or a clearly labeled fallback, and the wording is in the runbook. Pipeline bad news does not use the citation-incident template.

## Think a step ahead

The robotic stamp is one automation. The next one will be a handler-side macro that opens every citation in the background to satisfy the "citation opened" metric once people learn it is watched. Extend the bot register into a behavior register: events whose timestamps are too regular, or whose time-to-open is below a floor you set, are quarantined from the citation metric and reviewed as possible gaming. Write the floor as a hypothesis, the quarantine rule, and the conversation owner (the Columbus manager, not an automated accusation in the packet). The follow-on treats gaming as a pipeline-trust problem, because a gamed event is not a human act even when a human installed the macro.

## Interview angle

Tell the robotic-stamp story through the packet action. Then the reason a join failure must not look like a perfect guardrail. Trust work is the number you refused to show.
