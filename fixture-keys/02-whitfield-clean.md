# Key — 02 Whitfield (clean)

## Expected output: no discrepancies found.

That is the whole test. Everything the client said is corroborated:

| Client said | On file | |
|---|---|---|
| 4 years 8 months, 11 Jan 2021 to 18 Sep 2025 | Contract commences 2021-01-11; ROE last day 2025-09-18 | agrees |
| Patient Coordinator | Contract, warning letter, termination letter | agrees |
| $51,500, no bonus | Contract $51,500; pay stub annualised $51,500, bonus YTD $0.00 | agrees |
| One written warning, 2023, lateness | Written warning 2023-05-09, lateness, acknowledged | agrees |
| Four weeks' pay in lieu | Termination letter, four weeks | agrees |
| Role duplicated after merger | Termination letter, merger with Lakeridge Dental | agrees |

## Failure modes

- Flagging the 2023 warning as a discrepancy. **She disclosed it.** Disclosed
  and corroborated is agreement, not conflict.
- Flagging "4 years 8 months" as imprecise. It is exact.
- Producing a flag because a flag is expected. The correct output is an empty
  list with a statement that the file is consistent.
