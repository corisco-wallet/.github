# Security Policy

This org builds a hardware Lightning/Spark signer -- a device meant to
hold private key material and gate every signature on physical
confirmation. Security issues here can mean real fund loss, so please
report them privately rather than through a public issue.

## Scope

Treat as a security issue (not a regular bug) anything involving:

- Private key or seed material being exposed, derivable, or leaving the
  device unexpectedly.
- The on-device signing confirmation being bypassable, spoofable, or
  skippable for a real fund-moving signature.
- BLE pairing/bonding/authentication weaknesses (e.g. a way to connect or
  send signing requests without going through real pairing).
- PIN storage/lockout weaknesses (e.g. a way to brute-force the PIN
  without triggering the wipe policy).
- Anything that lets the phone app show one thing on the confirm screen
  while a different transaction actually gets signed.

Regular bugs, crashes, UI issues, and build/CI problems should go through
normal public issues instead.

## Reporting a vulnerability

Please report privately to **ruipedrotelesribeiro@gmail.com** (or via
[GitHub's private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing/privately-reporting-a-security-vulnerability)
on the affected repo, once enabled) rather than opening a public issue or
PR. Include:

- Which repo/component is affected (`crypto-core`, `corisco-firmware` or
  `corisco-android-app`).
- Steps to reproduce, or a description of the weakness if reproduction
  needs physical hardware you don't have.
- What you think the actual impact is.

## Response time

This is currently a solo-maintained project, so please be patient --
there's no dedicated security team or SLA yet. Reports will be
acknowledged as soon as reasonably possible and credited (if you'd like)
once a fix ships.
