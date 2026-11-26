# Stage 05: Render

Write the page admin reads. No new facts, no conclusions.

## Inputs

| Source | File | Scope | Why |
|---|---|---|---|
| Stage 04 | `<client>/output/04-flags.md` | Kept list, and the unverifiable list | What goes on the page |
| Stage 03 | `<client>/output/03-differences.md` | Claim, Fact and Sources columns, for the rows 04 kept or marked unverifiable | The client's words, the on-file wording, and their citations. 04 carries decisions, not wording. |
| Stage 02 | `<client>/output/02-documents.md` | Non-authoritative and misfiled rows | Document problems are reported too |
| Reference | `../01-claims/references/claim-rules.md` | "Fields to always look for" | Flag order |
| Reference | `../../shared/output-shape.md` | Full file | The four-part flag format and the never-answer rule |
| Reference | `references/page-format.md` | Full file | Order, headings, length |

**Before reading anything else:** the first line of `04-flags.md` must be
`Reviewed: …`. If it is missing or `pending`, stop — the client is at the flags
gate (`../../shared/review-gates.md`).

## Process

1. Write each kept flag in the four-part shape: what the client said, what is on
   file with citations, that they disagree, and the question.
2. Add a section for anything unverifiable, naming the document that would
   settle it.
3. Add a section for document problems — drafts, misfiled documents, illegible
   sources.
4. If nothing was kept, say so in one line. Do not pad.
5. Run the audit. Revise before saving.

## Audit

| Check | Pass condition |
|---|---|
| No new facts | Every statement traces to a stage 04 row or a stage 02 citation |
| Never-answer | No sentence says what a discrepancy means, whether there is a case, or connects two facts into a theory |
| Every flag asks | Each flag ends in a question addressed to a person |
| Citations survive | Every fact still shows its file and line |
| One glance | A flag can be verified by opening one cited document |
| Empty is allowed | A clean file produces a one-line statement, not invented content |

## Outputs

| Artifact | Location | Format |
|---|---|---|
| Pre-consult flags | `<client>/output/05-pre-consult-flags.md` | The page admin works from |
