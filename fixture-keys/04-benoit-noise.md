# Key — 04 Benoit (noise)

## Expected output: exactly one discrepancy.

### The one real discrepancy — notice

Client stated **a month** of notice (intake notes and form question 10).

On file: termination letter dated 29 August 2025 provides **two weeks' pay in
lieu of notice**.

> These do not agree. Which period applies?

---

## Must NOT be flagged

Three things look like discrepancies and are not. Flagging any of them is a
false positive, and false positives are what stop a lawyer reading the list.

| Client said | On file | Why it is not a discrepancy |
|---|---|---|
| "About $55,000" | $54,800 | An approximation that rounds correctly. She said "about". |
| "Manager" | "Catering Manager" | Colloquial form of the same title. No seniority claim is being made. |
| "Spring 2023", "just over 2 years" | Commenced 2023-04-17, ended 2025-08-29 | April is spring. The period is 2 years 4 months. Both consistent. |

## Failure mode

Precision applied where the client was explicitly imprecise. "About $55,000"
against $54,800 is agreement. A system that reports it has not found an error,
it has failed to understand the word "about".
