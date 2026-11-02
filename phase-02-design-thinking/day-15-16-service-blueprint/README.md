# Service Blueprint for a Human and a Model

**Days 15–16 · Phase 2, Design Thinking Studio · Beginner**

**Case.** Harbor is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual. The handler signs the note. Harbor may propose text and citations for the form in force on the date of loss and for the bulletin that amends it. Harbor does not decide coverage, set reserves, or write to the claimant. Pilot: Columbus, Ohio, personal auto, 40 handlers.

## Concept

A service blueprint is a picture of one episode across time, with the customer's path, the employee's path, the visible frontstage, and the backstage work that makes the frontstage true. When a model joins the service, it gets its own lane. It is not a decoration on the employee's lane, and it is not the customer. For Harbor the claimant never sees the model. The employee is the handler. The model lane proposes. A fourth lane, content operations, keeps the library and the bulletin true. Most AI blueprints forget that fourth lane and then act surprised when the draft cites a withdrawn form.

## Approach

Blueprint a single episode: a new Ohio personal-auto physical-damage notice, from the moment the first notice is opened in Lumen to the moment the handler commits the note and the supervisor's audit sample could include it. Use five lanes:

1. **Claimant.** What they are waiting on. They do not interact with Harbor.
2. **Handler frontstage.** What the handler sees and does, including the commit action.
3. **Model lane.** What Harbor retrieves, drafts, and refuses. Include the moment it has no safe citation.
4. **Content and compliance backstage.** Who published the form, who published the bulletin, and how an old edition is withdrawn.
5. **Supervision.** What the supervisor sees later, and which artifacts make the note defensible.

Mark fail points with a specific recovery, not a red dot. A fail point without a recovery is a complaint. Example: the bulletin arrived this morning and is not in the library yet. Recovery: Harbor shows "bulletin not in the published set as of \[time\]" and the handler falls back to the official email, which is an explicit path, not a hidden workaround.

## Components

- **Episode header.** Trigger, end state, actors, and the evidence each actor leaves behind.
- **Lane table or mermaid diagram.** Steps in order. Each step names the actor and the artifact produced.
- **Fail points.** At least five. For each: how the handler notices, what they do next, what gets logged.
- **Line of visibility.** What the handler is allowed to see about the model's sources. Citations are above the line. Hidden chain-of-thought is below it and stays there.
- **Support processes.** Library publish, bulletin ingest, access removal when a handler changes office.

## Flow

1. List the steps of the before-path from the problem-solution narrative. Place each step in a lane.
2. Insert the model lane only where the selected how-might-we concept acts. Do not insert it into every step.
3. Add the content-operations lane. If you cannot name a human owner for "bulletin published," write "owner missing" and treat it as a fail point.
4. Write five fail points with recoveries. At least one recovery must be "do not draft."
5. On day 16, walk the blueprint with a clock. Note which steps add handle time. A blueprint that saves nine minutes of searching and adds ten minutes of checking citations has not yet earned its place.

## Tools and stack

Markdown with a [mermaid](https://mermaid.js.org/) sequence or flowchart is enough. A spreadsheet with one column per lane also works and is easier to review in a pull request. Pick one and keep it legible in plain text.

## Setup

1. Create `harbor-portfolio/15-blueprint/blueprint.md`.
2. Put the selected concept from the workshop at the top, in two sentences.
3. Day 15 is lanes and the happy path. Day 16 is fail points, the line of visibility, and the clock check.

## Deliverables

- A blueprint of the episode with five lanes.
- Five fail points, each with a handler-visible recovery and a log line.
- A short timing note: which steps you expect to get faster, which get slower, and what you will time in a pilot.

## What done looks like

An engineer can see where a model call happens and where it must not. A compliance partner can see who publishes a bulletin and what the handler sees if today's bulletin is missing. The claimant lane contains waiting and a phone call, and contains no chat with Harbor.

## Think a step ahead

The blueprint assumes one office and one library. The next stress is a handler in Columbus opening a claim for a policy written in another state, or a temporary supervisor from a different line of business. Add a lane note for "wrong library": what the service does when the handler's office and the policy's governing state disagree. That note becomes an access and precedence requirement in the retrieval work on days 65–74.

## Interview angle

Narrate one fail point end to end, including the log line. Service design for AI is the recovery, not the happy path.
