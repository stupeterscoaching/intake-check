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

### Google Drive

| | |
|---|---|
| Sees structure | ?? |
| Reads contents | ?? **The unknown.** Drive stores `.md` as plain text; the connector indexes Google Docs natively. |
| Account needed | ?? |
| Install needed | ?? |
| How they point at it | ?? |
| Read-only sharing | ?? |
| Sharing model | Explicit grant to a Google account. A public link is **not** expected to surface in another user's connector — it is not in their Drive until they add a shortcut. ?? Confirm. |
| Setup cost | ?? |

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

?? Write the conclusion here once all three are in.

The likely shape: GitHub works best technically and is unusable by the actual
receiver. Which would make "which store fits" a question about the user, not
about the technology.
