# Data-Rights and Vendor RAID

**Days 49–50 · Phase 5, Delivery for AI Products · Intermediate**

**Case.** Harbor's drafts are produced by a hosted model. Prompts will include claim facts and excerpts of policy forms. Notes are committed to Lumen. Handlers' edits might, later, be useful as evaluation items. Northline's counsel has not yet said whether a vendor may retain prompts, whether policy forms may be sent to that vendor, or whether a handler's edit can be used to evaluate a model. The pilot clock is running.

## Concept

A RAID log for this kind of pilot is a working list of risks, assumptions, issues, and dependencies that can make the pilot unlawful, untrustworthy, or silently dependent on a vendor's terms. It is updated on a cadence during delivery. It is not a launch workshop and not a one-time premortem. The value is the owner, the next review date, and the decision you will force when a row stays red.

You will write the log for data rights and vendor terms, seed it with rows that are specific to Harbor, and write the weekly review ritual that keeps it alive for the ten weeks.

## Approach

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

## Components

- **RAID table.** At least eight rows with the fields above.
- **Decision calendar.** The seven-day-before-pilot meeting: who must attend, which rows are in scope, what the default is if counsel has not replied (the stricter product behavior).
- **Weekly ritual.** Fifteen minutes. Which rows are read (only red and newly closed), who updates evidence, where the log lives.
- **Handler-promise check.** A column or a note that compares each row with the acceptable-use page, so the log cannot approve a use the handlers were told would not happen.

## Flow

1. Walk one Harbor draft from notice opened to vendor call to commit. Every time data crosses a boundary, start a row.
2. Fill owner and next action. An owner of "legal" is incomplete; name the function and the product person who chases the function.
3. Write the unresolved decision for each row as a product behavior change, not as "escalate."
4. Compare the rows with the acceptable-use page. File a conflict if you find one.
5. On day 50, run the fifteen-minute ritual on your own log as a dry run. Close one row by writing the evidence that would close it, and leave the others honestly open. A log that closes everything in a classroom exercise has been sanitized.

## Tools and stack

Markdown or a spreadsheet with the columns above. No GRC platform. The ritual matters more than the database. Link the acceptable-use document by path so the promise check is real.

## Setup

1. Create `harbor-portfolio/49-raid/raid.md`.
2. Draw the data-boundary walk on paper first: handler, Lumen, Harbor service, vendor, eval store.
3. Day 49 is the boundary walk and the rows. Day 50 is decisions, the promise check, the ritual, and the dry run.

## Deliverables

- A RAID log of at least eight data-rights and vendor rows.
- A decision for each row if it is still open seven days before pilot.
- A fifteen-minute ritual and a note from the dry run.

## What done looks like

Every row can change a product behavior, and that behavior is named. The default when counsel is silent is the stricter path. Handler-facing promises and the log have been compared. At least one row is still open at the end, with an owner and a date.

## Think a step ahead

A zero-retention clause does not settle what the vendor's status page, support staff, or abuse-monitoring pipeline can see. Add a row for human access inside the vendor: who at the vendor can read a prompt, under what incident, and what notice Northline receives. Write the pilot behavior if that notice term is missing from the contract (for example, no loss-description text in the prompt, excerpts of forms only). The follow-on is about people at the vendor, not about the model.

## Interview angle

Walk one row from the data boundary to the product behavior you would ship if the row stays red. That is risk management a PM owns.
