# Elyvers 0.5.0

Elyvers 0.5.0 — internal beta, 2026-09-17.

Pulse can now show an HTML block the agent composes (EL-71): it renders inline on the start page, checked against the same allow-lists the server uses, with action links and embedded frames as per-agent switches (both off by default). A Pulse instruction no longer moves you to the chat — the page stays and says the instruction went out. Pulse refresh can be scheduled by time and weekday. Fixed: switching chats could show another chat's messages in the one you opened (EL-69).

Windows: `Elyvers Setup 0.5.0.exe` — built on a Windows machine from the same tag and uploaded to this release separately; unsigned: SmartScreen › More info › Run anyway on first install. Updates itself from here afterwards.
macOS: the dmg, opened via right-click › Open the first time (unsigned). The app tells you about the next version and links here; it cannot install it itself until it is signed.
