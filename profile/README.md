# Corisco

A self-custodial Lightning wallet where private keys live on a dedicated
ESP32-S3 hardware device, not your phone. Every signature is confirmed
physically on the device's own screen before it happens.

Built on [Spark](https://www.spark.money/)'s FROST-based threshold
signing protocol.

## Repositories

- **[corisco-firmware](https://github.com/corisco-wallet/corisco-firmware)** -- the
  ESP32 hardware-signer firmware and the BLE wire protocol it defines.
- **[corisco-android-app](https://github.com/corisco-wallet/corisco-android-app)** --
  the React Native mobile app, tested against the firmware's protocol
  vectors.
- **[crypto-core](https://github.com/corisco-wallet/crypto-core)** -- the
  platform-agnostic signing logic (BIP32/BIP39, FROST threshold signing,
  the leaf-ownership-transfer crypto) used by the firmware.

Start with `corisco-firmware`'s README for the architecture overview and a
quickstart for each component.
