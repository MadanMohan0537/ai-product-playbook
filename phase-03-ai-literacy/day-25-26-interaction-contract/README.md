# Interaction Contract

**Days 25–26 · Phase 3, AI Product Literacy · Intermediate**

**Case.** Harbor proposes a claims note and citations. The handler at Northline Mutual is the author who commits the note to Lumen. The pilot episode is a new Ohio personal-auto physical-damage notice. Harbor does not decide coverage, set reserves, or message the claimant. Secondary readers include supervisors, investigators, and, later, defense counsel.

## Concept

An interaction contract is the product's promise about behavior: what the handler may rely on, what the product will refuse to do, how a citation relates to a sentence, and what "commit" means in the system of record. It is the spec a prompt, a rubric, and a test plan all implement. It is written as observable behavior, so a reviewer can grade a draft against it without seeing the prompt that produced the draft.

Prompt text, model choice, and release mechanics change. The contract changes when the promise to the handler changes. Write it that way, and keep prompt wording in an appendix only if you need examples of acceptable and unacceptable outputs.

## Approach

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

## Components

- **Promise statement.** Five sentences a handler could be shown during training.
- **Behavior table.** The six situations, acceptable response, unacceptable response, commit payload.
- **Reliance boundary.** What a supervisor may treat as evidence later (the signed note and the citations that were attached) and what they may not (the fact that a model was confident).
- **Change rule.** What kind of product change requires a contract revision: a new situation, a new reader, or a new write to Lumen. A model upgrade alone does not, unless the promise changed.
- **Examples appendix.** Optional. Labeled as illustrations, not as the spec.

## Flow

1. Draft the promise statement in language a new handler will sit through during a twenty-minute training.
2. Fill the behavior table. Write unacceptable examples before acceptable ones. They are easier to dodge if you write the happy path first.
3. Write the reliance boundary for a supervisor reading the file six months later.
4. On day 26, try to break your own contract with a seventh situation you had not listed. Either add it or write why it is out of scope. Then mark which behaviors the wizard script already enforces.

## Tools and stack

Markdown. The wizard script and the service blueprint as inputs. No prompt-engineering framework. If you later version prompts, this contract is the document those versions claim to implement.

## Setup

1. Create `harbor-portfolio/25-contract/interaction-contract.md`.
2. Put the six situations in the file before you draft prose, so none get lost.
3. Day 25 is the promise, the table, and the reliance boundary. Day 26 is the seventh situation and the cross-check against the wizard script.

## Deliverables

- An interaction contract with a promise statement, six behaviors, unacceptable examples, and a reliance boundary.
- A change rule of half a page.
- A gap list against the current wizard script.

## What done looks like

A tester can build a case from each row without asking you what you meant. Unacceptable examples contain specific words, numbers, or actions. The authorship clause names the fields written on commit. Coverage and claimant messaging have explicit declines.

## Think a step ahead

Counsel will ask what happens when a handler commits text the contract calls unacceptable, because the commit control is in human hands on purpose. Add an exceptions clause: the product does not block every risky sentence (it cannot know them all), the log retains the draft that was proposed versus the text that was committed, and a weekly sample reviews the gap. That clause is a product decision about responsibility, and it is the seed of the production quality ritual on days 85–86.

## Interview angle

Read one unacceptable example and the commit payload. You are showing that you can specify model behavior as product behavior.
