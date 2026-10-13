# UI options — verified claims

2026-10-13 · From the `ui-on-stacks` research workflow (33 agents, public web only).

Each research agent proposed its most load-bearing claims. Each claim was re-checked
against its own source by a separate skeptic told to refute it. **29 checked: 0 refuted,
17 corrected, 12 held.** Where a claim was corrected, the corrected wording is what counts.

Basis: **stated** = the source says it · **demonstrated** = shown working · **inferred** =
a reading between the lines.

## GitHub

### G1 — CORRECTED

**Claim** [stated]: GitHub Pages can publish from a private repository only on GitHub Pro, GitHub Team, GitHub Enterprise Cloud or GitHub Enterprise Server; GitHub Free and GitHub Free for organizations allow public repos only. GitHub warns that the published site is publicly available on the internet even when the repository is private, and says Pages shouldn't be used for sensitive transactions.

**Source:** https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

**Corrected:** GitHub Pages can publish from a private repository only on GitHub Pro, GitHub Team, GitHub Enterprise Cloud or GitHub Enterprise Server. On GitHub Free and GitHub Free for organizations, the repository must be public. On Free/Pro/Team, GitHub warns that the site is publicly available on the internet even when the repository is private. That doesn't hold on every plan.

- **GitHub Enterprise Cloud:** sites are public only by default. An organization can publish a project site from a private or internal repository privately, so only people with read access to that repository can view it. Organization sites can't be made private. Enterprises using Enterprise Managed Users can only publish privately.
- **GitHub Enterprise Server:** a site is public on the internet only if the site administrator has turned on Public Pages.

GitHub also says Pages sites shouldn't be used for sensitive transactions like sending passwords or credit card numbers.

### G2 — held

**Claim** [stated]: Restricting who can see a Pages site ('publishing privately') requires the organization to use GitHub Enterprise Cloud, applies only to organization-owned project sites built from private or internal repos, and limits the site to people with read access to the source repository. Under Enterprise Managed Users, all Pages sites are private and visible only to enterprise members.

**Source:** https://docs.github.com/en/enterprise-cloud@latest/pages/getting-started-with-github-pages/changing-the-visibility-of-your-github-pages-site

### G3 — held

**Claim** [stated]: A server can read the private repo with no end-user GitHub identity by authenticating as a GitHub App installation. GitHub recommends a GitHub App over a personal access token for organization or long-lived integrations. An App acts independently of any user and consumes no seat. Each installation access token can be limited to specific repositories and permissions (reading files needs only 'Contents' read) and expires after 1 hour.

**Source:** https://docs.github.com/en/apps/creating-github-apps/about-creating-github-apps/deciding-when-to-build-a-github-app

### G4 — CORRECTED

**Claim** [stated]: Google Apps Script can host that server inside the firm's Google Workspace. A web app can be restricted with access=DOMAIN ('Only users in the same domain as the deployer can run it') and set to executeAs=USER_DEPLOYING ('The web app runs as the user who deployed it'). Google Workspace accounts get 100,000 URL Fetch calls/day and a 6-minute limit per script execution.

**Source:** https://developers.google.com/apps-script/manifest/web-app-api-executable

**Corrected:** Google Apps Script can host that server as a web app. A script with a doGet or doPost function that returns HtmlOutput or TextOutput can be deployed and reached at a URL (Web Apps guide, developers.google.com/apps-script/guides/web; the manifest page only lists the deployment settings). In the manifest, access=DOMAIN means 'Only users in the same domain as the deployer can run it', and executeAs=USER_DEPLOYING means 'The web app runs as the user who deployed it'. The quotas page gives Google Workspace accounts 100,000 URL Fetch calls/day (consumer accounts: 20,000) and both kinds of account a 'Script runtime' of '6 min / execution'. Three caveats from the same page: (1) 'Quotas are per user'. With USER_DEPLOYING, the script 'always executes as you ... no matter who accesses the web app' (Web Apps guide), so all firm users share the deploying account's one 100,000/day allowance. That last step is my inference from the two pages. (2) 'Additional limits apply for trial accounts.' After a trial converts to paid, the limits rise only once the domain has paid at least USD 100 in total and 60 days have passed since then. (3) Every quota and limit 'is subject to elimination, reduction, or change at any time, without notice.' Two points remain inferences: that this keeps the GitHub key off the client, and that a firm-domain account must deploy the app. The Web Apps guide supports the second: web apps 'cease to function if their ownership changes to a shared drive or account in a different domain.'

### G5 — held

**Claim** [stated]: Anthropic's Claude Code GitHub Action (v1) runs in automation mode (a prompt input) on schedule, workflow_dispatch, repository_dispatch and workflow_run events, plus issue and PR events, but not on push: push-triggered workflows exit at startup with 'Unsupported event type: push'. The bug report is still open, and the event list is unchanged in the latest release, v1.0.248 (2026-10-09). Anthropic's docs page says the opposite: that it runs 'on any GitHub event'.

**Source:** https://github.com/anthropics/claude-code-action/issues/1456

### G6 — held

**Claim** [stated]: Events caused by a workflow's GITHUB_TOKEN, including the push of a commit it makes, do not start new workflow runs. The exceptions are workflow_dispatch and repository_dispatch (which always run) and some pull_request events (created in an approval-required state).

**Source:** https://docs.github.com/en/actions/concepts/security/github_token

### G7 — held

**Claim** [stated]: By default the action authenticates to GitHub as Anthropic's Claude GitHub App, and installing that App grants its whole permission set on the repo, not just what the action uses. That set includes read and write on Contents, Actions, Workflows, Checks, Discussions, Issues, Pull requests and Repository hooks, and read on Administration, Members, Merge queues, Metadata and Statuses. GitHub doesn't let you accept a subset; the documented alternatives are a custom GitHub App or passing your own github_token.

**Source:** https://code.claude.com/docs/en/github-actions

### G8 — CORRECTED

**Claim** [stated]: Workflow run logs can be viewed, searched and downloaded by anyone with read access to the repository, and are kept 90 days by default (configurable from 1 to 400 days for private repos). The action's show_full_output input is off by default, but if enabled (or auto-enabled when ACTIONS_STEP_DEBUG is true) it writes all Claude messages into those logs, including tool outputs and file contents.

**Source:** https://docs.github.com/en/actions/how-tos/monitor-workflows/use-workflow-run-logs

**Corrected:** Workflow run logs can be viewed, searched and downloaded by anyone with read access to the repository. GitHub says read access is required, and you must be signed in to GitHub even for public repos, so for a public repo that means any signed-in user. Logs are kept 90 days by default. That can be changed to 1–400 days for private repos (1–90 for public), within any limit the org or enterprise sets, and anyone with write access can delete logs sooner. The action's show_full_output input defaults to "false". When it is "true", every Claude message is written to those logs as JSON, including tool outputs and file contents. The action's security doc also says full output turns on automatically in debug mode (when the ACTIONS_STEP_DEBUG secret is true). In practice it does not. The code only checks process.env.ACTIONS_STEP_DEBUG === "true", and the GitHub runner never passes that name into a step's environment. Setting the secret or variable, or re-running with debug logging, only sets RUNNER_DEBUG=1. Open issue #1604 (filed 2026-08-05, not fixed on main) reproduces this. So today full output is on only when show_full_output is true, or when the workflow itself sets an ACTIONS_STEP_DEBUG=true env var for the step. Treat debug mode as unsafe anyway: the documented behaviour, and the proposed fix (also check RUNNER_DEBUG), would make it log everything.

### G9 — CORRECTED

**Claim** [stated]: For private repositories, included GitHub-hosted runner minutes per month are 2,000 (GitHub Free, GitHub Free for organizations), 3,000 (GitHub Pro, GitHub Team) and 50,000 (GitHub Enterprise Cloud). Beyond that, Linux 2-core minutes cost $0.006 each, self-hosted runners are free, and minutes bill to the repository owner. Claude API tokens are billed separately by Anthropic.

**Source:** https://docs.github.com/en/billing/concepts/product-billing/github-actions

**Corrected:** For private repositories, the included minutes per month on standard GitHub-hosted runners are 2,000 (GitHub Free, GitHub Free for organizations), 3,000 (GitHub Pro, GitHub Team) and 50,000 (GitHub Enterprise Cloud). Larger runners are always charged, even with quota left. Beyond the quota, Linux 2-core (x64) minutes cost $0.006 each (Linux 2-core arm64 costs $0.005). That applies only with a payment method on file; without one, usage is blocked. Self-hosted runners are free. Minutes bill to the repository owner. Model usage is separate from GitHub minutes, and who bills it depends on authentication. With an API key, Anthropic bills Claude API tokens. With a Claude subscription OAuth token (Pro, Max, Team or Enterprise), runs use the subscription instead of API billing. Inference routed through Amazon Bedrock, Google Cloud's Agent Platform or Microsoft Foundry goes through that cloud account.

### G10 — held

**Claim** [stated]: GitHub's own UI only works for GitHub users with repository access. On GitHub Team and GitHub Enterprise Cloud, each outside collaborator on a private repository is billed as a seat. Asking Claude inside GitHub (an @claude issue comment) also requires write access on issue events, unless the builder sets allowed_non_write_users and passes their own github_token.

**Source:** https://docs.github.com/en/billing/reference/github-license-users

## Google Drive / Workspace

### W1 — CORRECTED

**Claim** [stated]: Who can open an Apps Script web app, and whose access it runs with, is set by two deployment settings. executeAs is USER_DEPLOYING or USER_ACCESSING. access is MYSELF, DOMAIN, ANYONE or ANYONE_ANONYMOUS. DOMAIN limits use to users in the deployer's Workspace domain. USER_ACCESSING makes each user go through Google's consent screen and runs the app with that user's own Drive permissions.

**Source:** https://developers.google.com/apps-script/manifest/web-app-api-executable

**Corrected:** Two web app settings, `access` and `executeAs`, control who can run an Apps Script web app and whose identity it runs under. They are chosen in the deployment dialog and stored in the manifest's `webapp` object. executeAs is USER_DEPLOYING (runs as whoever deployed it, which is not necessarily the script owner) or USER_ACCESSING (runs as the user accessing it). access is MYSELF (only the deployer), DOMAIN (only users in the same domain as the deployer, which in practice means the deployer's Google Workspace domain), ANYONE (any logged-in user) or ANYONE_ANONYMOUS (any user, even if not logged in). The rest comes from the Web Apps guide, not the manifest page. With USER_ACCESSING, each user sees Google's granular OAuth consent screen when they first authorize the app. The script then runs under that user's identity, so it can reach only the Drive files that user can reach. It is further limited to the scopes the user chooses to grant, because individual scopes can be refused, and Google recommends checking with ScriptApp.getAuthorizationInfo. Apps Script also limits how fast new users can authorize a web app that runs as the user. Those limits depend partly on whether the publishing account is in a Google Workspace domain.

### W2 — CORRECTED

**Claim** [stated]: The Drive scopes needed to list or read any client folder are 'restricted': drive, drive.readonly, drive.metadata, drive.metadata.readonly, drive.activity, drive.activity.readonly, drive.meet.readonly and drive.scripts. Only drive.file, drive.appdata and drive.install are non-sensitive. Apps Script's DriveApp folder methods need drive.readonly or drive.

**Source:** https://developers.google.com/workspace/drive/api/guides/api-specific-auth

**Corrected:** Google's Drive API scopes page (last updated 2026-09-03) classes eight Drive scopes as restricted: drive, drive.readonly, drive.activity, drive.activity.readonly, drive.meet.readonly, drive.metadata, drive.metadata.readonly and drive.scripts. drive.apps.readonly is sensitive. The non-sensitive scopes are drive.file, drive.appdata/drive.appfolder (two scope strings listed in one row) and drive.install.

Not all eight restricted scopes give access to a client folder:
- drive and drive.readonly can list and read any file.
- drive.metadata and drive.metadata.readonly can list folders and show metadata, but not file content.
- drive.activity, drive.activity.readonly, drive.meet.readonly (Meet-created files only) and drive.scripts give no general folder access.

The page never says that listing or reading a client folder needs a restricted scope; that is an inference. Under drive.file, an app reaches only files it creates, files the user opens with it, or files the user picks in the Google Picker. Nothing official says that picking a folder gives access to what is inside it, and developer reports say it does not. So in practice, listing the contents of an existing client folder needs drive, drive.readonly or a metadata scope, and all of those are restricted. Files a user picks one by one can still be read with the non-sensitive drive.file scope.

In Apps Script, the DriveApp and Folder methods that read or list (getFolderById, getFolders, getFoldersByName, searchFolders, getFiles, getFilesByName and others) need drive.readonly or drive. Methods that write, such as createFolder and createFile, need drive. DriveApp cannot reach shared drives; the advanced Drive service is needed for that.

### W3 — held

**Claim** [stated]: Internal apps need no OAuth verification and are exempt from the restricted-scope requirements, including the security assessment. An app is internal when its Cloud project is owned by the firm's organisation and its consent screen is set to Internal. An Apps Script project is internal automatically when its owner uses a Workspace account and only people in that owner's domain use it. If the firm has restricted Drive API access, its admin may still have to trust internal apps.

**Source:** https://support.google.com/cloud/answer/13464323

### W4 — CORRECTED

**Claim** [stated]: An app used outside its owner's domain (External) that uses restricted Drive scopes faces the heavy path. Unverified, it shows users an unverified-app screen and is capped at 100 new users for the project's lifetime. It needs restricted-scope verification, plus a CASA security assessment, renewed every year, if it stores or transmits restricted-scope data on servers. A Workspace admin can lift this for their own users by marking the app trusted.

**Source:** https://support.google.com/cloud/answer/13465431

**Corrected:** An External app (open to any Google Account) that requests restricted Drive scopes (drive, drive.readonly, drive.metadata and others) faces the heavy path. Until those scopes are verified, users see the unverified-app screen and the project can take only 100 new users in total. That cap lasts the project's whole lifetime and cannot be reset, though Google says it may adjust it per app. To go past it, the app needs restricted-scope verification, redone every year, plus a CASA security assessment from a Google-approved assessor, redone at least every 12 months. Google's developer guides require the assessment when the app can access, store or transmit restricted data from or through a server, which any hosted backend does. Its help-center pages, including the cited one, say every restricted-scope app needs it. A Workspace admin can add the app to their org's trusted list. That org's users can then install it whether or not it is verified, Google treats it as internal for that org, and the help center lists admin-trusted apps as exempt from mandatory verification. This covers only that org's users. Google calls trusting an unverified external app "generally discouraged", and its restricted-scope guide says apps that rely on domain-wide installation and use restricted or sensitive scopes still need verification. Treat the admin route as a workaround for one client at a time, not a way around verification. Cite 13465431 only for the CASA and yearly-renewal part. The rest comes from 13463817, 15549945 and 13464323, the Drive scopes guide, and the restricted-scope-verification and production-readiness overview guides on developers.google.com.

### W5 — CORRECTED

**Claim** [stated]: These Apps Script limits shape a five-stage pipeline on Workspace accounts. Each execution may run 6 min. Custom functions get 30 s, and so does each Google Workspace add-on execution. Total trigger runtime is 6 hr/day (90 min on consumer accounts). URL Fetch allows 100,000 calls/day, 50 MB per POST or response, and 30 simultaneous executions per user. UrlFetchApp waits 360 s by default. Breaking a limit throws an error and stops the execution, and Google may change any of these without notice.

**Source:** https://developers.google.com/apps-script/guides/services/quotas

**Corrected:** These Apps Script limits constrain a five-stage pipeline on Workspace accounts. Each script execution can run for up to 6 min. Custom functions get 30 s per execution. Google Workspace add-on executions also get 30 s, except add-ons that extend Workspace Studio (a Gemini Alpha program), which get 2 min. Total trigger runtime is 6 hr/day per user (90 min on consumer accounts). URL Fetch allows 100,000 calls/day per user, and 50 MB per POST and per response. Quotas reset 24 hours after the first request. The 30-simultaneous-executions limit is not a URL Fetch limit. It is a general cap: one user can have at most 30 script executions running at once, across all their scripts, and a single script can have at most 1,000. The Workspace-tier figures are not guaranteed on new accounts. Trial accounts have extra limits, and after a trial converts to paid, the higher limits apply only once the domain has paid at least US$100 in total and 60 days have passed since reaching that amount. Per the UrlFetchApp reference page (not the quotas page), timeoutSeconds defaults to 360 s. Going over a quota or limit makes the script throw an exception and stop. Google says all quotas and limits may be eliminated, reduced or changed at any time without notice.

### W6 — CORRECTED

**Claim** [inferred]: Apps Script can run the pipeline, not just store and display it. UrlFetchApp can make the authenticated HTTPS POST that the Claude Messages API needs. Because of the 6-minute ceiling and the lack of documented streaming, the workable design is one stage per execution, chained by a time-driven trigger that checks which output files exist. That keeps ICM's 'state = files' but replaces Claude Code's agent loop with a fixed, script-driven call per stage.

**Source:** https://developers.google.com/apps-script/reference/url-fetch/url-fetch-app

**Corrected:** Apps Script can plausibly run the pipeline as well as store and display it. This is inferred from the docs, and nothing has been run. UrlFetchApp.fetch accepts method 'post', a headers map, a JSON payload and contentType. That covers everything POST https://api.anthropic.com/v1/messages requires: Authorization: Bearer <key> (or the legacy x-api-key), anthropic-version, and content-type: application/json. It needs the script.external_request scope, and its timeoutSeconds parameter defaults to 360 seconds. UrlFetchApp returns only complete responses, with no documented streaming. Every execution is capped at 6 minutes on both consumer and Workspace accounts; that limit comes from the quotas page, not the cited page.

So one synchronous Messages call per stage, per execution, chained by a time-driven trigger that checks which output files exist, is A workable design. It works only for stages whose call reliably finishes well inside 6 minutes, including the Drive reads and writes. Set timeoutSeconds below 360 to leave room for those.

It is not THE only design. Claude's Long-requests guidance names the Message Batches API, which lets a client poll for results instead of holding a connection open. A stage can be submitted in one trigger run and collected in a later one. Most batches finish within an hour, they expire at 24 hours, and they cost 50% less. That takes model latency out of the 6-minute window, at the cost of turnaround time.

The trigger also needs LockService or an in-progress marker. Up to 30 executions per user can run at once, so an every-minute trigger can start the same stage again while the previous run is still going. Every-minute triggers are also unavailable if this ships as a Workspace add-on, which is limited to one time-driven run per hour.

Throughput: the 6 hr/day of total trigger runtime applies only to Google Workspace accounts, and trial accounts get extra limits. Consumer gmail.com accounts get 90 min/day. In the worst case that is 15 six-minute stage runs a day, or 3 five-stage clients, not 60 and 12. The no-op polling runs count against the same quota, so 60 is a ceiling even on Workspace, not a floor.

### W7 — CORRECTED

**Claim** [stated]: A Workspace add-on can be published privately to the firm. A private listing is visible only inside the organisation, goes live immediately and skips Google's app review. Publishing needs a standard Cloud project. The interface is built from cards, Drive add-ons do not run on mobile, each add-on execution gets 30 s, and an add-on's scheduled trigger fires at most once an hour. So an add-on can show stage and flags but cannot host the stage runs.

**Source:** https://developers.google.com/workspace/marketplace/how-to-publish

**Corrected:** A Google Workspace add-on can be published privately, but only to the Workspace organisation of the account that builds and publishes it. To reach the firm, it has to be published from an account inside the firm's own Workspace domain. A private listing is available only to users in that organisation and also appears in the Marketplace's Internal Apps section. It is available immediately, and Google does not review it; public apps are reviewed. Allowlists and install settings still decide who can install it. Publishing an Apps Script add-on needs a standard Cloud project, not the default one. The UI is built from cards, and Drive add-ons can't run on mobile clients yet. For Apps Script add-ons, the Card service limits callback functions to 30 s (the quota table lists 'Google Workspace add-on runtime 30 sec / execution'). A time-driven trigger in an add-on can run at most once an hour. The docs tie the 30 s limit to card callbacks; they do not say trigger runs stop at 30 s, and the general Apps Script script runtime is 6 min per execution. So an Apps Script add-on suits showing stage and flags, not running multi-minute stage runs inside it. That is an inference, and it does not hold for Drive add-ons built on HTTP endpoints. Those run on a backend you host, such as Cloud Run, and Google suggests that route for add-ons that need heavy resources.

### W8 — held

**Claim** [stated]: AppSheet Core is included at no cost for domain-verified users in Business Starter, Standard and Plus; Enterprise Starter, Standard and Plus; Enterprise Essentials Plus; Frontline Starter, Standard and Plus; Education Standard and Plus; and Google Workspace for Nonprofits (also Business Base, India only). AppSheet Enterprise Plus costs extra. Google's Workspace Services Summary lists Drive and Apps Script as Core Services and AppSheet under Other Services.

**Source:** https://knowledge.workspace.google.com/admin/appsheet/manage-appsheet-in-your-organization

### W9 — held

**Claim** [stated]: Which company processes the client data depends on how Claude is called. Through api.anthropic.com, Anthropic is the data processor. Its commercial policy deletes API inputs and outputs within 30 days by default, retained data is not used for training without express permission, and zero data retention (ZDR) needs a sales arrangement. Through Claude on Google Cloud's Agent Platform, Google Cloud is the processor, but Message Batches is not available there and requests are capped at 30 MB.

**Source:** https://platform.claude.com/docs/en/manage-claude/api-and-data-retention

### W10 — CORRECTED

**Claim** [inferred]: Keeping storage, screens and orchestration inside the firm's Workspace (Drive, Sheets, Apps Script, a private add-on) adds no new company to the data flow. Drive and Apps Script are Core Services under the firm's existing agreement, Drive sharing controls who sees what, and admins get on/off switches, audit logs and, on Business Plus or Enterprise, an allowlist for outbound URLs. The one deliberate exit is the model call, and the firm chooses the processor: Anthropic directly, or Google Cloud's Agent Platform. A third-party ICM platform holds the files and runs the work too, so it is a processor for both, with its own access model and retention. Gemini in Drive answers questions with no new processor, but it is not the ICM pipeline.

**Source:** https://workspace.google.com/terms/user_features.html

**Corrected:** Keeping storage, screens and orchestration in the firm's Google environment (Drive, Sheets, Apps Script, a private add-on) should add no new company to the data flow. That is an inference, but every piece is run by Google. Drive, Sheets and Apps Script are Core Services covered by the firm's existing Workspace agreement. A private Marketplace add-on also needs a standard Google Cloud project, because the default project can't be used to publish. That project falls under Google Cloud terms, not the Workspace Services Schedule. Drive sharing controls who sees what. Admins get these controls: (a) an Apps Script on/off switch per OU, on all editions; (b) a separate Marketplace install setting, because turning Apps Script off does not stop Marketplace add-ons built with Apps Script; (c) Drive log events, which record Apps Script project actions and log 'URL Accessed' when a script or add-on fetches a URL; (d) an allowlist of the external URLs Apps Script and Sheets may reach, where blocked URLs return an error. The allowlist is only on Frontline Plus, Business Plus, Enterprise Standard and Plus, Education Standard and Plus, and Enterprise Essentials Plus — not every edition with 'Enterprise' in its name. The one deliberate exit is the model call, and the firm chooses the processor: Anthropic directly, or Claude through Google Cloud's Gemini Enterprise Agent Platform (formerly Vertex AI). The Agent Platform is a Google Cloud service under Cloud terms, not a Workspace Core Service. A third-party ICM platform would hold the files and run the work, so it would be a processor for both, with its own access model and retention. That is an inference; no platform's terms were checked. Ask Gemini in Drive answers questions under Gemini in Workspace, which is a Core Service, so it adds no new processor. It is generally available since 22 Apr 2026 on Business Standard and Plus and Enterprise Standard and Plus. It is not the ICM pipeline.

## EdubaWare

### E1 — held

**Claim** [demonstrated]: An HTML file stored in a workbench opens inside EdubaWare's file viewer as a working, interactive page. Scripts evidently run in it.

**Source:** https://www.youtube.com/watch?v=oBgIrK3uOgs&t=50s

### E2 — CORRECTED

**Claim** [demonstrated]: The only public example is built as a snapshot. The agent bakes the data into the HTML. Anything coming back goes by a downloaded file, a manual drop into a stage folder, and a chat prompt that makes the agent rebuild the page.

**Source:** https://www.youtube.com/watch?v=oBgIrK3uOgs&t=44s

**Corrected:** The only public example found of an interactive UI on an EdubaWare workspace is Mark Fitchett's "Clief Pong". It appears in Jake's MCP video at about 0:44–1:05, and the same game shows up in Don's Bookshelf explainer at about 9:00–9:17. It is built as a snapshot. The on-screen ICM agent calls stages/03_game_build/output/pong.html "a complete, self-contained file with all 12 courts baked in … No server", and promises to "rebake" the leaderboard into it (stated). The page itself shows "BUILD 20260815-1300" and baked court records such as "HELD BY Mark · +4 · 6 SHOT" (demonstrated). The video also shows that pong.html opens and plays inside EdubaWare's in-app file preview (0:50–1:05), which has Link in message, share and download buttons. So you do not have to download the page to use it, even though the agent's text says to open it in a browser. According to the agent's on-screen instructions (stated, not demonstrated), results come back like this: click "Download match log (.json)", drop the file in stages/04_match_log/output/, then say "Update scores" so the agent re-aggregates the leaderboard and rebakes pong.html. The video never shows a log being downloaded or dropped, or the agent's reply to "Update scores". That this is the only way data can come back is an inference (inferred). No public source shows a page reading workspace files or messaging the agent, but none says it cannot.

### E3 — CORRECTED

**Claim** [demonstrated]: EdubaWare's MCP server is real, per-org and OAuth-protected. The tools it showed manage templates only: Finish draft push, Get template, List templates, List versions, Push draft, Set default.

**Source:** https://www.youtube.com/watch?v=oBgIrK3uOgs&t=4s

**Corrected:** EdubaWare's MCP server is real, per-org and OAuth-protected. In Jake's video of 2026-08-27 (oBgIrK3uOgs), Claude's Customize > Connectors page for the connected 'EdubaWare' connector (https://mcp.eduba.io/o/019d9e23-8e85-75f3-8597-b904203d80cf/mcp) is on screen from 0:00 to about 0:11, not to 0:13. After a scroll at about 0:07, its only tool group, 'Other tools 6', lists exactly six tools: Finish draft push, Get template, List templates, List versions, Push draft, Set default (demonstrated). At about 1:44–1:52 a Claude chat uses the connector to list the org's live templates (demonstrated).

Per-org: at about 3:44–3:56 the Add custom connector dialog shows https://mcp.eduba.io/o/{organizationId}/mcp, and Jake says 'each MCP server is separated to each org' (4:25–4:30). At about 4:55–5:09 he pastes an org ID copied from the chat.eduba.io admin URL into it.

OAuth: at about 3:50 Eduba's client ID goes into Claude's 'OAuth Client ID (optional)' field. Jake describes the Eduba login at 5:05–5:17, but the video never shows it, so this part is stated, not demonstrated. The public metadata, re-fetched 2026-10-13, does confirm OAuth. The protected resource 'EdubaWare ICM' lists scopes openid, profile and email, with bearer tokens in a header. The authorization server adds offline_access, PKCE S256, public clients (token auth 'none') and client ID metadata documents.

Two things in the cited material have since changed:
1. **The client ID is no longer needed.** Eduba's Discord #changelogs post 'EdubaWare Alpha · Update 3.1 and Update 3.2' (David McDermott, 2026-09-03) is on screen in Don's video (8ghs34RXaUw, about 20:46–20:54). It says 'MCP authentication no-longer requires a special ClientId instead it uses CIMD instead'. So the client-ID setup step is outdated, and the earlier research that requires it is outdated on that point.
2. **There is a seventh tool.** The same note reads 'New MCP tool read_file for template files'. Don's 'New MCP read file for template files' is his spoken paraphrase. The message above it calls this 'the builder-facing MCP server'.

So at least seven tools are publicly known, all template-scoped.

RyMac's Claude (Ib1cZdCEj1g, 2026-08-31, 7:10–8:09) described 'six things it can do', and these roughly match the six tools. One of them, 'add a note to that draft', has no tool of that name. 'Manage templates only' and 'no tool lists workbenches, reads workbench files or sends chat' are inferences from the tool names and from finding nothing else. They were not shown. The nearest public mention is Jake on 2026-10-09 (Dvzh9wUUYtQ, about 1:43:16–1:43:28). He floats end users connecting 'an MCP or a plugin' to a deployed ICM, as a plan only.

### E4 — CORRECTED

**Claim** [demonstrated]: Public checks find nothing to build a separate UI on. The API host serves no API description, no SDK is published, and chat.eduba.io's response headers forbid framing by other sites.

**Source:** https://chat.eduba.io/

**Corrected:** Public checks find no documented API, SDK or embeddable view for building a separate UI on EdubaWare. api.eduba.io returns an empty 404 (server: Kestrel) on its root and on every common API-description path tried (swagger, openapi, scalar, docs, redoc). No Eduba SDK is published on npm, PyPI or NuGet. The only npm package is @eduba/ui, a brand React component kit with no API client. chat.eduba.io sends `content-security-policy: frame-ancestors 'self'` and `x-frame-options: SAMEORIGIN`, so no other origin can frame it, including Eduba's own subdomains. Terms s.6 also bars "unauthorized framing of or linking to the Services". One programmatic surface does exist: mcp.eduba.io, a separate Eduba host. It publishes OAuth metadata for a resource named "EdubaWare ICM", with public clients, PKCE and refresh tokens. It is undocumented and not in the MCP Registry. In the alpha material (C10–C13), this is the MCP connector members add to Claude, using an org-specific URL and a client ID that Eduba supplies. Its known tools manage templates. It is not a documented backend for running workbench chats from your own UI, and whether any of its tools reads workbench files is unknown.

### E5 — CORRECTED

**Claim** [stated]: What Jake has said, shipped versus planned. The 'deployment layer' shipped as the EdubaWare alpha: upload a zip, log in, work with the folder through chat. The end-user layer was still a goal on 2026-10-09: a 'little HTML dashboard', a white-label UI, auto-deployed plugins or MCP for paying customers, and payment processing.

**Source:** https://www.youtube.com/watch?v=Dvzh9wUUYtQ&t=6251s

**Corrected:** What Jake has said, shipped versus planned. The "deployment layer" (his phrase on 2026-06-14) went live as the EdubaWare alpha on 2026-08-06: upload a zip, log in, work with the folder through chat. A per-org MCP connector was also live in alpha by 2026-08-27, with manual setup. In Lyceum office hours recorded on a Thursday (most likely 2026-10-08) and published 2026-10-09 US Eastern, he said "you could do this right now ... except for the payment processing". He described the rest as goals or work in progress:
- a "little HTML dashboard" for people who just want to ask questions ("that's what we want")
- a white-labelled UI ("we're working on making it so that your UI can be yours too")
- automatically deployed plugins ("we're going to automatically deploy plugins", "looking at OpenAI plugins"), so customers can pay you for access through a plugin or MCP. Only the plugin deployment is future tense; the MCP connection already existed.
- payment processing ("We're working on that right now. You just have to charge yourself").

He gives no date for these four items. He does say "we're pushing a new UI this week", and he hopes members will have paying customers "by the end of Lyceum".

### E6 — held

**Claim** [stated]: EdubaWare can run the pipeline, not just store and display it. An agent (a Claude Code harness on Claude Sonnet) works the files inside each workbench's container whenever someone sends a chat message.

**Source:** https://www.youtube.com/watch?v=qzVXfVvXbXU&t=375s

### E7 — held

**Claim** [stated]: Eduba's Terms bar the usual ways of building on top of someone else's app: automated access, automated use and data mining, systematic retrieval, unauthorized framing, reverse engineering, and copying its code.

**Source:** https://auth.eduba.io/legal/terms

### E8 — CORRECTED

**Claim** [stated]: Commercial use and confidential material both need Eduba's approval. Commercial endeavors must be 'specifically endorsed or approved', the licence covers personal, non-commercial or internal business use, and uploaders warrant their material is not confidential.

**Source:** https://auth.eduba.io/legal/terms

**Corrected:** Commercial use needs Eduba's approval. Confidential material has no approval route. Under s.6 the Services "may not be used in connection with any commercial endeavors except those that are specifically endorsed or approved by us", and that sentence does not require the approval to be in writing. A s.6 bullet separately bars using the Services or Content "for any revenue-generating endeavor or commercial enterprise", and the bullet itself has no carve-out. Under s.2, access is licensed "solely for your personal, non-commercial use or internal business purpose", and no part of the Services, Content or Marks may be "exploited for any commercial purpose whatsoever, without our express prior written permission". Requests go to info@eduba.io.

On confidentiality, users unconditionally "warrant and represent that your Submissions and/or Contributions do not constitute confidential information" (s.2). s.7 adds that Contributions "may be treated as non-confidential and non-proprietary", and s.8 gives Eduba a perpetual licence that includes the right to "disclose" them. No clause lets Eduba approve confidential material.

The only "unless expressly agreed by Eduba in writing" exception is s.27, and it covers regulated data (protected health information, cardholder data, other industry-regulated data), not confidential information in general. s.1 also says that if your interactions would be subject to HIPAA- or FISMA-type rules, "you may not use the Services", with no exception. The Terms do not say whether private workspace files count as "Contributions". (Terms v2.0, last updated July 14, 2026.)

### E9 — CORRECTED

**Claim** [stated]: The receiver would need their own Eduba login and an org invitation, but no Claude or ChatGPT account. Sign-in is by emailed code or 'Continue with Google'.

**Source:** https://auth.eduba.io/login

**Corrected:** You sign in with a 6-digit code emailed to you or with 'Continue with Google' (auth.eduba.io/login, stated). EdubaWare's own sign-in at chat.eduba.io/Account/Login sends you to the same 'eduba-auth' service, 'with email verification or Google'. That login page also says: 'Use the same email as your Skool account so your membership links automatically.' So Eduba accounts are tied to Clief Notes Skool membership.

To work in someone else's org through the browser chat, a receiver needs:
- Their own Eduba login. The Terms (s.6) ban 'sharing account credentials or allowing others to access the Services through your account'. That it must be their own login is inferred from this ban.
- An email invitation into that org. This is the only route shown so far. chat.eduba.io/for-enterprise says: 'Invite an existing account into a specific persona inside the organization.'

Jake says they need no ChatGPT or Claude account, because Eduba supplies the model (stated: launch video 18:37–19:07, office hours 1:43:06). No real end user has been shown doing this.

It is unknown whether a login plus an invite is enough for someone outside Clief Notes. At launch Jake said non-members 'can sign up' but 'won't have access to anything' (qzVXfVvXbXU, about 20:07–20:27).

The cited login page supports only two things here: the sign-in methods and the Skool-membership link. The invite, the 'own login' point and the no-AI-account point all come from other sources.

