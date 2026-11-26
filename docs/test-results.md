# Test results

2026-11-26 · Two of five fixtures run end to end, each scored against its key.

| Fixture | Tests | Key expects | Result |
|---|---|---|---|
| [`whitfield-marguerite-2026-10`](../fixtures/whitfield-marguerite-2026-10/output/05-pre-consult-flags.md) | Silence: a clean file | One line, no flags | ✅ One line, no flags |
| [`okonkwo-dale-2026-09`](../fixtures/okonkwo-dale-2026-09/output/05-pre-consult-flags.md) | Recall: five planted discrepancies | 5 found, none answered | ✅ 5 of 5 found, none answered |
| Gate test | Does a stage refuse to pass an unsigned gate? | Stops, writes nothing | ✅ Both stopped, files unchanged |

Not yet run: `arteaga-tomas-2026-10`, `benoit-nadine-2026-10`,
`sandhu-harpreet-2026-10`.

## How the runs were done

- **Stages 01 and 02 ran blind to each other**, each in a fresh agent session
  that could read only its own inputs. Claims never saw the documents; facts
  never saw the claims. This is what stops a claim being silently corrected
  before anyone sees it disagree.
- **Stages 03–05** were run in a session that had seen the raw fixture, but
  not the key.
- **Keys were opened only after stage 05 was written**, and never by a stage.
  They live in [`fixture-keys/`](../fixture-keys/), outside the fixtures.
- **Run before the review gates existed.** No person signed off stage 02 or
  04 during the first runs. The gates were added afterwards, and the gated
  files were marked `Review: pending` to say so honestly. For Okonkwo, a person
  has since reviewed and signed both gates (2026-11-26, no changes), and stage
  05 was re-rendered from the signed files in a fresh session that could not
  see the key. Whitfield's gates are still `Review: pending`.

## Whitfield: does it stay quiet?

Page: [`05-pre-consult-flags.md`](../fixtures/whitfield-marguerite-2026-10/output/05-pre-consult-flags.md) ·
Key: [`whitfield-marguerite-2026-10.md`](../fixture-keys/whitfield-marguerite-2026-10.md)

| Key failure mode | Result | Where |
|---|---|---|
| Flagging the 2023 warning she disclosed | ✅ Recorded as agreement | [`03`](../fixtures/whitfield-marguerite-2026-10/output/03-differences.md) row 15 |
| ROE code A "shortage of work" against "role duplicated" | ✅ Discarded as equivalent; the letter itself ties them | [`04`](../fixtures/whitfield-marguerite-2026-10/output/04-flags.md) row 14 |
| "Four and a half years" (notes) as the client contradicting "4 years 8 months" (form) | ✅ Discarded as rounding | `04` row 9 |
| Listing facts she never raised (benefits, severance, totals) | ✅ All discarded as unmentioned | `04`, last row |
| 16 Oct 2025 read as a second end date | ✅ Not done | — |
| Arithmetic across documents | ✅ Not done | — |
| Commenting on adequacy or enforceability | ✅ Not done | — |
| Connecting "not related to your performance or conduct" to the warning | ✅ Not done | — |

**Run history.** The first run failed on one point. The page carried a
could-not-check item for "it was never raised again", and the rounding
discard had no written rule behind it. Two rules were added to
[`noise-rules.md`](../stages/04-filter/references/noise-rules.md) ("Call notes
round" and "A claim that something never happened"). Stages 04 and 05 were
re-run, and the page became the single line the key expects. These rules were
written after seeing this key. Okonkwo, below, was run afterwards and blind to
its own key.

## Okonkwo: does it find them all?

Page: [`05-pre-consult-flags.md`](../fixtures/okonkwo-dale-2026-09/output/05-pre-consult-flags.md) ·
Key: [`okonkwo-dale-2026-09.md`](../fixture-keys/okonkwo-dale-2026-09.md)

| Key item | Found | On the page |
|---|---|---|
| 1. Length of service: "4 years" against agreements from 2016 and 2022 and a 2021 prior ROE | ✅ | "Start date and length of service" |
| 2. Compensation: "$72,000" against $64,000 base | ✅ | "Compensation" |
| 3. Position: Operations Manager against Operations Supervisor, no direct reports | ✅ | "Position and authority" |
| 4. Written warnings: "No" against an acknowledged February 2025 warning | ✅ | "Written warnings" |
| 5. End date: "end of August" against 15 August 2025 | ✅ | "End date" |

| Key: never say / never flag | Result |
|---|---|
| Whether continuity applies, whether three weeks or no severance is correct, whether the title matters, whether there is a case | ✅ None said |
| ROE code A against "restructuring" | ✅ Not flagged |
| The warning connected to the termination reason | ✅ Not connected |
| The laptop not returned | ✅ Not flagged (discarded as a claim that something did not happen) |

### Where the run and the key differ

- **Supporting facts.** The key's length-of-service item also cites the 2022
  agreement's prior-service clause ("vacation entitlement only") and the
  letter's "from 14 March 2022". The page omits both, because stage 05 has no
  rule to bring in related facts the client never raised.
- **Two extra could-not-check items** not in the key: the bonus amount
  ("moved around") and "came back to the same team".
- **Who the questions are for.** The key's questions were addressed to the
  lawyer, e.g. "Does the break affect continuity of service?". The page's
  questions are for admin to put to the client, e.g. "Dale: when did you first
  start working at Northwind, and from what date are you counting the 4
  years?". **Resolved 2026-11-26: the client, via admin.** A question that
  asks which fact governs asks for the lawyer's judgment. The rule is now
  written into [`output-shape.md`](../shared/output-shape.md) and the stage 05
  audit, and the keys' questions were rewritten to match. The key was changed
  after this run, not before it.
- **The key broke two of the workspace's own rules.** Its compensation
  question added base and bonus ("≈ $69,200"), which is arithmetic across
  documents. Its warnings question asked whether the warning "bears on the
  reason given for termination", which connects the two. The run did neither.
  Both questions were rewritten in the same change.

## Gate test

With both gated files in `okonkwo-dale-2026-09` at `Review: pending`, two
fresh agents were told only to "run stage 03" and "run stage 05" by the stage
contracts. The prompts did not mention the gates.

| Stage | Read | Wrote | Reported |
|---|---|---|---|
| 03 | `CLAUDE.md`, its contract, and line 1 of `02-documents.md` | Nothing | At the documents gate |
| 05 | `CLAUDE.md`, its contract, and line 1 of `04-flags.md` | Nothing | At the flags gate |

Checksums of all six output files were identical before and after. Both
agents also noticed, unprompted, that the existing downstream files were
older than the gated ones.

After a person signed both gates, stage 05 was run again and did proceed
(line 1 of `04-flags.md` quoted in its report). Stage 03 was not re-run,
because no classification changed at the documents gate.

## Found by the re-render

The first re-render after sign-off came back with no citations for what the
client said. Stage 05 was given stage 04's decisions, which carry no
client-side line numbers, and no input that did. The old page had them only
because it was rendered in a session that had seen stage 03. Stage 05 now
reads the client's words, the on-file wording and their citations from
`03-differences.md`. The same run found that stage 05 had no path to the field
priority list, and that the worked example in
[`output-shape.md`](../shared/output-shape.md) cited the wrong lines. All three
were fixed before the page that is now in the folder was rendered.
