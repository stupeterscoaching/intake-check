# Stage 04: Filter

Decide which differences are real. Record why each discard was discarded.

## Inputs

| Source | File | Scope | Why |
|---|---|---|---|
| Stage 03 | `<client>/output/03-differences.md` | Full file | Every difference found |
| Reference | `references/noise-rules.md` | Full file | Approximation, equivalence, and what is not a discrepancy |

## Process

1. For each difference, decide: **real**, **approximation**, **equivalent**, or
   **unverifiable**. Rows stage 03 marked `unmentioned` are discarded, never
   kept — see `noise-rules.md`, "Unmentioned is not a discrepancy". An
   `unverifiable` row that only claims something did not happen is discarded
   as `absence claim` — see "A claim that something never happened".
2. Write the reason for every decision. One sentence.
3. Nothing is discarded silently. A discard with no stated reason is a bug.
4. Run the audit. Revise before saving.
5. Save with `Review: pending` as the first line. Then stop.

## Checkpoints

| After step | Agent presents | Human decides |
|---|---|---|
| 5 | **Gate.** Kept list and discarded list, each with reasons | Whether anything real was filtered out, or anything trivial survived, and signs off per `../../shared/review-gates.md`. **This is the review that protects the lawyer's trust in the flags.** Stage 05 will not run until they do. |

## Audit

| Check | Pass condition |
|---|---|
| Every row decided | Nothing from stage 03 is unaccounted for |
| Every discard reasoned | No row is removed without a stated reason |
| Hedges honoured | A claim the client hedged ("about", "around") is not treated as precise |
| Unverifiable kept separate | Cannot-check is its own outcome, not a discard and not a flag |
| No arithmetic findings | Nothing is kept as real where the difference was produced by calculation rather than stated in a document |

## Outputs

| Artifact | Location | Format |
|---|---|---|
| Flags | `<client>/output/04-flags.md` | Two tables: kept, and discarded with reasons |
