# XiaoDroidLink 7.63 (versionCode 109)

## What changed

- Car voice, fixes from the 2026-10-26 trip log: "увімкни дальнє світло" turned on the cabin light (now high beam 打开远光灯, also when heard as "у вікні дальнє світло"); "підігрів (переднього / лобового) скла" turned on seat heating (now windshield defog 打开前挡除雾); "противотуманка" was not understood; "вибне кондиціонер" / "виб не вентиляцію" (misheard "вимкни") turned things on; "відкрий дзеркало" folded the mirrors (now unfolds them as 打开后视镜 — the car ignored 展开后视镜); "задніх пасажирів" went to the front passenger (now 后排).
- Temperature as a number without a seat goes to the driver (主驾温度调到N度): the car otherwise sets the zone the phone's voice comes from.
- The phone listens for the car's answer up to 9 s (it gave up after ~1 s every time, so battery and range were never read) and logs the car's reply to every command.
- New commands from the car's Voice Skills menu: drive mode, light and mirror settings pages, close settings, home screen, unlock, system version, light/dark theme, notifications, "what can you do", radio / FM frequency, voice volume, Standard drive mode. Nine of them also as Quick action buttons (52 in total, three pages).
- User guide lists only the commands verified in the car; the full table with results is in docs/20-car-voice-commands.md.

## Verified

- Emulator: the guide phrases, the trip-log phrases and the new commands give the expected Chinese (TestHook carmatch).
- Quick emulator smoke test: 48 passed, 0 failed, 2 skipped.
- Not verified in the car: everything new in this list.

APK SHA-256: `d4208f0c28f245c3f0db068644dd1491162cc59383ab0048c30cc3db5d5ee121`

AAB SHA-256: `6657163495074d5ff9132d32ead47d5522ffb1380c67fe7311c74c18f0865e0e`
