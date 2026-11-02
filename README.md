# AI Product Playbook

A beginner-to-advanced curriculum for product managers who ship in the AI era. Fifty standalone projects, organized in ten phases, following one continuing case from a blank page to a gated pilot.

**[Read the full plan in PLAN.md](PLAN.md).** That document writes out every phase and every project: goals, skills, concept, approach, components, flow, tools, deliverables, and the follow-on each project anticipates. The tables below are the catalog. The folders are the working copies, one project at a time.

Maintained by [Madan Mohan](https://github.com/MadanMohan0537).

## How to use it

Work in order if you are building the muscle for the first time. Open a single project if you already know which muscle is weak. Each folder stands alone: it restates the case, names the artifact, and says what done looks like.

Keep a local `harbor-portfolio/` folder of the documents you produce. Later projects refer to earlier decisions, and the capstone asks you to narrate them. Nothing here requires a paid API, a cloud account, or a running model. A markdown editor, a spreadsheet, and the fixtures in a few folders are the stack on purpose. The skill being practiced is the decision artifact.

## The case that runs through every project

**Harbor** is a draft-and-cite assistant for personal-auto claims handlers at Northline Mutual, a fictional mid-size US insurer. Handlers remain the author of every note. Harbor does not decide coverage, set reserves, or write to the claimant. The pilot on offer is the Columbus, Ohio office: 40 handlers. A claims-operations review reports 26 minutes average handle time on a new auto claim, about 9 of those minutes spent finding the policy form in force on the date of loss, and 3.1% of audited notes citing a form that was not in force. The library is roughly 1,400 pages, plus a weekly compliance bulletin.

Northline, Lumen (the claims system), and the handlers in the fixtures are invented. Numbers in fixtures are given so you can practice claim hygiene. They are not results from a real pilot.

## Where the topics sit

| Topic | Where you practice it |
| --- | --- |
| Product management | Phases 1, 5, and 10, and the decision artifacts throughout |
| Project management | Phase 5 |
| Design thinking | Phase 2 |
| AI, including what a model class can and cannot own | Phase 3 |
| Transformers, as product constraints | Days 23–24 |
| Analytics and data analytics | Phases 4 and 9 |
| Machine learning | Phase 6 |
| RAG, as a product rather than a tutorial stack | Phase 7 |
| Evals and AI evals | Phase 8 |
| Harnesses | Days 83–84 |
| Pipelines | Phase 9 |

## Phase map

| Phase | Days | Level | Projects |
| --- | --- | ---: | ---: |
| [1. Product Sense Studio](#phase-1--product-sense-studio) | 1–10 | Beginner | 5 |
| [2. Design Thinking Studio](#phase-2--design-thinking-studio) | 11–20 | Beginner | 5 |
| [3. AI Product Literacy](#phase-3--ai-product-literacy) | 21–30 | Intermediate | 5 |
| [4. Decision Analytics](#phase-4--decision-analytics) | 31–42 | Intermediate | 6 |
| [5. Delivery for AI Products](#phase-5--delivery-for-ai-products) | 43–52 | Intermediate | 5 |
| [6. Machine Learning Product Practice](#phase-6--machine-learning-product-practice) | 53–64 | Advanced | 6 |
| [7. Retrieval-Augmented Product Design](#phase-7--retrieval-augmented-product-design) | 65–74 | Advanced | 5 |
| [8. Evaluation and Harness Practice](#phase-8--evaluation-and-harness-practice) | 75–86 | Advanced | 6 |
| [9. Data Pipelines and Trust](#phase-9--data-pipelines-and-trust) | 87–94 | Advanced | 4 |
| [10. Advanced Bets](#phase-10--advanced-bets) | 95–100 | Advanced | 3 |

## Phase 1 — Product Sense Studio

Days 1–10. Beginner. Five projects.

Learn to fence a problem, separate evidence from opinion, describe the job a person has already hired a workaround to do, and say what a pilot will not automate. No model required. The output of this phase is a problem a later spec is allowed to solve.

| Days | Project | Summary |
| --- | --- | --- |
| 1–2 | [Opportunity Brief](phase-01-product-sense/day-01-02-opportunity-brief/README.md) | Write the one-page argument for a single-office pilot, including the decisions Harbor must not make. |
| 3–4 | [Interview Field Kit](phase-01-product-sense/day-03-04-interview-field-kit/README.md) | Build a discussion guide, tag two transcripts, and keep opinions out of the insight memo. |
| 5–6 | [Switch Story](phase-01-product-sense/day-05-06-switch-story/README.md) | Record the forces behind two different workarounds handlers have already hired. |
| 7–8 | [Problem-Solution Narrative](phase-01-product-sense/day-07-08-problem-solution-narrative/README.md) | Tell one claim episode before and after the assistant, with a human commit point. |
| 9–10 | [Competitive Teardown](phase-01-product-sense/day-09-10-competitive-teardown/README.md) | Compare public alternatives, including the shared drive, and write the capabilities you will not chase. |

## Phase 2 — Design Thinking Studio

Days 11–20. Beginner. Five projects.

Move from the problem to a service a handler can survive: extremes, a workshop with kill criteria, a blueprint that gives content operations a lane, a wizard-of-oz script, and a critique built for generative screens.

| Days | Project | Summary |
| --- | --- | --- |
| 11–12 | [Empathy Maps and Extreme Users](phase-02-design-thinking/day-11-12-empathy-and-extremes/README.md) | Map who you have actually heard, and choose which failure line the pilot protects first. |
| 13–14 | [How-Might-We Workshop](phase-02-design-thinking/day-13-14-how-might-we/README.md) | Diverge on paper, then kill ideas against criteria you froze before scoring. |
| 15–16 | [Service Blueprint](phase-02-design-thinking/day-15-16-service-blueprint/README.md) | Draw the episode across handler, model, content operations, supervision, and the waiting claimant. |
| 17–18 | [Wizard-of-Oz Script](phase-02-design-thinking/day-17-18-wizard-of-oz/README.md) | Test commit behavior with a human wizard, a latency floor, and a citation the wizard must not invent. |
| 19–20 | [Critique and Test Plan](phase-02-design-thinking/day-19-20-critique-and-test-plan/README.md) | Grade the screen on authorship, provenance, uncertainty, editability, reversibility, and pace. |

## Phase 3 — AI Product Literacy

Days 21–30. Intermediate. Five projects.

Learn enough about model classes, transformer constraints, and cost to specify behavior. The artifacts are a capability card, a constraint backlog, an interaction contract, a unit-economics memo, and an acceptable-use policy.

| Days | Project | Summary |
| --- | --- | --- |
| 21–22 | [Model Capability Card](phase-03-ai-literacy/day-21-22-model-capability-card/README.md) | Judge three model classes against Harbor's moves, with visible cost arithmetic. |
| 23–24 | [Transformer Constraints](phase-03-ai-literacy/day-23-24-transformer-constraints/README.md) | Turn tokens, context, attention, and sampling into backlog items a designer can build. |
| 25–26 | [Interaction Contract](phase-03-ai-literacy/day-25-26-interaction-contract/README.md) | Specify the drafts a handler may rely on, the refusals, and what commit writes to the file. |
| 27–28 | [Unit Economics and Latency](phase-03-ai-literacy/day-27-28-unit-economics/README.md) | Model cost per draft and the latency behavior, and name the assumption that flips the bet. |
| 29–30 | [Principles and Acceptable Use](phase-03-ai-literacy/day-29-30-principles-and-use-policy/README.md) | Write the rules handlers and supervisors see, and the reply when a senior asks for coverage decisions. |

## Phase 4 — Decision Analytics

Days 31–42. Intermediate. Six projects.

Define measures before you collect them, instrument an AI interaction without copying the note into an analytics stream, and practice reading funnels, mixed evidence, dashboards, and a fixed experiment table.

| Days | Project | Summary |
| --- | --- | --- |
| 31–32 | [Metric Tree](phase-04-decision-analytics/day-31-32-metric-tree/README.md) | Tie the pilot's numbers to expand, hold, or stop, and pair every efficiency win with a guardrail. |
| 33–34 | [Tracking Plan](phase-04-decision-analytics/day-33-34-tracking-plan/README.md) | Specify the events that can compute the tree, and the fields that stay out of the stream. |
| 35–36 | [Activation Funnel](phase-04-decision-analytics/day-35-36-activation-funnel/README.md) | Compute activation from a twelve-handler fixture and reject a definition that flatters the product. |
| 37–38 | [Triangulation Memo](phase-04-decision-analytics/day-37-38-triangulation-memo/README.md) | Answer whether handlers check citations or paste drafts, using counts and quotes in the same claim. |
| 39–40 | [Dashboard Spec](phase-04-decision-analytics/day-39-40-dashboard-spec/README.md) | Specify the Monday page and the monthly page, including the week the audit file does not arrive. |
| 41–42 | [Experiment Story](phase-04-decision-analytics/day-41-42-experiment-story/README.md) | Turn a handed-to-you result table into a sentence you will allow and a list you will not say. |

## Phase 5 — Delivery for AI Products

Days 43–52. Intermediate. Five projects.

Run the pilot as a sequence of evidence gates. Plan dependencies you do not control, write sprint goals that can fail honestly, keep a data-rights log, and design the messages for the week a gate slips.

| Days | Project | Summary |
| --- | --- | --- |
| 43–44 | [Milestone Map and RACI](phase-05-delivery/day-43-44-milestone-map/README.md) | Lay ten weeks of gates, proofs, and a single accountable owner per gate. |
| 45–46 | [Dependency Map](phase-05-delivery/day-45-46-dependency-map/README.md) | Sum lead times across legal, content, and Lumen, and change the plan where the chain does not fit. |
| 47–48 | [Sprint Goals](phase-05-delivery/day-47-48-sprint-goals/README.md) | Replace "finish the API" with two goals defined by evidence, plus the cut rule for day 6. |
| 49–50 | [Data-Rights RAID](phase-05-delivery/day-49-50-data-rights-raid/README.md) | Log vendor, retention, and prompt risks, each with the product behavior if the row stays red. |
| 51–52 | [Stakeholder Communications](phase-05-delivery/day-51-52-stakeholder-comms/README.md) | Write the audience system, including the same-day note for a missed gate. |

## Phase 6 — Machine Learning Product Practice

Days 53–64. Advanced. Six projects.

Decide which subtask is a rule, which is a model, and which is not a model yet. Then specify labels, features, costs, errors, and the card a handler-facing disclosure has to match.

| Days | Project | Summary |
| --- | --- | --- |
| 53–54 | [Approach Decision](phase-06-ml-product/day-53-54-approach-decision/README.md) | Assign edition selection to a rule and sentence drafting to a language model, with overturn conditions. |
| 55–56 | [Labeling Guideline](phase-06-ml-product/day-55-56-labeling-guideline/README.md) | Define the judgments, write fifteen gold examples, and adjudicate the borderline ones. |
| 57–58 | [Feature Specification](phase-06-ml-product/day-57-58-feature-spec/README.md) | Specify an audit-priority score with point-in-time rules, leakage stories, and prohibited fields. |
| 59–60 | [Cost Matrix](phase-06-ml-product/day-59-60-cost-matrix/README.md) | Choose a threshold from confusion counts and supervisor hours, and show why accuracy flatters. |
| 61–62 | [Error Analysis](phase-06-ml-product/day-61-62-error-analysis/README.md) | Sort twenty failed drafts by the system that must fix them, and keep a retrain off the ones it cannot. |
| 63–64 | [Model Card and Disclosure](phase-06-ml-product/day-63-64-model-card/README.md) | Write the drafting card, a short disclosure, and a stub that stops the audit score from borrowing either. |

## Phase 7 — Retrieval-Augmented Product Design

Days 65–74. Advanced. Five projects.

Treat retrieval as a product with an empty-result behavior, a corpus policy, a golden set, an answer experience, and a postmortem that blames a wrong real document correctly.

| Days | Project | Summary |
| --- | --- | --- |
| 65–66 | [Retrieval Requirements](phase-07-rag-product/day-65-66-retrieval-prd/README.md) | Specify reason codes, the corpus boundary, and the freshness promise the content owner must hit. |
| 67–68 | [Corpus Policy and Citations](phase-07-rag-product/day-67-68-corpus-and-citations/README.md) | Write precedence when a bulletin and a form disagree, and the fields a citation must show. |
| 69–70 | [Golden Question Set](phase-07-rag-product/day-69-70-golden-questions/README.md) | Author twenty-five retrieval items, including unanswerables, with slice floors and a leakage rule. |
| 71–72 | [Answer Experience](phase-07-rag-product/day-71-72-answer-experience/README.md) | Design full, partial, empty, and out-of-job states, and withhold a draft when a missing source would change a number. |
| 73–74 | [Retrieval Postmortem](phase-07-rag-product/day-73-74-retrieval-postmortem/README.md) | Review a committed citation of the wrong real form, and change a spec or a test rather than a prompt. |

## Phase 8 — Evaluation and Harness Practice

Days 75–86. Advanced. Six projects.

Decide what is allowed to block a release, write anchors a second grader can use, govern the sets, read a bad-tempered report honestly, specify a harness by what it must refuse to print, and install the weekly quality meeting.

| Days | Project | Summary |
| --- | --- | --- |
| 75–76 | [Evaluation Strategy](phase-08-evals-harnesses/day-75-76-eval-strategy/README.md) | Bind each behavior to a method and a gate, and keep a single quality score from deciding the pilot. |
| 77–78 | [Anchored Rubric](phase-08-evals-harnesses/day-77-78-anchored-rubric/README.md) | Write fail, meet, and exceed anchors, and leave the overall average off the score form. |
| 79–80 | [Gold-Set Charter](phase-08-evals-harnesses/day-79-80-gold-set-charter/README.md) | Assign an owner, a change rule, and a leakage rule to every living set, and decline a blended set. |
| 81–82 | [Eval Ship Note](phase-08-evals-harnesses/day-81-82-eval-ship-note/README.md) | Read a fixture report and make a ship, restrict, or hold call the strategy can defend. |
| 83–84 | [Harness Requirements](phase-08-evals-harnesses/day-83-84-harness-brief/README.md) | Specify a runner that cannot recommend shipping, cannot hide a small slice, and fails extra retrieved ids. |
| 85–86 | [Production Quality Ritual](phase-08-evals-harnesses/day-85-86-quality-ritual/README.md) | Run a weekly continue, restrict, or pause meeting, with a same-day path for a single bad note. |

## Phase 9 — Data Pipelines and Trust

Days 87–94. Advanced. Four projects.

Design the paths that make the earlier promises true in week six: human feedback that does not become a sneaky training set, analytics numbers that can be withheld, a publishing clock for the corpus, and a deletion story that survives contact with a fine-tune.

| Days | Project | Summary |
| --- | --- | --- |
| 87–88 | [Human Feedback Pipeline](phase-09-pipelines/day-87-88-feedback-pipeline/README.md) | Route citation flags to reviewed eval candidates, and stop note bodies at a named stage. |
| 89–90 | [Analytics Trust Runbook](phase-09-pipelines/day-89-90-analytics-trust/README.md) | Handle duplicate events, missing builds, late audits, and broken joins before they become a decision. |
| 91–92 | [Knowledge Publishing Pipeline](phase-09-pipelines/day-91-92-knowledge-pipeline/README.md) | Move a document from intake to published to withdrawn, with clocks and a fail-closed rule. |
| 93–94 | [Training-Data Lineage](phase-09-pipelines/day-93-94-training-lineage/README.md) | Specify the record a row must carry, and the choice when a deletion arrives after training consumed it. |

## Phase 10 — Advanced Bets

Days 95–100. Advanced. Three projects.

Spend the judgment on purpose. Choose what not to platform, package the cost without a fantasy price, and compress the stack into a narrative and a first ninety days that do not start with a rebuild.

| Days | Project | Summary |
| --- | --- | --- |
| 95–96 | [Platform versus Feature](phase-10-advanced-bets/day-95-96-platform-bet/README.md) | Choose depth, platform-first, or a declared sequence, with kill criteria and a tenant who must bring a corpus owner. |
| 97–98 | [Pricing and Packaging](phase-10-advanced-bets/day-97-98-pricing-packaging/README.md) | Package the assistant as capacity with a pause when the ceiling breaks, and refuse an outcome fee you cannot adjudicate. |
| 99–100 | [Capstone Narrative](phase-10-advanced-bets/day-99-100-capstone/README.md) | Tell the six decisions in under 1,200 words, then write a 30-60-90 that installs a cadence on a team that already has tools. |

## Fixtures

Three projects include something to push against, so the write-up is not only a prompt to imagine data:

- [Handler transcripts](phase-01-product-sense/day-03-04-interview-field-kit/fixtures/transcripts.md) for the field kit and the switch story.
- [Event CSV](phase-04-decision-analytics/day-35-36-activation-funnel/fixtures/copilot_events.csv) for the activation funnel.
- [Eval report](phase-08-evals-harnesses/day-81-82-eval-ship-note/fixtures/eval_report.md) for the ship note.

Other projects embed a table, a failure list, or a scenario in the project file itself.

## What this curriculum is for

It is a practice repo for AI-era product judgment: framing, design, specification, measurement, delivery, and the operations that keep a generative feature inside its promise. The folder you leave with is a set of Harbor decisions you can talk through in a product interview, starting from the [capstone](phase-10-advanced-bets/day-99-100-capstone/README.md).
