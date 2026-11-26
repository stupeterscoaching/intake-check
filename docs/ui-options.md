# UI options — GitHub, Google, EdubaWare

2026-10-13 · Can a UI be built on top of each stack, so legal admin can see every
client's stage, read a client's flags, and ideally ask a question? Researched on the
public web. The 29 claims a decision would rest on were each re-checked against their
source: **0 refuted, 17 corrected.** Evidence is in
[ui-options-claims.md](ui-options-claims.md).

## Short answer

- **GitHub and Google: yes.** Both let an outside program list folders and read files
  through documented, permitted APIs. Because state here is "which output files exist",
  that is all a status board and a flag reader need.
- **EdubaWare: you can build *in* it, not *on* it.**
  - There's no documented API or SDK, and `chat.eduba.io` refuses to be embedded by
    other sites.
  - The MCP's known tools manage templates, not the workbench files where stage
    outputs live.
  - The Terms bar the workarounds: automated access, scraping, framing.
  - The one UI you can add today is an HTML page the agent writes into a workbench.
    It runs inside the file viewer, but it's a snapshot.
  - An end-user dashboard and a white-label UI are Jake's stated plans, with no date.
- **For legal admin, use Google.** A firm-owned Sheet shows every client's stage and
  links to their flags, with nothing new to learn.

## Four layers

The capstone already frames work as **instructions / runner / state**. A UI adds a
fourth layer.

| Layer | What it is | In `intake-check` |
|---|---|---|
| **Instructions** | The method, the same for every client | `CLAUDE.md`, `CONTEXT.md`, `stages/`, `shared/` |
| **State** | The client's material and what the stages produced | Each client folder, including `output/` |
| **Runner** | Whatever runs an instruction against state with a model | You in Claude Code. **It has never run.** |
| **UI** | A view of state, plus optionally a door into a runner | Doesn't exist yet |

Instructions and state don't need the same store, and for a law firm they shouldn't.
Keep the method in GitHub and the client state in the firm's Drive.

**What a UI needs from each part:**

- **Seeing each client's stage (a)** takes one directory listing per client.
- **Reading a flag list (b)** takes one file read.
- **Asking a question (c) is a model call over client files, not a display feature.**
  That makes it a small runner, so the confidentiality decision applies to it too.

**The test for any stack:** does it let an outside program list and read the state
through a documented, permitted route?

| Stack | Passes? | How |
|---|---|---|
| GitHub | Yes | Contents and Trees APIs, with a GitHub App token |
| Google | Yes | DriveApp or the Drive API, from Apps Script inside the firm's domain |
| EdubaWare | No | There's no public way to read workbench files. The MCP only writes instructions in. |

## By stack

### GitHub

| | |
|---|---|
| Best UI | A small app that reads the repo server-side with a **GitHub App** token. Read access to Contents only, for this one repo. Tokens expire after an hour, and the App takes no seat. For this receiver, host it as an Apps Script web app, so it opens behind their Google login anyway. |
| Ruled out | **github.com:** every viewer needs a GitHub account. **Pages:** Free can't publish from a private repo. On Pro and Team the site is **public on the internet** even when the repo is private. Only Enterprise Cloud can publish privately, and then only to people with repo access. |
| Runs the pipeline? | **Yes, and it's the strongest runner**, because Actions runs Claude Code itself. Two catches: |
| | - The Claude Code action **doesn't run on push**. It errors with `Unsupported event type: push`, although Anthropic's docs say "any GitHub event". It does run on a schedule, on manual dispatch and on issue events. |
| | - Commits a workflow makes don't trigger further workflows. Chain stages by dispatching each one explicitly, or run them all in one job. |
| Confidentiality | Fine for instructions and fixtures. Wrong for real client state: |
| | - Anyone with read access sees every client and every run log, and logs are kept for 90 days by default. |
| | - Files are checked out onto GitHub's machines. |
| | - The default Claude GitHub App asks for broad write permissions. |
| Effort | The highest for this receiver: two systems to secure, plus a Drive copy to keep in sync. |
| **Verdict** | **The home of the method, and the runner for fixture runs. Neither the receiver's UI nor the store for real client files.** |

### Google Workspace

| | |
|---|---|
| Best UI | **A firm-owned Google Sheet with a bound Apps Script.** One row per client: stage (worked out from which output files exist), last change, and a link to the flags. Later, add an HTML sidebar with "Ask about this client" and "Run next stage". |
| End user needs | Their existing firm Google login and view access to the Sheet. No new tool, no new account. |
| Runs the pipeline? | **Plausibly, but untested, and not the way Claude Code runs it.** |
| | - Apps Script can POST to the Messages API, so a stage becomes **one fixed model call**: the stage contract, its references, earlier outputs and the client docs in one request. It isn't Claude Code's tool loop. |
| | - Each run is capped at **6 minutes**, with no streaming. |
| | - The explicit Inputs tables in the stage contracts are what make this possible. The script has to gather each stage's inputs itself. |
| Confidentiality | **The best of the three.** Drive, Sheets and Apps Script are Core Services under the firm's existing Workspace agreement, Drive sharing decides who sees what, and Apps Script actions appear in the audit log. The one deliberate exit is the model call, and the firm picks who processes it: Anthropic's API, or Claude on Google Cloud. |
| **Must be built inside the firm's domain** | An app owned by a firm account and used only inside the firm is **internal**: no OAuth verification, no security assessment, no user cap. Built from your gmail, it's **external**. Users then see an unverified-app screen, the app is capped at 100 users for life, and it needs yearly verification plus a CASA security assessment. **Either the firm deploys it, or the firm gives you an account in its domain.** |
| Effort | The lowest: a Sheet and a few hundred lines of Apps Script. No hosting, no separate secrets server. |
| **Verdict** | **Fits the receiver. Drive is the store for client state, and a Sheet is the UI.** |

### EdubaWare

| | |
|---|---|
| Best UI | Its own workbench UI: a folder tree, rendered markdown and a shared chat. The only way to add one is to have the agent write a `dashboard.html`, which runs in the file viewer as a working page. It's a snapshot someone has to ask the agent to rebuild. |
| End user needs | An Eduba login, tied to a Clief Notes Skool membership ("use the same email as your Skool account") and an email invite. **Whether anyone outside Clief Notes can get in at all is unknown.** |
| Runs the pipeline? | Yes, in place: Claude Code on Sonnet in each workbench's container. But only when someone types in chat. There's no schedule, webhook or API. |
| Confidentiality | **Ruled out for real client material, with no approval route.** The non-confidential warranty in s.2 is unconditional, and the s.27 written-agreement exception covers regulated data only. |
| **Verdict** | **A demo venue for fictional data, among community members.** |

## Two traps the layering exposes

**1. File-existence state can't see the review gates.** It can't tell "`03-differences.md`
was written" from "03 was reviewed and is ready for 04". Any automatic runner that does
"run the next missing stage" (an Actions cron, an Apps Script timer) **silently removes
every review gate.** There are two ways out:

- A person starts each stage from the UI, so the UI *is* the gate. This keeps "no tracker".
- The gate gets written into state, for example as a marker file. That changes the
  "no tracker" decision.

**2. The never-answer rule only binds a runner that reads it.** Today the
question route (c) is the receiver's own Claude with the Drive connector, which is what
the external tester used. **Nothing makes that session read `CLAUDE.md`, so the rule isn't
enforced there.** That's the real argument for eventually building "Ask about this
client" yourself: a sidebar that sends `shared/output-shape.md` as its system prompt.
The rule lives in the instructions, and it travels with them only if the runner loads them.

## The cheapest prototype

An intake board in a Google Sheet, over the five fixtures. About three hours, in chunks
that can stop and start.

1. **Run the pipeline in Claude Code (60–90 min).** It has never run, so every row would
   read "not started".
   - Take `whitfield-marguerite-2026-10` to stage 05. The right answer is one line.
   - Take `okonkwo-dale-2026-09` to stage 05.
   - Stop `benoit-nadine-2026-10` after stage 03, so the board shows a mix.
   - Keep an untouched copy of the fixtures for the cold baseline.
2. **Copy to Drive without `fixture-keys/` (15 min).** Today's Drive copy includes the
   keys.
3. **Build the Sheet (about 60 min).**
   - Extensions → Apps Script, roughly 80 lines.
   - `refresh()` walks each client's `output/` folder and writes one row per client:
     the stage, last modified, and a link to `05-pre-consult-flags.md`.
   - Add an Intake → Refresh menu.
   - Pin the Drive scope to `drive.readonly` so the board can't change client files.
4. **Test it with the external tester (15 min).** Share the Sheet with them, view only. From the
   Sheet alone, they should be able to answer: which client is at which stage, and what
   does Whitfield's flag list say?

Stretch goals, fixtures only: an "Ask about this client" sidebar carrying
`shared/output-shape.md`, and a "Run stage 05" menu item to test whether Apps Script can
be the runner.

Left out: a GitHub App (a day of work, not a few hours), and EdubaWare (you'd have to drive
it by hand, and it can't serve this receiver).

## Open

- **The firm (binding):** can client material go to a model at all, and through which
  processor? Until then, the runner and the question box stay on fixtures.
- **The firm:** who owns the build? That decides internal or external.
- **The firm's admin:** which Workspace edition is the firm on? Is Apps Script enabled
  for admin staff? Is Drive API access restricted?
- **You and the lawyer:** which review gates stay human?
- Does a stage fit inside 6 minutes on real-sized documents? Stage 02 is the stress test,
  and 17 KB of fixtures can't answer it.
- Real documents arrive as PDFs, Word files and scans. A one-call-per-stage runner has no
  tools to convert them. Should conversion be its own stage?
- What does a five-stage run cost per client in tokens? The Business room will ask.
