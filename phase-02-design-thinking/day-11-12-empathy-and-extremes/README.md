# Empathy Maps and Extreme Users

**Days 11–12 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot candidate: Columbus, Ohio, 40 handlers. Baseline: 26 minutes on a new auto claim, about 9 minutes finding the form in force, 3.1% of audited notes citing a form that was not in force. Practice transcripts for two day-shift handlers live in [`../../phase-01-product-sense/day-03-04-interview-field-kit/fixtures/transcripts.md`](../../phase-01-product-sense/day-03-04-interview-field-kit/fixtures/transcripts.md).

## Concept

An empathy map puts one person's situation on a single page: what they are trying to do, what they see on screen, what they say to a coworker, what they do under pressure, and what they fear will be true of them if they are wrong. Extreme users are the people at the edge of that situation, where a design that works for a confident four-year handler fails in a way that matters.

For Harbor, the instructive extremes are not "power users who love AI." They are the new handler who will paste a wrong paragraph rather than leave a note blank, the night-shift handler whose help-desk index is stale, the supervisor who must defend the note six months later, and the handler who was written up because a sentence in a note sounded like a coverage denial.

## Approach

Build four maps. Two are grounded in the transcripts (Priya, Andre). Two are extreme sketches you label as hypotheses, because you have not interviewed them: a night-shift handler, and a supervisor who audits 8% of notes. A hypothesis map is useful only if every item is marked "heard" or "supposed." Mixing the two is how teams invent a user and then build for the invention.

On each map, add a failure line: the sentence this person is afraid will appear in a file with their name on it. That line is more useful than a demographic. Priya's failure line is a denial that she did not mean to write. Andre's failure line is a blank note that fails audit, which pushes him toward copying anything the tool offers at the end of a long day.

## Components

- **Map header.** Role, tenure, shift, claim mix, and whether the map is heard or supposed.
- **Doing and seeing.** The actual artifacts on their desk or screen during a new auto notice.
- **Saying and hearing.** What coworkers and supervisors tell them. Quote the transcripts where you have them.
- **Fearing.** The career or claimant consequence they are managing.
- **Failure line.** The bad sentence in the file.
- **Design implication.** One behavior Harbor must support or prevent for this person. Implications are not features. "Must show the bulletin date next to the form edition" is an implication. "Add a chatbot" is not.

## Flow

1. Fill Priya's map only from transcript quotes. If you cannot point at a line, it does not go in the heard map.
2. Fill Andre's map the same way. Pay attention to the closure metric he named. Speed pressure is part of his empathy map, and it is a risk to accuracy.
3. Draft the night-shift and supervisor maps. Stamp every sticky as supposed. Write the interview question that would promote it to heard.
4. Compare failure lines. Circle the place where helping Andre's speed makes Priya's failure line more likely.
5. On day 12, choose the extreme you will design for first, and write five lines on what you will deliberately make slightly worse for a different user in order to protect that extreme.

## Tools and stack

Markdown, or four sheets of paper photographed and summarized back into markdown. The durable artifact is the markdown, because a photo of stickies does not survive a portfolio review on its own.

## Setup

1. Create `harbor-portfolio/11-empathy/maps.md`.
2. Open the transcripts beside the file.
3. Day 11 is the two heard maps. Day 12 is the two supposed maps, the conflict between them, and the choice of who you design for first.

## Deliverables

- Four empathy maps with heard and supposed stamps.
- Four failure lines.
- A one-page choice: which extreme the pilot protects first, what that costs another user, and the interview that would change your mind.

## What done looks like

A designer can start a workshop from the maps without inventing a new persona. The two supposed maps are visibly less certain than the heard maps. The choice of who to protect first is explicit, including the cost.

## Think a step ahead

Empathy maps decay when the office changes shift patterns or when a new bulletin type arrives. Add a refresh rule: which map items expire after the next bulletin cycle, and who on the pilot team is responsible for re-hearing them. A map that cannot say when it becomes fiction will be treated as fact in a roadmap review three months from now.

## Interview angle

Show the heard-versus-supposed stamp. It signals that you know the difference between research and a plausible story.
