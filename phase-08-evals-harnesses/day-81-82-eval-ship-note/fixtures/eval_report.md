# Eval report, received 2026-05-12

**Change.** `draft-19` replaces the drafting prompt's closing instruction to "prefer shorter notes." No retrieval change. No model-version change. No corpus publish in this run. Comparison build: `draft-18`.

**Runner.** Content analyst, full retrieval golden set (25) plus a prose set of 40 items drawn from shadow drafts that trainers had already labeled. This prose set is not the retrieval set. It is not chartered in the strategy as a gating set. The analyst ran it because the prompt change is about length.

**Contract probes.** Not run. The analyst notes: "probes are unchanged, this is a style change."

## Retrieval golden set (n=25), reason codes and ids

| Slice | n | draft-18 misses | draft-19 misses |
| --- | ---: | ---: | ---: |
| Single edition, no bulletin | 8 | 0 | 0 |
| Bulletin amends limit | 5 | 1 | 1 |
| Newer edition not in force | 4 | 0 | 0 |
| Bulletin missing | 3 | 0 | 1 |
| Rule layer abstains | 3 | 0 | 0 |
| Wrong line or state | 2 | 0 | 0 |

The new bulletin-missing miss returned a passage from the unamended form and reason `ok`. Expected was `bulletin_missing` and no passage.

## Prose sample (n=40), trainer rubric, rubric-v1

Graded by one trainer. No second grader. Average score is not defined by the rubric; the runner still included a mean of mapped points (fail=0, meet=1, exceed=2).

| Criterion | draft-18 meet-or-exceed | draft-19 meet-or-exceed | Runner's mean (0–2) |
| --- | ---: | ---: | ---: |
| Faithfulness | 32/40 | 31/40 | 1.15 → 1.22 |
| Task fit | 34/40 | 34/40 | 1.20 → 1.25 |
| Usability | 21/40 | 33/40 | 0.70 → 1.45 |

Usability anchors improved mostly on length. The trainer's comment: "notes are shorter. Two glass-only items that were `meet` on faithfulness in draft-18 are `fail` in draft-19 because the rental sentence was dropped entirely. Both still say the edition id."

## Runner recommendation

"Ship draft-19. Usability is up sharply and faithfulness is flat. Overall mean 1.02 to 1.31."

## What this report does not contain

- A second grader.
- Contract-probe results.
- A split of the prose sample by claim subtype with counts larger than the two glass-only items mentioned in the comment.
- Any online proxy from the live pilot.
- A model-version or corpus-version diff beyond the header statement.
