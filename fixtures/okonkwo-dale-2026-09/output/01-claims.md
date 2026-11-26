# Stage 01: Claims — Dale Okonkwo

> **Checkpoint not held live.** This was a test run. The step 6 checkpoint (human
> review of the claim list) was not held; the audit was run and the list saved
> without a human seeing it first. A reviewer should still check whether anything
> the client said has been missed, flattened, or quietly interpreted.

Sources: `intake-notes.md` (call notes, 2026-09-29) and `intake-form.md`
(questionnaire, submitted 2026-09-29). `docs/` not read at this stage.

Claims are in the client's words. Where the form answer only makes sense with its
question, the question is given too.

## Fields to always look for

| # | Field | Claim | Source | Confidence |
|---|---|---|---|---|
| 1 | Employer name | "Northwind Logistics Inc." | intake-notes.md:5; intake-form.md:7 | stated |
| 2 | Position or title | "Operations Manager" | intake-notes.md:7; intake-form.md:8 | stated |
| 3 | Start date | "March 2022" | intake-form.md:10 | stated |
| 3 | Start date | Notes do not give a start date | intake-notes.md (silent) | not stated |
| 4 | End date | "End of August 2025" | intake-form.md:11 | stated |
| 4 | End date | Let go "end of August" — no year given in the notes | intake-notes.md:10 | unclear |
| 5 | Length of service (as client states it) | "four years" (notes); "4 years" (form) | intake-notes.md:6; intake-form.md:9 | stated |
| 6 | Compensation — salary | "$72,000" (notes: "Salary: says $72,000"; form, asked "Annual salary": "$72,000") | intake-notes.md:9; intake-form.md:12 | stated |
| 6 | Compensation — how it is paid | Neither source says how pay was paid (frequency or method) | — | not stated |
| 7 | Bonus or commission — whether paid | "Mentioned a bonus" (notes); asked "Were you paid a bonus or commission?": "Yes" (form) | intake-notes.md:9; intake-form.md:13 | stated |
| 7 | Bonus or commission — amount | "it moved around" (notes); "varied" (form). No amount given | intake-notes.md:9; intake-form.md:13 | hedged |
| 8 | Reason given for termination | Told it was "restructuring" | intake-notes.md:10; intake-form.md:14 | stated |
| 8 | Reason given for termination — in writing | "No written reason given on the day; letter came after." | intake-notes.md:10-11 | stated |
| 9 | Written warnings | Asked "Did you receive written warnings?": "No" | intake-form.md:15 | stated |
| 9 | Warnings | "No warnings, no performance plan that he knows of." | intake-notes.md:12 | hedged |
| 9 | Performance management | "no performance plan that he knows of" | intake-notes.md:12 | hedged |
| 10 | Notice or pay in lieu | Asked "Were you given notice or pay in lieu?": "Three weeks" — the answer does not say whether this was notice, pay in lieu, or both | intake-form.md:16 | unclear |
| 10 | Notice or pay in lieu | Notes do not cover notice or pay in lieu | intake-notes.md (silent) | not stated |

## Other claims

| Field | Claim | Source | Confidence |
|---|---|---|---|
| Employer location | "Mississauga" | intake-notes.md:5 | stated |
| Area of work | "Warehouse / ops side" | intake-notes.md:5 | stated |
| Duties | "Managed a team" | intake-notes.md:7-8 | stated |
| Duties | "did scheduling and carrier bookings" | intake-notes.md:8 | stated |
| Break in service | "I had a year out, family stuff" | intake-notes.md:13 | stated |
| Break in service — when | "a while back" | intake-notes.md:13 | hedged |
| Break in service — return | "came back to the same team" | intake-notes.md:13-14 | stated |
| Company property | "Still has his laptop, hasn't returned it." | intake-notes.md:15 | stated |

## Not recorded

Questions and requests are not claims and are left for the lawyer:
intake-notes.md:15 ("Asked what to do"), intake-notes.md:16. The list of documents
the client is sending (intake-notes.md:18) is a note about the file, not a claim
about the employment.

## Audit

| Check | Result |
|---|---|
| Sourced | Pass — every row cites file and line, or says the source is silent |
| No interpretation | Pass — claims quote the client; form answers carry their question where the answer alone is a bare "Yes"/"No"/number |
| Hedges preserved | Pass — "that he knows of", "it moved around", "varied", "a while back" kept verbatim |
| Conflicts kept | Pass — no field where notes and form state different values, so no row is marked `client inconsistent`. Where the two differ in wording or certainty (end date, warnings), both are recorded as separate rows rather than merged |
| Unclear marked | Pass — end date in notes (no year) and "Three weeks" (notice vs pay in lieu) marked `unclear` |
