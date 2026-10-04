## What does this change and why?

<!-- One or two sentences. Link an issue if there is one. -->

## Component(s) touched

- [ ] `crypto-core`
- [ ] `esp32-firmware`
- [ ] `corisco-android-app`
- [ ] docs / CI only

## Checks

- [ ] `cargo fmt` / `cargo clippy` clean (for Rust changes)
- [ ] `npx tsc --noEmit` clean (for corisco-android-app changes)
- [ ] Tests added/updated for the behavior change, or N/A
- [ ] If this touches the BLE wire protocol: both `ble.rs` and
      `postcard.ts` were updated in this PR, with the new variant
      **appended**, not inserted
- [ ] If this is a firmware UI/screen change: attached a screenshot or
      short clip from real hardware

## Anything reviewers should look at closely?

<!-- e.g. "this touches signing confirmation gating" -- flag it, don't
     make the reviewer discover it. -->
