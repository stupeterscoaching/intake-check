# intake-check

Reads a new client's intake file and produces a short list of facts that
disagree, so legal admin can clear them up before lawyer time is spent on them.

An [Interpretable Context Methodology](https://github.com/RinDig/Interpretable-Context-Methodology)
workspace. The folder structure is the architecture — numbered stages run in
order, each reads the previous stage's `output/`, and a human reviews and may
edit every artifact in between. No framework, no server.

## The pipeline

```
intake notes + form + docs/
        |
  01-claims    what the client said
  02-facts     what the documents say, each with a citation
  03-compare   every difference, unfiltered
  04-filter    which differences are real, and why the rest were not
  05-render    the page admin works from
        |
  a short list of facts that disagree
```

Every artifact is a plain markdown file you can open, edit and hand to the next
stage. Two are **hard gates**: a person signs off the document inventory before
the comparison runs, and the kept/discarded flags before the page is written.
The sign-off is the first line of the file, so the folder still shows where
each client stands. See `shared/review-gates.md`.

## The rule

The system states what is on file, names where two things disagree, and asks the
question. **It never answers the question.** Whether a discrepancy changes the
case is the lawyer's judgment.

That is the point of the whole thing, not a caveat on it. See
`shared/output-shape.md`.

## Try it

```
cd intake-check && claude
```

Then: `run fixtures/okonkwo-dale-2026-09`

Five fictional test fixtures are in `fixtures/`, each a different shape:

Five fictional client files, each a different shape. **What each one tests is
deliberately not written down inside `fixtures/`** — the folder has to be
handable to a person or an agent without telling them what to find. The mapping
lives in `fixture-keys/README.md`.

Expected results are in `fixture-keys/`, kept in a separate tree so a fixture can
be handed over without leaking what it should find. **Stages never read them.**

Only `01` tests finding things. The other four test restraint, which is harder
and matters more — a system that always returns flags is one the reader stops
reading.

## Status

Run end to end on two fixtures (2026-11-26) and scored against the keys:
`whitfield-marguerite-2026-10` returns the one-line clean result;
`okonkwo-dale-2026-09` finds all five planted discrepancies. The review gates
were tested too: a stage stops at an unsigned gate and writes nothing. Full
scoring is in [`docs/test-results.md`](docs/test-results.md). The other three
fixtures have not been run. Several rules still carry `??` markers where a real
practitioner needs to set them.

Nothing real is in this repo. Whether real client material may be processed at
all is unresolved and is the firm's decision.
