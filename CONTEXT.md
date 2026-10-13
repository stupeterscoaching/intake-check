# intake-check — task routing

Intake notes and client documents in, a list of facts that disagree out.

## Task routing

| Task | Go to | Produces |
|---|---|---|
| Pull out what the client said | `stages/01-claims/CONTEXT.md` | Structured claims |
| Pull out what the documents say | `stages/02-facts/CONTEXT.md` | Facts, each with a citation |
| Find every difference | `stages/03-compare/CONTEXT.md` | Differences, unfiltered |
| Decide which differences are real | `stages/04-filter/CONTEXT.md` | Survivors, and what was discarded |
| Write the page admin reads | `stages/05-render/CONTEXT.md` | The flag list |

Stages run in order. Each reads the previous stage's `output/`. A human reviews
and may edit any output before the next stage runs.

## Shared resources

| Resource | Location | Holds |
|---|---|---|
| Output shape | `shared/output-shape.md` | The flag format and the never-answer rule |
| Source reliability | `shared/source-reliability.md` | What to do when a source is unclear or not authoritative |
| Test fixtures | `fixtures/` | Five fictional client files, different shapes |

## Entry

Start at stage 01 with a client folder containing intake notes, an intake form,
and a `docs/` folder. `fixtures/01-okonkwo-dense/` is the worked example.
