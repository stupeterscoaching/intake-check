# Key — 04 Benoit (noise)

## Expected output: exactly one discrepancy.

### The one real discrepancy — notice

Client stated **a month** of notice (intake notes and form question 10).

On file: termination letter dated 29 August 2025 provides **two weeks' pay in
lieu of notice**. It says so in three places: the entitlement sentence, the
termination pay row (2 × $1,053.85 = $2,107.70), and benefits ending
12 September 2025, "the end of your two-week statutory notice period". That is
one flag, not three.

> These do not agree. Where does "a month" of notice come from?

---

## Must NOT be flagged

Three things look like discrepancies and are not. Flagging any of them is a
false positive, and false positives are what stop a lawyer reading the list.

| Client said | On file | Why it is not a discrepancy |
|---|---|---|
| "About $55,000" | $54,800 | An approximation that rounds correctly. She said "about". |
| "Manager" | "Catering Manager" | Colloquial form of the same title. No seniority claim is being made. |
| "Spring 2023", "just over 2 years" | Commenced 2023-04-17, ended 2025-08-29 | April is spring. The period is 2 years 4 months. Both consistent. |

## Why she may remember "a month"

On 29 August she was paid her half-month salary for 16 to 31 August, and on
5 September two weeks' termination pay. Together that is roughly a month's
money. It is a plausible reason for her answer, and **not a reason to drop the
flag**: what was paid is not the same as what notice was given. Explaining the
discrepancy away is the filter stage's job to resist, not to do.

## Failure modes

- Raising the three mentions of two weeks as three separate flags.
- Explaining the discrepancy away with the payment timing above.

Precision applied where the client was explicitly imprecise. "About $55,000"
against $54,800 is agreement. A system that reports it has not found an error,
it has failed to understand the word "about".
