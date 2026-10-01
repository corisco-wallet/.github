# Corisco

A self-custodial Lightning wallet where private keys live on a dedicated
ESP32-S3 hardware device, not your phone. Every signature is confirmed
physically on the device's own screen before it happens.

Built on [Spark](https://www.spark.money/)'s FROST-based threshold
signing protocol.

## Repositories

- **[corisco-wallet](https://github.com/corisco-wallet/corisco-wallet)** -- the
  ESP32 firmware and the React Native mobile app, which share one BLE
  wire protocol and evolve together.
- **[crypto-core](https://github.com/corisco-wallet/crypto-core)** -- the
  platform-agnostic signing logic (BIP32/BIP39, FROST threshold signing,
  the leaf-ownership-transfer crypto) used by the firmware.

Start with `corisco-wallet`'s README for the architecture overview and a
quickstart for each component.
