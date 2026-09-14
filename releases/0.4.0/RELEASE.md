# Elyvers 0.4.0

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
