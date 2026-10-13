# Matching claims to facts

## How to match

Match on **field**, not on wording. "Pay", "salary", "rate" and "what I was on"
are the same field.

Where a claim covers two fields, it was split in stage 01 and matches twice.

## Outcomes

| Outcome | When |
|---|---|
| `agrees` | Claim and governing fact say the same thing |
| `differs` | They say different things |
| `unverifiable` | No governing document covers the field |
| `unmentioned` | A fact on file the client never raised |

## Record everything

Stage 03 does no filtering. A difference of one day, one dollar or one word is
recorded exactly like a difference of four years. Whether it matters is stage
04's decision and it has to be able to see what it is deciding about.

This is the stage where silent tidying does the most damage, because nothing
downstream can tell that a row was never created.

## Non-authoritative documents

Facts from drafts, superseded versions and misfiled documents **do not** take
part in matching. They are carried forward separately so that stage 05 can
report them.

A claim that matches only a non-authoritative document is still `differs`
against the governing one — and the fact that it matches the draft is itself
worth carrying, because it explains where the client got the figure.
