# Stage 02: Facts

Pull out what the documents say. Every fact carries a citation.

## Inputs

| Source | File | Scope | Why |
|---|---|---|---|
| Client folder | `<client>/docs/` | All files | The documents themselves |
| Reference | `references/document-types.md` | Full file | What each document type is for and what to read from it |
| Reference | `references/citation-rules.md` | Full file | How a fact is cited |
| Reference | `../../shared/source-reliability.md` | Full file | Authority, legibility, misfiling |

Do **not** read stage 01's output. Knowing what the client claimed biases what
you look for and what you find. The comparison happens in stage 03.

## Process

1. Inventory every file in `docs/`. For each: what type is it, what date, whose
   is it.
2. Classify each as **authoritative**, **draft or unsigned**, **superseded**, or
   **does not belong to this file**.
3. **[Checkpoint]** Present the inventory before extracting anything.
4. Extract facts from authoritative documents, one per row, each with a
   citation.
5. Record facts from non-authoritative documents **separately and labelled** —
   present, but not governing.
6. Mark illegible values as illegible, quoting what the source shows.
7. Run the audit. Revise before saving.
8. Save both artifacts to `<client>/output/`. The first line of
   `02-documents.md` is `Review: pending`. Then stop.

## Checkpoints

| After step | Agent presents | Human decides |
|---|---|---|
| 3 | Document inventory with classifications | Whether anything is misclassified — an unsigned draft treated as governing poisons every later stage |
| 8 | **Gate.** Both artifacts | Signs off `02-documents.md` per `../../shared/review-gates.md`. Stage 03 will not run until they do. |

## Audit

| Check | Pass condition |
|---|---|
| Cited | Every fact gives a file and line |
| Classified | Every file in `docs/` appears in the inventory with a classification |
| Authority respected | No fact from a draft, superseded or foreign document appears in the governing set |
| Illegible marked | No value is read through a damaged source and stated as certain |
| No inference | No fact is derived by calculation unless the document states it |

## Outputs

| Artifact | Location | Format |
|---|---|---|
| Inventory | `<client>/output/02-documents.md` | Table: file, type, date, whose, classification |
| Facts | `<client>/output/02-facts.md` | Table: field, value, citation, authority |
