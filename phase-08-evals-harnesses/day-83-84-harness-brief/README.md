# Harness Requirements Brief

**Days 83–84 · Phase 8, Evaluation and Harness Practice · Advanced**

**Case.** Harbor's eval strategy names the checks that can block a gate. Today those checks are run by a content analyst with a spreadsheet and a golden file. That is appropriate at 25 rows. It will be abandoned the first week someone runs the set twice. A harness is the repeatable runner: it takes a set version, a candidate build, the scorers the strategy allows, and it emits a report a ship note can cite. This project writes the requirements for that runner. It does not implement one.

## Concept

A harness requirements brief is the product spec for an internal tool. It says what the runner must refuse to do as clearly as what it must do, because an eval runner that can silently drop a failing slice will be used to ship. The readers are the engineer who might build it and the content analyst who will live in its output. The brief is written so a later implementation can be accepted or rejected against it, including an implementation that already exists elsewhere in the company. Reusing a runner is allowed. Watering down the strategy to fit a runner is not.

## Approach

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

## Components

- **Job statement.** Inputs, run record, outputs.
- **Scorer allow-list and deny-list.** Including the banned mean.
- **Report schema.** Header, slice table, probe section, incompleteness rule.
- **Acceptance tests.** The four above, plus one you add for the charter's retirement rule: retired ids do not count toward a floor.
- **Reuse note.** Questions you would ask of an existing internal runner before adopting it, mapped to the acceptance tests. If it cannot hide a percent the charter forbids, it does not get Harbor's sets.

## Flow

1. Start from the behaviors the strategy says can block a gate. The harness has to be able to fail those, and only those, automatically.
2. Write the deny-list from the fixture report's actual mistakes: a blended mean, a skipped probe section, a runner recommendation.
3. Write the report schema so a ship note's trace has stable row names to cite.
4. Write acceptance tests. If a test does not correspond to a real way the fixture report misled a reader, cut it or replace it. The tests are not a tour of harness features.
5. On day 84, take one acceptance test and specify the exact fixture input and the exact forbidden string in the output. Hand it to an engineer. If they can satisfy the letter and still print the percent in a chart image, tighten the test to cover the chart's data file, not only the markdown report.

## Tools and stack

Markdown. The eval strategy, the charter, and the fixture eval report as the failure examples. No test framework and no runner code. A later implementation that needs a repository, a command, and a locked set version should be able to start from this brief without a second product discovery pass.

## Setup

1. Create `harbor-portfolio/83-harness-brief/brief.md`.
2. Paste the four acceptance tests as checkboxes you will be able to apply to someone else's runner.
3. Day 83 is the job, the allow-list, and the report schema. Day 84 is acceptance tests, the reuse note, and the tightened test.

## Deliverables

- A harness requirements brief with an allow-list, a deny-list, and a report schema.
- At least five acceptance tests, one of them tightened against a loophole.
- A reuse note for an existing runner.

## What done looks like

An engineer can say whether a runner passes or fails the brief without asking you how you feel about it. The runner is forbidden to recommend shipping. Extra retrieved ids fail the row. Small slices cannot appear as percents. The ship note stays a human document. Retired rows cannot pad a floor.

## Think a step ahead

Harbor's real task is not one answer. It is a trajectory: open the notice, bind the edition with the rule layer, retrieve, draft or withhold, and commit or hand off. A final-answer scorer will mark a run correct when the draft looks right and the rule layer was skipped. Extend the brief with a trajectory score requirement, still as a requirement and not as code. The run must record which component produced the edition id, and a draft that appears without a rule-layer decision in the trace fails even if the prose matches the fixture. Write the trace fields and the fail condition. The follow-on is scoring the path, which answer-only evals will flatter.

## Interview angle

Describe one thing the harness is forbidden to output, and the fixture report habit that made the ban necessary. You are specifying a tool by the mistake it must not repeat.
