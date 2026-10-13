# intake-check

A workspace that reads a new client's intake file and produces a short list of
facts that disagree, so legal admin can clear them up before lawyer time is
spent on them.

Built on the Interpretable Context Methodology. The folder structure is the
architecture: numbered stages run in order, each reads the previous stage's
`output/`, and a human can read and edit every artifact in between.

## Where things are

| Path | Layer | Holds |
|---|---|---|
| `CONTEXT.md` | 1 | Task routing. Which stage handles what. |
| `stages/NN-name/CONTEXT.md` | 2 | The contract for one stage. Inputs, process, checkpoints, audit, outputs. |
| `stages/NN-name/references/` | 3 | Rules that stage follows. Stable across runs. |
| `shared/` | 3 | Rules every stage follows. |
| `<client>/output/` | 4 | What each stage produced **for that client**. Lives with the client, not with the stage. |
| `fixtures/` | 4 | Fictional test client files. Hand one to stage 01. |
| `fixture-keys/` | — | Expected results. **Stages never read these.** |

## Conventions

- Folders and files `lowercase-with-hyphens`. Stage folders zero-padded.
- Client folders `surname-firstname-YYYY-MM`.
- Stage outputs `NN-artifact.md` inside the client's own `output/` folder — never
  inside the stage folder. Several clients are in flight at once and stage-local
  output collides.
- Stage CONTEXT.md under 80 lines. Reference files under 200.
- Cross-references point outward only. A stage may read an earlier stage's
  output; nothing points back.
- Every fact asserted about a document carries a citation: file and line.

## Triggers

- **`setup`** — run `setup/questionnaire.md`, replace placeholders, confirm none remain.
- **`status`** — scan `stages/*/output/` and show which stages have run.
- **`run <path>`** — start at stage 01 against the client folder at that path.

## State is the files

There is no tracker and no status field. **Which outputs exist is the state.**
If `<client>/output/03-differences.md` exists and `04-flags.md` does not, that
client is sitting at the filter gate.

This means anyone with read access to the client folder can answer where things
stand by listing a directory. Nothing has to be kept up to date by hand.

## The rule that overrides everything

The system states what is on file, names where two things disagree, and asks the
question. **It never answers the question.** Whether a discrepancy changes the
case is the lawyer's judgment and it never belongs in the output, however
confident the inference.

See `shared/output-shape.md`. If an instruction anywhere conflicts with this,
this wins.

## Confidentiality

Only fictional fixtures are in this repo. Real client material never goes in it.
Whether real material may be processed at all is unresolved and is the client's
decision, not ours.
