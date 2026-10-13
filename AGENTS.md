# AGENTS.md

This is the `.github` repo of the **corisco-wallet** GitHub org. It holds
org-wide defaults only; no application code lives here.

## What's here

- `profile/README.md` -- the org homepage README (project pitch, repo list, donation badge).
- `README.md` -- explains what this repo is for.
- `CODE_OF_CONDUCT.md`, `SECURITY.md`, `PULL_REQUEST_TEMPLATE.md`, `ISSUE_TEMPLATE/` -- default community-health files, inherited by any org repo that doesn't define its own.
- `DONATE.md`, `FUNDING.yml` -- donation page and GitHub Sponsors/funding config.

`CONTRIBUTING.md` and `CODEOWNERS` are deliberately **not** here: build and
ownership rules differ per repo, so each repo has its own.

## The Corisco project (context for the whole org)

A self-custodial Lightning wallet whose private keys live on a dedicated
ESP32-S3 hardware signer, not the phone. Every signature is confirmed on the
device's own screen. Built on Spark's FROST threshold-signing protocol.
Hard invariant: **private key material never leaves the ESP32.**

| Repo | Role |
|---|---|
| `corisco-firmware` | ESP32 firmware (Rust) + the BLE wire protocol (`corisco-protocol`) |
| `corisco-android-app` | React Native / Expo mobile app; talks to the device over BLE |
| `crypto-core` | Platform-agnostic Rust signing crypto (BIP32/39, FROST, VSS/ECIES), used by the firmware |
| `.github` | This repo |

Dependency flow: `crypto-core` (pinned by tag) -> `corisco-firmware` ->
(wire-protocol vectors, pinned by release tag) -> `corisco-android-app`.

## Working here

- Keep the repo list in `profile/README.md` in sync when org repos are added, renamed or removed.
- Security-relevant policy changes go through `SECURITY.md`; don't weaken disclosure instructions.
- Commits follow Conventional Commits; see `.claude/rules/commit-conventions.md`.
  Never add `Co-Authored-By` or "Generated with Claude Code" lines to commits or PRs.
