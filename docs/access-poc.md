# Access PoC — how users reach a workspace

How a non-technical user gets a Claude session pointed at this workspace, across
three stacks. Fill in as each is tested.

## What matters

| Dimension | Why |
|---|---|
| Sees structure | Can it list folders and files without being told what's there |
| Reads contents | Can it open a `.md` and use what's inside, or only see filenames |
| User needs an account | Legal admin will not create a GitHub account |
| User needs an install | Anything requiring a terminal is out |
| How they point at it | URL, path, connector picker, something else |
| Read-only sharing | Can one person be given read access without edit rights |
| Sharing model | Explicit grant to a named account, or link-based. A firm will never link-share client folders, so explicit grant is the realistic path. |
| Setup cost | Who has to do what, once |

## Results

### GitHub

| | |
|---|---|
| Sees structure | ✅ Listed all five client folders and the file tree from the repo path alone |
| Reads contents | ✅ Read the README and built a table from the intake forms |
| Account needed | Yes — and `gh` was already authed as the repo owner |
| Install needed | GitHub CLI or the GitHub connector |
| How they point at it | `github.com/owner/repo/path` |
| Read-only sharing | Yes, collaborator with read permission |
| Sharing model | Explicit grant, per GitHub account |
| Setup cost | Low for a developer. **Not viable for legal admin.** |

Notes: answered from structure rather than reading everything. Respected the
`fixture-keys/` boundary without being told.

**Sharing note, 2026-10-13.** GitHub gives collaborators on a personal repo
**write** access; read-only requires an organisation-owned repo. Invitations must
be accepted before access works, and until then the repo 404s.

### Three different Drive mechanisms — do not confuse them

They behave differently and only one of them is what a receiver would use.

| Mechanism | How it reaches Drive | Needs | Status |
|---|---|---|---|
| **Drive connector** | Authenticates as the user, searches their own Drive and Shared with me | Connector enabled in the session | **Untested. This is the one that matters.** |
| **Browser pane** | Opens drive.google.com as a web page and reads the rendered UI | That browser signed in to Google | Tested 2026-10-13. **Failed** — private folder redirected to sign-in. |
| **Fetch a public link** | HTTP GET on a shared URL | Folder set to anyone-with-link | Not tested. Rejected: a firm will not link-share client folders. |

The browser-pane failure is not a finding about Drive. It is a finding about
browsers: a private folder needs an authenticated session, and a chat agent
cannot and should not sign in on the user's behalf.

A legal admin would never browse to the folder. They would have the connector
and ask a question. **Test that.**

### Google Drive — connector

Tested 2026-10-13.

| | |
|---|---|
| Sees structure | ✅ Found the folder and listed all five client folders |
| Reads contents | ✅ **The unknown is answered.** Read plain `.md` and quoted from it — "they just put me on the trucks", "six years, maybe seven". Not just filenames. |
| Account needed | Google account, which the receiver already has |
| Install needed | None. Connector enabled in the session. |
| How they point at it | They don't. The connector searches their Drive. |
| Read-only sharing | Yes, standard Drive sharing |
| Sharing model | Explicit grant to a named account ✅ |
| Setup cost | **Low, and viable for legal admin** — the thing GitHub fails |

Substantively it did well: identified the missing contract, ROE, pay history
and notice information, and framed them as missing information rather than
discrepancies. Declined to open `fixture-keys/` again, unprompted — second
stack, same behaviour.

**External user test, 2026-10-13 — passed.** DavidTMark, with the folder shared
to his Google account, queried it from his own Claude session through the Drive
connector. Listed all five clients correctly, with folder and month. He had no
GitHub access at the time (invite sent minutes earlier, not yet accepted), so
this is a Drive-only result. ?? Confirm his session had no GitHub connector.

- Worked across languages: English files, Swedish user, answer in Swedish.
- Names were taken from folder names, so "Tomás" came back as "Tomas" — folder
  names are an index, not the record. The session said so unprompted: it had not
  opened `intake-form.md` to check spelling.
- Saw `fixture-keys/`, guessed it was the answer key from the name, did not open
  it. Third session, same restraint. Keys are visible because the whole workspace
  was dragged into Drive; a blind test needs them kept out of the shared folder.

This likely clears the caveat below: an external user, on Drive alone, got the
right answer.

**Caveat on this run.** It said: *"I checked his folder in Drive; the other
clients' counts come from the GitHub copy."* Both stacks were reachable in the
same session and it mixed them. Drive reading `.md` is proven; Drive answering
the whole question alone is not. ?? Re-run in a session with Drive only.

**Second finding.** It knew what Arteaga's fixture was for. That was not a leak
— nothing outside `fixture-keys/` states it. It inferred the test design from
`shared/source-reliability.md` plus a thin folder. The rules are clear enough to
be reverse-engineered, which is a compliment to the rules and a problem for
blind evaluation. **For a blind eval the fixtures need separating from the
workspace, not just from the keys.** For a demo this is fine.

### EdubaWare

| | |
|---|---|
| | ?? Not yet tested |

## The test

Same question to every stack, so the answers are comparable:

> What are the names of all the clients in our current files?

Then, to see whether it read contents or only filenames:

> Which client has the fewest documents, and what are they missing?

## Finding so far

Both stacks work technically. Both read structure, both read `.md` contents,
both respected the keys boundary without being told.

The difference is the user. GitHub needs an account and a mental model of
repositories; legal admin has neither and will not acquire them. Drive needs
nothing — it is already open on their second monitor.

**"Which store fits" turned out to be a question about the receiver, not the
technology.** The prediction held. ?? EdubaWare still to test.
