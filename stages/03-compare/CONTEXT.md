# Stage 03: Compare

Put the claims next to the facts. List every difference. Filter nothing.

## Inputs

| Source | File | Scope | Why |
|---|---|---|---|
| Stage 01 | `<client>/output/01-claims.md` | Full file | What the client said |
| Stage 02 | `<client>/output/02-facts.md` | Full file | What the documents say |
| Stage 02 | `<client>/output/02-documents.md` | Full file | Which documents govern |
| Reference | `references/comparison-rules.md` | Full file | How claims and facts are matched |

**Before reading anything else:** the first line of `02-documents.md` must be
`Reviewed: …`. If it is missing or `pending`, stop — the client is at the
documents gate (`../../shared/review-gates.md`).

## Process

1. Match each claim to the facts covering the same field.
2. For each matched pair, record whether they **agree**, **differ**, or the
   claim is **unverifiable** because no governing document covers it.
3. Record every difference, however small. **No judgment about whether it
   matters.** That is stage 04.
4. Record claims with no corresponding document as unverifiable, naming the
   document that would settle them.
5. Record facts with no corresponding claim — something on file the client did
   not mention.
6. Run the audit. Revise before saving.

## Audit

| Check | Pass condition |
|---|---|
| Complete | Every claim from stage 01 appears exactly once |
| Unfiltered | No difference has been dropped for being minor, trivial or obviously an approximation |
| Both directions | Facts the client never mentioned are listed |
| Citations carried | Every row keeps the claim source and the fact citation |
| No conclusions | No row says what a difference means |

## Outputs

| Artifact | Location | Format |
|---|---|---|
| Differences | `<client>/output/03-differences.md` | Table: field, claim, fact, status, sources |
