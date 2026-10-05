## What does this change and why?

<!-- One or two sentences. Link an issue if there is one. -->

## Component(s) touched

- [ ] `corisco-firmware` (firmware / `corisco-protocol`)
- [ ] `corisco-android-app`
- [ ] `crypto-core`
- [ ] docs / CI only

## Checks

- [ ] `cargo fmt` / `cargo clippy` clean (for Rust changes)
- [ ] `npx tsc --noEmit` clean (for corisco-android-app changes)
- [ ] Tests added/updated for the behavior change, or N/A
- [ ] If this touches the BLE wire protocol (`corisco-protocol`): new
      `Request`/`Response` variants are **appended**, not inserted, and
      `protocol/vectors.json` was regenerated
      (`UPDATE_VECTORS=1 cargo test -p corisco-protocol`)
- [ ] If this changes the wire protocol: a follow-up PR updates `postcard.ts`
      in `corisco-android-app` and bumps its pinned firmware release
- [ ] If this changes `crypto-core`: firmware's pinned `crypto-core` tag is
      bumped in a follow-up PR
- [ ] If this is a firmware UI/screen change: attached a screenshot or
      short clip from real hardware

## Anything reviewers should look at closely?

<!-- e.g. "this touches signing confirmation gating" -- flag it, don't
     make the reviewer discover it. -->
