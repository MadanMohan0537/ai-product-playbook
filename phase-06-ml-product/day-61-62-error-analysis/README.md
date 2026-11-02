# Error Analysis and the Fix Portfolio

**Days 61–62 · Phase 6, Machine Learning Product Practice · Advanced**

**Case.** During shadow review, a claims trainer looked at 40 Harbor drafts for Ohio personal-auto notices. Twenty were acceptable under the labeling guideline. Twenty were not. The failures are listed below as a fixture. You will group them, decide which system is actually broken, and write a fix portfolio that does not send every failure to the model team.

## Concept

Error analysis is the practice of reading misses until they become a portfolio of causes, each with an owner. Teams that skip it "improve the model" because that is the team that is listening. In this fixture, several misses are content problems, product-rule problems, or handler-interface problems. A model change would not touch them. The deliverable is a fix portfolio: a small set of actions, each aimed at a cause, with a way to know the action worked, and an explicit "no model change" on the causes that do not deserve one.

## Approach

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

## Components

- **Cause groups.** Name, item ids, owning system, whether a model change is in or out.
- **Fix portfolio.** Up to five actions, with proof and exclusions.
- **Ordering note.** Why the first action is first, tied to the interaction contract.
- **Measurement note.** Which groups are large enough in this sample of forty to discuss as patterns, and which are single items you will watch and not chart. Items 19's page number is a single. Do not invent a rate for it beyond "1 of 40 in this review."
- **Feedback to the guideline.** Any item where the trainer's note and the labeling guideline disagree. If you find none, say what you checked.

## Flow

1. Read all twenty before grouping. First groupings tend to be "the model messed up," which is the grouping you are here to break.
2. Assign an owning system to each item. Where two systems could own it, pick the one that can make the failure impossible, not the one that can apologize after it.
3. Draft actions. Merge only when the proof is the same.
4. Order them. Write the ordering note in sentences, not in a fake numeric score.
5. On day 62, take the top action and write the sprint goal it implies, in the shape you used on days 47–48. The analysis is unfinished if it cannot become a goal.

## Tools and stack

Markdown. A spreadsheet helps if you want to sort item ids. No embedding visualization and no error-analysis framework. Forty notes is a reading job.

## Setup

1. Create `harbor-portfolio/61-errors/analysis.md`.
2. Paste the twenty summaries so your groups can refer to stable ids.
3. Day 61 is grouping. Day 62 is the portfolio, the ordering, and the sprint goal.

## Deliverables

- Cause groups covering all twenty ids.
- A fix portfolio of at most five actions, ordered, with proofs.
- One sprint goal derived from the top action, and a measurement note on singletons.

## What done looks like

Items 8–10 are not assigned to a model retrain as the primary fix. Items 11–12 are treated as contract violations. Item 18 has an owner who can keep a commercial form out of a personal-auto retrieval. The portfolio says what it will not clear. A sprint goal could be picked up on Monday.

## Think a step ahead

Shadow review of forty will not match live traffic once handlers learn to ask shorter questions. Specify a monthly error-review sample that is drawn from committed notes, not from drafts the trainer finds interesting, and write the sampling rule: a fixed count, stratified by result state (`cited`, `no_source`, `declined`) and by whether a citation was opened. Include the rule that any out-of-job sentence found in the sample pages the incident addendum from the comms system, even if the count is one. The follow-on is a sampling frame that cannot be satisfied by rereading the same twenty famous bugs.

## Interview angle

Pick item 8 and item 11 and say, in two sentences each, who fixes them and why a model change is the wrong first move. That is error analysis.
