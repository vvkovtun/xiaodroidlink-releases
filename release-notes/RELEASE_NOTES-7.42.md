# XiaoDroidLink 7.42 (versionCode 88)

## What changed

- Album art: the cover of the playing song now appears on the car screen. It is sent once per track as a PNG together with the player id — the format the car accepts (a JPEG cover in 7.22 was ignored and slowed down track switching). Checked in the car: the cover showed and switching stayed fast.
- Voice in the headrest: while CarLink is connected, speed-camera and air-raid warnings and the built-in route prompts go to the car as a separate voice stream, which the Xiaomi YU7 plays in the driver's headrest, the same way as its own navigation prompts. Without CarLink they are spoken as before.
- The test copy ("XDL test") has extra protocol checks (car microphone, call state for the car, clean disconnect, window modes); they are off in the regular app.

## Verified

- Core tests: 16 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped.
- In the car (test build, 2026-10-17): album art shown, test phrase heard in the headrest.

APK SHA-256: `11a7650214cc1b0a3b862cb288e35472948e85e1c5be62cc7cbc948687b2d6aa`

AAB SHA-256: `9e38ec5424dfdfdf4293f7f4a5e59bf9f9a7fdd37189665d8ea7188639384e8a`
