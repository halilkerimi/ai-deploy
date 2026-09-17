# Changelog

All notable changes to the published builds, newest first. Versions follow the
app's `package.json`; each entry links the GitHub release that carries the files.

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
