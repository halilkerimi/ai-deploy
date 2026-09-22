# Changelog

All notable changes to the published builds, newest first. Versions follow the
app's `package.json`; each entry links the GitHub release that carries the files.

## 0.7.0 — 2026-09-22

Elyvers 0.7.0 — internal beta, 2026-09-22.

Changes since v0.6.0:
- feat(chat): the tasks list is a drawer beside the chat, and the whole rail opens it (EL-72 round 5)
- docs(tickets): EL-73 — the model chip blames the administrator for a failed catalogue read
- feat(chat): the Background tasks panel — running and finished, stop one task, show its transcript (EL-72 round 4)
- feat(chat): show live what the agent is doing — background tasks, the round it starts by itself, the turn receipt (EL-72)
- docs(jira): strip the folder down to the actions
- docs(28): the Windows handover for 0.6.0 — the pilot build
- docs(jira): rewrite the comments to post — English, and worth reading
- docs(jira): two more arrived — VERS-258 and VERS-324, both zu-entscheiden
- feat(chat): search message text, not just titles (VERS-194)

Windows: `Elyvers-0.7.0-x64-setup.exe` — unsigned: SmartScreen › More info › Run anyway on first install. Installs per machine since 0.6.0: run it as administrator, and an installed copy updates only with administrator rights.
macOS: no build in this release (Windows only). Installed Mac copies stay on 0.6.0, whose files remain on the 0.6.0 release.

Release: https://github.com/halilkerimi/ai-deploy/releases/tag/v0.7.0

## 0.6.0 — 2026-09-21

Elyvers 0.6.0 — internal beta, 2026-09-21.

Changes since v0.5.0:
- docs(jira): re-pull — the High one PASSED, and two arrived from the in-chat search story
- fix(feedback): report times in the reader's own zone, not raw UTC (VERS-236)
- docs(jira): re-pull — VERS-236 is new and failing, three tickets left your name
- fix: make the suites green — one of mine, three that predate me
- docs(jira): six tickets are fixed and UNRELEASED — say so in the index
- feat(chat): show how long a turn has been running (VERS-221)
- feat(chat): name what the agent is doing, instead of showing the tool id (VERS-220)
- feat(chat, connectors): keep the rejected draft, and make 282 tools reviewable
- docs(jira): VERS-305 now backs a client commitment, and the ask should change
- docs(29): the client's IT has already called the certificate 'kein Blocker'
- docs(jira): the hand-made 282-row tool spreadsheet is VERS-305's real evidence
- docs: the owner's screenshots answer VERS-141 and expose a defect behind VERS-239
- docs(29): the legal entity is Leonova GmbH — half of the open question answered
- chore: keep meetings/ out of git
- build(win): per-machine install, for the pilot clients' IT to deploy
- docs(29): scope to Windows only — macOS signing deferred on the owner's word
- docs(29): how to stop shipping unsigned — what to buy, from whom, in what order
- test: gate the two fixes — danger-hover fill, and the editor's two modals
- docs(jira): the VERS-303 capture — tester was on 0.2.0, and no session switch
- fix(processes): the signed-out notice no longer hides the close question (VERS-230)
- fix(ui): a danger button's label no longer vanishes on hover (VERS-197)
- docs(jira): ready-to-paste resolutions for the five fixed tickets
- docs(jira): what is fixed and what is not — 21 tickets checked against the source
- docs(jira): my live Jira tickets, worked locally — one file per ticket and an index
- docs(28): the Windows runbook's release block is 0.5.0's

Windows: `Elyvers Setup 0.6.0.exe` — built on a Windows machine from the same tag and uploaded to this release separately; unsigned: SmartScreen › More info › Run anyway on first install. Updates itself from here afterwards.
macOS: the dmg, opened via right-click › Open the first time (unsigned). The app tells you about the next version and links here; it cannot install it itself until it is signed.

Release: https://github.com/halilkerimi/ai-deploy/releases/tag/v0.6.0

## 0.5.0 — 2026-09-17

Elyvers 0.5.0 — internal beta, 2026-09-17.

Pulse can now show an HTML block the agent composes (EL-71): it renders inline on the start page, checked against the same allow-lists the server uses, with action links and embedded frames as per-agent switches (both off by default). A Pulse instruction no longer moves you to the chat — the page stays and says the instruction went out. Pulse refresh can be scheduled by time and weekday. Fixed: switching chats could show another chat's messages in the one you opened (EL-69).

Windows: `Elyvers Setup 0.5.0.exe` — built on a Windows machine from the same tag and uploaded to this release separately; unsigned: SmartScreen › More info › Run anyway on first install. Updates itself from here afterwards.
macOS: the dmg, opened via right-click › Open the first time (unsigned). The app tells you about the next version and links here; it cannot install it itself until it is signed.

Release: https://github.com/halilkerimi/ai-deploy/releases/tag/v0.5.0

## 0.4.0 — 2026-09-14

Elyvers 0.4.0 — internal beta, 2026-09-14.

What's new since 0.3.0

New
- Chat: paste or drop a file into the conversation to attach it; a pasted screenshot shows its own picture on the chip (EL-62).
- Chat: files an agent sends are SHOWN, not only offered — pictures, text, CSV tables and now PDF pages you can turn, above the download chip (EL-63, EL-67).
- Chat: your own sent files get the same preview under your message, PDFs included (EL-67).
- Chat: "Report this chat" saves one self-contained HTML file with the conversation, the agent and a picture of the chat, for feedback (EL-64).
- Pulse: with more than one agent it is a dashboard — every agent's report, grouped by day.
- Sign-in: every sign-in is "keep me signed in" — the credential sits in the OS keychain (Keychain on macOS, DPAPI on Windows), Touch ID guards it where a Mac has one, and signing out is what forgets it.
- Connectors: the client-credentials sign-in kind (client id + secret + scope) is built end to end.

Changed
- Chats, Runs and Setups: the list and what it opens are two columns of one card, divided by a handle you drag or move with the arrow keys; the width is shared and remembered (EL-65, EL-66).
- Chat list: sticky group headers, a lighter ground, a clearer selected row, thinner full-width dividers.
- Agents: the agent picker is one row, and "updated … ago" sits with the lifecycle actions.
- The rail's icons and the main card sit centred in their gutters.

Fixed
- An account with no agent assigned is handled on every screen — no endless "Resolving your agents…", nothing offered that cannot work (EL-68).
- Connectors: a platform credential no longer reports itself cleared when nothing was deleted; the disconnect dialog says whose credential it is and what the wire knows about it.
- Update and deployment: 25 review findings — among them the release notes baked into the app, the notes credited to the wrong version, and a stale session timer after changing the master.
- The in-card divider's grab pill runs the full height.

Under the hood
- One content model for the transcript — live, restored from the server and cached locally render the same way, so a reloaded turn shows its tool activity, reasoning and files exactly as the live one did.
- The transcript refactor's tests were paid back (16 files) and the last 13 journeys made green, with three real defects found on the way.

Windows: `Elyvers Setup 0.4.0.exe` — built on a Windows machine from the same tag and uploaded to this release separately; unsigned: SmartScreen › More info › Run anyway on first install. Updates itself from here afterwards.
macOS: the dmg, opened via right-click › Open the first time (unsigned). The app tells you about the next version and links here; it cannot install it itself until it is signed.

Release: https://github.com/halilkerimi/ai-deploy/releases/tag/v0.4.0

## 0.3.0 — 2026-09-06

Elyvers 0.3.0 — internal beta, 2026-09-06.

Changes since v0.2.0:
- fix(shell): say the app is checking your session, instead of a form nobody should type into (EL-61)
- docs: how 0.2.0 was cut, and the website-publish path
- chore(deploy): publish from the website with --no-gh, and clear the failed win build's tree

⚠ macOS only — no Windows installer in this release.
macOS: the dmg, opened via right-click › Open the first time (unsigned). The app tells you about the next version and links here; it cannot install it itself until it is signed.

Release: https://github.com/halilkerimi/ai-deploy/releases/tag/v0.3.0

## 0.2.0 — 2026-09-06

Elyvers 0.2.0 — internal beta, 2026-09-06.

Changes since v0.1.0:
- feat(update): the app tells you about a new version and asks before restarting (EL-60)
- chore(deploy): the tag names the release commit, win is x64, and the Rosetta fact

⚠ macOS only — no Windows installer in this release.
macOS: the dmg, opened via right-click › Open the first time (unsigned). The app tells you about the next version and links here; it cannot install it itself until it is signed.

Release: https://github.com/halilkerimi/ai-deploy/releases/tag/v0.2.0

⚠ Corrected 2026-09-07: this entry originally also listed `chore(deploy): publish from the website with --no-gh…`, which landed AFTER 0.2.0 was built and is in 0.3.0. The resumed deploy computed its notes from HEAD instead of from the release commit; `scripts/deploy.mjs` now computes them from the release commit. The notes baked into the app's own channel file were always the right two.
