Review: pending

# 02 — Document inventory: okonkwo-dale-2026-09

> **Checkpoint not held live.** Step 3 (human review of this inventory before
> extraction) could not be held during this test run. The inventory was audited
> and saved, and extraction went ahead on the classifications below. A reviewer
> should confirm the classifications before stage 03 runs, and the two
> classification calls flagged under "Judgement calls" in particular.

## Inventory

| File | Type | Date | Whose | Classification |
|---|---|---|---|---|
| `docs/employment-contract-2016.md` | Employment agreement | 4 July 2016 (`:5`) | Northwind Logistics Inc. and Dale Okonkwo (`:3`) | **Authoritative**: signed by both parties (`:16`). See judgement call 1. |
| `docs/employment-contract-2022.md` | Employment agreement | 28 February 2022 (`:5`) | Northwind Logistics Inc. and Dale Okonkwo (`:3`) | **Authoritative**: signed by both parties (`:20`) |
| `docs/job-description.md` | Job description | "Revised January 2024" (`:3`) | Northwind Logistics Inc., role of Operations Supervisor (`:1`). Does not name an employee. | **Authoritative**: company role document, not marked draft, no blank signature block. See judgement call 2. |
| `docs/pay-stub-2025-08.md` | Pay statement | Period 2025-08-03 to 2025-08-16, pay date 2025-08-22 (`:5`) | Dale Okonkwo, Employee No. 10448, Northwind Logistics Inc. (`:3`) | **Authoritative**: employer-issued pay record. See judgement call 2. |
| `docs/record-of-employment.md` | Record of Employment (ROE) | No issue date shown. Last day paid 2025-08-15 (`:9`) | Dale Okonkwo, employer Northwind Logistics Inc. (`:3`, `:4`) | **Authoritative**: employer-issued statutory record. See judgement call 2. |
| `docs/termination-letter.md` | Termination letter | 18 August 2025 (`:5`) | Addressed to Mr. Dale Okonkwo (`:10`), from Northwind Logistics Inc. (`:1`) | **Authoritative**: signed by the employer (`:114`, `:116`) |
| `docs/written-warning-2025-02.md` | Written warning | 2025-02-11 (`:3`) | Dale Okonkwo, Employee No. 10448 (`:5`), Northwind Logistics Inc. (`:1`) | **Authoritative**: issued by P. Whitcombe (`:7`), acknowledged by employee 2025-02-13 (`:29`) |

7 files in `docs/`. All 7 are in the inventory. None is marked draft. None has a
blank signature block. None names a different person or employer.

## Observations

These are things the file does or does not contain. Absences have no line
number, so they are recorded here and not in the facts table.

1. **Two signed employment agreements are on file (2016 and 2022).** Neither one
   says whether the 2022 agreement replaces, supersedes or amends the 2016
   agreement. Neither has an entire-agreement clause. Both are recorded in the
   facts. This file does not decide which one governs.
2. **The 2016 agreement has no bonus clause and no prior-service clause.** The
   2022 agreement has both. The 2022 prior-service clause is quoted word for
   word in the facts table.
3. **No document on file says when or how the employment under the 2016
   agreement ended.** The ROE notes that "a prior ROE was issued for this
   employee in 2021". That 2021 ROE is not on file.
4. **No document on file covers the period between the 2016 agreement and the
   2022 agreement** (no pay records, no termination or resignation record, no
   rehire record).
5. **No offer letter is on file** for either agreement.
6. **The job description does not name Dale Okonkwo.** It describes the
   Operations Supervisor role, is unsigned, and is dated "Revised January 2024",
   which is after the 2022 agreement.
7. **One pay statement only** (period 2025-08-03 to 2025-08-16). The termination
   letter says a pay statement for the termination lump sum "will be issued with
   the deposit". That statement is not on file. Nothing on file shows that the
   amounts in the letter were actually paid.
8. **No vacation records are on file.** The termination letter states 7 days of
   accrued and unused vacation. No other document on file records vacation
   accrued or taken.
9. **No bonus records are on file** apart from the YTD line on the August 2025
   pay stub ("Bonus (paid 2025-03-14) $5,200.00"). No bonus letter or bonus
   calculation is on file for any year.
10. **No document on file shows the employee's response to the termination
    letter.** There is no signed acknowledgement, release or reply.
11. **The ROE shows no issue date**, and no serial number or issuer signature.
12. **The termination letter's signature shows as the placeholder
    `_[signed]_`** (`:114`), above the typed name Paula Whitcombe. The 2016 and
    2022 agreements show their signatures as typed names. No signature image
    appears in any document.
13. **Legibility.** No damaged, garbled or illegible values were found in any of
    the 7 documents. The ROE's SIN shows as "[redacted]" (`:4`). That is a
    redaction, not damage.

## Judgement calls (for the reviewer)

1. **2016 agreement classified as authoritative, not superseded.** It is signed
   and dated by both parties. A later signed agreement exists, but neither
   document says the later one supersedes the earlier one. Calling it
   superseded would mean concluding something the documents do not state. Its
   facts are kept in the governing set under their own sub-heading. If the
   reviewer classifies it as superseded, move those rows to the
   non-authoritative set.
2. **Unsigned records classified as authoritative.** The "unsigned →
   not authoritative" rule in `shared/source-reliability.md` was applied to
   documents that would normally be signed (agreements, letters). It was not
   applied to employer records that are not normally signed: the job
   description, the pay statement and the ROE. None of the three is marked
   draft or has a blank signature block.
