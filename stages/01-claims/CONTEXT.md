# Stage 01: Claims

Pull out what the client said. Capture only — no checking, no interpretation.

## Inputs

| Source | File | Scope | Why |
|---|---|---|---|
| Client folder | `<client>/intake-notes.md` | Full file | What they said on the call |
| Client folder | `<client>/intake-form.md` | Full file | Their written answers |
| Reference | `references/claim-rules.md` | Full file | What counts as a claim, how to write one |
| Reference | `../../shared/source-reliability.md` | "Is the source legible?" | Transcription and note quality |

Do **not** read `docs/`. That is stage 02's job and mixing them is how a claim
gets silently corrected before anyone sees it disagreed.

## Process

1. Read the intake notes and the intake form.
2. Extract every factual claim the client makes, one per row, with its source
   line.
3. Where notes and form say the same thing, record once and cite both.
4. Where they say different things, record **both** — the client disagreeing
   with themselves is a finding, not an error to tidy.
5. Mark any claim the source states unclearly as `unclear`, quoting what the
   source actually says.
6. **[Checkpoint]** Present the claim list.
7. Run the audit. Revise before saving.
8. Save to `output/`.

## Checkpoints

| After step | Agent presents | Human decides |
|---|---|---|
| 6 | The full claim list with sources | Whether anything the client said has been missed, flattened, or quietly interpreted |

## Audit

| Check | Pass condition |
|---|---|
| Sourced | Every claim cites a file and line |
| No interpretation | No claim contains a word the client did not say or clearly mean |
| Hedges preserved | "About", "around", "maybe", "not sure" are kept verbatim, never rounded away |
| Conflicts kept | Where notes and form differ, both appear |
| Unclear marked | Anything ambiguous in the source is marked `unclear`, not resolved |

## Outputs

| Artifact | Location | Format |
|---|---|---|
| Claims | `output/[client-slug]-claims.md` | Table: field, claim, source, confidence |
