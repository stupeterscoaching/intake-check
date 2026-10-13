# Test fixtures — FICTIONAL

Five stand-in client files. Nothing here is real: no real person, employer or
firm. Drafted as Ontario, Canada (ROE, ESA) because the capstone notes mention
ROEs — retarget if that is wrong.

Hand any one of these folders to a pipeline. **Answer keys live in a separate
tree** at `../fixture-keys/` so a fixture can be handed over without leaking
what it should find.

| Folder | Client | Shape | What it tests |
|---|---|---|---|
| `okonkwo-dale-2026-09` | Dale Okonkwo | Well documented, five real discrepancies | Recall. Does it find them all? |
| `whitfield-marguerite-2026-10` | Marguerite Whitfield | Well documented, nothing wrong | **Silence.** Does it invent flags when there are none? |
| `arteaga-tomas-2026-10` | Tomás Arteaga | Barely any documents | Absence is not disagreement. Does it say "cannot be verified" rather than inventing a conflict? |
| `benoit-nadine-2026-10` | Nadine Benoit | Three near-misses, one real discrepancy | **False positives.** Can it separate signal from approximation? |
| `sandhu-harpreet-2026-10` | Harpreet Sandhu | Poor scan, unsigned draft, misfiled document | Document validity. Does it know a draft is not an agreement? |

Folders are named the way real client folders would be, deliberately. The old
names said which one was clean and which was messy, which gives the answer away
to anyone reading the directory — including anyone you are showing it to.

## Why these five

A system that always returns flags is worse than no system, because the lawyer
stops reading them. Fixture 01 is the only one that tests finding things.
The other four test restraint, which is harder and matters more.
