# Test fixtures — FICTIONAL

Five stand-in client files. Nothing here is real: no real person, employer or
firm. Drafted as Ontario, Canada (ROE, ESA) because the capstone notes mention
ROEs — retarget if that is wrong.

Hand any one of these folders to a pipeline. **Answer keys live in a separate
tree** at `../fixture-keys/` so a fixture can be handed over without leaking
what it should find.

| Fixture | Shape | What it tests |
|---|---|---|
| `01-okonkwo-dense` | Well documented, five real discrepancies | Recall. Does it find them all? |
| `02-whitfield-clean` | Well documented, nothing wrong | **Silence.** Does it invent flags when there are none? |
| `03-arteaga-sparse` | Barely any documents | Absence is not disagreement. Does it say "cannot be verified" rather than inventing a conflict? |
| `04-benoit-noise` | Three near-misses, one real discrepancy | **False positives.** Can it separate signal from approximation? |
| `05-sandhu-messy` | Poor scan, unsigned draft, misfiled document | Document validity. Does it know a draft is not an agreement? |

## Why these five

A system that always returns flags is worse than no system, because the lawyer
stops reading them. Fixture 01 is the only one that tests finding things.
The other four test restraint, which is harder and matters more.
