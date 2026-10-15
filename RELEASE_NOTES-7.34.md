# XiaoDroidLink 7.34 (versionCode 80)

## What changed

- New item in Permissions: **Bluetooth calls in the car**. Enter this phone's Bluetooth address once (Settings → About phone → Status information). Without it the Xiaomi YU7 treats the Bluetooth phone as a different phone and disconnects calls when CarLink connects, so calls and ChatGPT stay on the phone.
- Like Samsung CarLink and Xiaomi CarWith, the app now sends the car a SHA-256 fingerprint of that address after the picture starts (BluetoothMacInfo, synchronous message, up to three tries waiting for the car's acknowledgement). The Permissions item then shows whether the car confirmed it.
- With the address entered, the "car Bluetooth is not connected" notification opens Bluetooth settings directly and no longer pauses CarLink.
- The address field formats itself (colons are added automatically) and opens with the keyboard ready.

## Verified

- Core tests: 15 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped.
- Address entry and saving checked on the emulator.

## To verify in the car

- Whether the car acknowledges the message (the Permissions item shows "confirmed by the car"), and whether Bluetooth calls (HFP) now stay connected next to CarLink.

APK SHA-256: `7ba42f259d8cdb27314e81bb92f225df585b880227d014b311eb4960beac378c`

AAB SHA-256: `fbfaa6b81b91a07a5dff26798593ff8add76d12324ce3cf65ca1c0500387261a`
