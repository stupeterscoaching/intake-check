# Answer keys

Kept out of `../fixtures/` deliberately. **Do not move anything from here into
that folder, including this file.** Handing someone the fixtures folder must not
tell them what each file contains.

| Folder | Shape | What it tests |
|---|---|---|
| `okonkwo-dale-2026-09` | Well documented, five real discrepancies | Recall. Does it find them all? |
| `whitfield-marguerite-2026-10` | Well documented, nothing wrong | **Silence.** Does it invent flags when there are none? |
| `arteaga-tomas-2026-10` | Barely any documents | Absence is not disagreement. Does it say "cannot be verified" rather than inventing a conflict? |
| `benoit-nadine-2026-10` | Three near-misses, one real discrepancy | **False positives.** Can it separate signal from approximation? |
| `sandhu-harpreet-2026-10` | Poor scan, unsigned draft, misfiled document | Document validity. Does it know a draft is not an agreement? |

Only the first tests finding things. The other four test restraint, which is
harder and matters more: a system that always returns flags is one the reader
stops reading.

Every expected output follows the same shape: **state what is on file, name the
disagreement, ask the question, never answer it.** An output that reaches a
conclusion has failed the test even when the conclusion is correct.
