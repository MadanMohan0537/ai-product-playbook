# Training-Data Lineage and Deletion

**Days 93–94 · Phase 9, Data Pipelines and Trust · Advanced**

**Case.** The feedback pipeline forbids training on Harbor notes during the pilot. A future quarter may reopen that decision for a narrow evaluation set, and a vendor or an internal team may already be talking about a fine-tune. Separately, Northline can receive a deletion or retention demand for a claimant's information. If any claim fact has entered a dataset, someone will ask whether the model still "has" it. This project writes the lineage and deletion brief so that question has an answer other than a shrug. It does not build a training run, and it does not audit a synthetic dataset. The asset is the record of what a row is, where it went, and what you do when it must die.

## Concept

Lineage is the chain from a source event to a dataset version to a model version that consumed it. Deletion is the product and legal behavior when a link in that chain must be removed or when removal is no longer possible. A brief that says "we honor deletion requests" without saying what happens to a fine-tune that already consumed the row is a slogan. You will write the fields every training-candidate row must carry, the uses those fields permit, and the decision tree when a row is already baked into a model.

## Approach

Specify the minimum lineage record for any row that might leave the reviewed-candidate table, even for an offline eval export:

- source act and source id (the citation flag, not a vague "user feedback"),
- notice id and the retention class of the notice,
- what was stripped, as a list of field classes removed, not the removed content,
- dataset name and version the row was exported into, if any,
- purpose flag: `eval` or `train`, default `eval`,
- model version that consumed it, empty until true,
- legal basis note: a pointer to the closed RAID row that allowed the export, empty if none, and an export with an empty basis is forbidden,
- deletion status: `active`, `suppressed`, `exported-then-suppressed`.

Purpose and basis are product controls. An engineer does not flip `train` because a notebook is convenient. The brief names the decision forum (the same escalation path as a principle change) and the default (export refused).

Write the deletion tree.

1. **Row only in the candidate table, never exported.** Suppress the row, keep a tombstone with no claim content, so you can prove the suppression. Harbor behavior is unchanged.
2. **Exported to an eval set, not consumed by a training run.** Remove the row in the next set version, retire the id under the charter, and mark prior reports that included it as "set version superseded" if the row could have changed a gate. For Harbor's citation ids this will be rare; the rule still exists.
3. **Consumed by a model version.** You cannot promise the row is gone from the weights. The decision, made with counsel, is one of: stop using that model version for Harbor and return to the prior version or to no-model; or keep the version under a written residual-risk acceptance that names the model version, the data class, and the review date. There is no third option called "approximately deleted." Write that sentence in the brief.

State the pilot default, given training is forbidden: any deletion demand is case 1, and the brief's job is to keep the pilot from accidentally creating case 3. The control is the empty legal-basis field blocking export, plus a quarterly confirmation from the model owner that no Harbor row was in a training file. The confirmation is a ritual, not a tool. Name the owner.

Write what the handler-facing product does during a deletion. Nothing visible, unless the deletion withdraws a source document, which is the knowledge pipeline's job, not this one. Say that explicitly so the two pipelines are not mashed into one project.

## Components

- **Lineage fields.** The list above, with who is allowed to set each field.
- **Export gate.** Empty basis or `train` without a forum decision blocks the export. Write it as an acceptance condition.
- **Deletion tree.** Three cases, the tombstone rule, and the banned phrase "approximately deleted."
- **Pilot default and quarterly confirmation.** Who signs, what they sign, where it is kept.
- **Boundary with the knowledge pipeline.** Deleting a training row is not withdrawing a form. Withdrawing a form is not a deletion of a claimant's note.

## Flow

1. Draft the fields from a row's life, from flag to export to hypothetical training. Cut any field you cannot imagine a person filling. A lineage record nobody fills is fiction.
2. Write the export gate as a block, not a warning.
3. Write the deletion tree, case 3 last, with counsel in the decision.
4. Set the pilot default and the quarterly confirmation.
5. On day 94, run a tabletop: a claimant deletion arrives, and an engineer admits a notebook export happened last month with no basis field set. Apply the tree. The honest case may be "we must treat it as case 3 because we cannot prove it was not consumed." Write that outcome and the control that should have made the export impossible. If the tabletop is comfortable, you have not made the export gate concrete enough.

## Tools and stack

Markdown. The feedback-pipeline brief and the RAID log as inputs. No training stack, no feature store, and no synthetic-data generator. The quarterly confirmation can be a checklist in the same file.

## Setup

1. Create `harbor-portfolio/93-lineage/brief.md`.
2. Write "approximately deleted is not a status" at the top and keep it in the final deletion section.
3. Day 93 is fields and the export gate. Day 94 is the deletion tree, the confirmation, and the tabletop.

## Deliverables

- A lineage field list and an export gate.
- A three-case deletion tree with a tombstone rule.
- A pilot default, a quarterly confirmation, and a tabletop note that includes an untracked export.

## What done looks like

A row cannot be exported for training by changing a config in silence. Case 3 names a real choice: stop using the model version, or accept residual risk in writing with counsel. The pilot default is that training rows do not exist, and the confirmation exists so the default stays true. The knowledge pipeline is a different path, and the brief says so. The tabletop ended in a specific case, not in a promise to do better.

## Think a step ahead

A vendor fine-tune may keep training artifacts the quarterly confirmation cannot see, because the confirmation is about Northline's files. Add a vendor clause to the RAID log's training row: the vendor certifies that prompts and exports from the pilot tenant were not used to train a model shared with other customers, names the model versions that statement covers, and notifies Northline before a version trained on any Northline content is served back to Harbor. Write the product behavior if the certification is missing or late: Harbor stays on the rule layer and retrieval citations with no vendor prose, which is a fallback you have already specified elsewhere. The follow-on ties lineage to the vendor boundary, where a local tombstone does not reach.

## Interview angle

Explain case 3 in plain language, including the option to stop using the model version. Then the export gate that keeps the pilot out of case 3. Lineage is a decision tree, not a metadata hobby.
