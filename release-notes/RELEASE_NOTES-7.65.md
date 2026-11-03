# XiaoDroidLink 7.65 (versionCode 111)

7.64 was built but never uploaded to Google Play; its changes ship in 7.65.

## What changed

- "Assistant commands" list: on the car screen, a button at the top of the settings opens the commands verified in the car, grouped (climate, seats, wheel and glass, mirrors, windows, trunks and charge port, wipers, lights, screen theme, phone AI), plus what the car does not do by voice and what is still being tested. The same list opens from the "Assistant commands" button under the "Car assistant in your language" switch on the phone.
- Car voice buttons removed from Quick actions (the steering wheel button had to be pressed anyway); saved car voice buttons are dropped on load.
- From 7.64: removed commands the car refused (settings pages, home screen, unlock, system version, notifications, voice skills, radio, Standard mode); "high beam" is answered on the phone (left stalk only); new tries for temperature as a number, AC off, battery, range and volume.
- Documentation (5 languages): install from Google Play only, the APK download is gone; if an APK was installed before, uninstall it first (different signature).

## Verified

- Emulator: assistant commands panel on the car screen (Ukrainian and English) and settings button.
- Quick emulator smoke test: 48 passed, 0 failed, 2 skipped.
- Not verified in the car.

AAB SHA-256: `349f86d28c189fa88f0744d80b41c958301f90efd9e7e16f869e6150fbe2c99b`
