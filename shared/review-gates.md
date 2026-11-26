# Review gates

Two stages stop for a person before anything downstream may run. The gate is
recorded in the artifact itself, so the files still are the state.

| Gate | Artifact | Person checks | Blocks |
|---|---|---|---|
| Documents | `<client>/output/02-documents.md` | Every classification. An unsigned draft treated as governing, or a misfiled document used as evidence, poisons every later stage. | Stage 03 |
| Flags | `<client>/output/04-flags.md` | The kept list and the discarded list. Anything real filtered out, anything trivial kept. This is the review that protects the lawyer's trust in the page. | Stage 05 |

## How a gate is recorded

1. The stage saves its artifact with this as the **first line**:

   `Review: pending`

2. A person reads the artifact, edits it if needed, and replaces that line with:

   `Reviewed: <name>, <YYYY-MM-DD>` — optionally followed by ` · changed: <what>`

3. The blocked stage reads that first line **before anything else**. If it is
   missing or says `pending`, it stops and reports `<client> is at the <gate>
   gate`. It does not run, and it does not run "just this once".

## Who may write the Reviewed line

A person. The agent writes it only when a person says, in their own words, that
they have reviewed that file — and then with that person's name and today's
date. "Continue", "next", "run it" and "looks fine" about a different file are
not a review. Never write it to unblock yourself.

## Why only two

Stage 01 also has a checkpoint, but a missed claim surfaces later as an
unmatched fact, so it presents and continues. Stage 03 filters nothing, so
there is nothing to approve. Stage 05's reader is the reviewer.
