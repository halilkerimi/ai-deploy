# Elyvers — releases

Compiled builds of **Elyvers**, the agent owner's desktop client for an
agent-mesh deployment. **This repository holds no source code** — the source is
private. What is here:

- **GitHub Releases** (`v<version>`): the installers and the files the app's
  updater reads — `latest.yml` (Windows), `latest-mac.yml` (macOS), the
  `.blockmap` beside each artifact.
- `releases/<version>/` in git: the channel files as published and a short
  note per version. Small text only; never a binary.
- `CHANGELOG.md`: what changed, per version.

## Installing

- **Windows:** download `Elyvers Setup <version>.exe` from the latest release
  and run it. Until the installer is code-signed, SmartScreen shows a warning
  on first install — choose *More info › Run anyway*. The app updates itself
  from here afterwards.
- **macOS:** download `Elyvers-<version>-arm64.dmg`, drag Elyvers to
  Applications, and open it with **right-click › Open** the first time (the
  build is not yet signed with a Developer ID, so Gatekeeper asks). macOS
  builds do not auto-update until the app is signed.

## Versions

Plain semver, no suffixes. `0.x.y` is the internal-testing line (every build
there is a beta, whatever its notes say); `1.0.0` is the first public release.
Releases are never marked "pre-release" on GitHub: the app's feed resolves
`releases/latest/download/`, which skips pre-releases.

## The update feed

The app is built with its feed pointed at
`https://github.com/halilkerimi/ai-deploy/releases/latest/download/`, so
publishing a release here IS the rollout. Rollback is re-pointing
`latest.yml` in a new release; staged rollout is `stagingPercentage` in the
channel file.

Published by `npm run publish:deploy` from the private repository — a script
that refuses to copy anything but the known artifact types.
