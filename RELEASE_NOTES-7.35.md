# XiaoDroidLink 7.35 (versionCode 81)

## What changed

- Removed the Bluetooth address item from 7.34: the car acknowledged it, but it did not change when the car keeps Bluetooth calls.
- Bluetooth calls now follow the order the Xiaomi YU7 accepts: car Bluetooth first, CarLink a moment later. Auto-connect waits up to 10 s for the car's Bluetooth and connects CarLink as soon as it arrives.
- If you choose the car in Bluetooth settings during a session, the app pauses CarLink for a moment so the car accepts the connection, then reconnects right after it.
- The "car Bluetooth is not connected" notification opens Bluetooth settings directly.
- A handset icon next to the clock on the car screen: green when calls and ChatGPT go through the car, grey when they stay on the phone.

## Verified

- Core tests: 15 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped.

## To verify in the car

- Bluetooth calls staying connected after car start, after choosing the car in Bluetooth during a session, and the handset icon.

APK SHA-256: `0362502d75685a30b77344ed2e2612d0923cd7bd10419339a4427b523148d65b`

AAB SHA-256: `9e28119f139b8a7ee9c66e6d6b81a8bfd01b35980ccbe2433404653379103789`
