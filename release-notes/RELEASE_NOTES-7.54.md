# XiaoDroidLink 7.54 (versionCode 100)

## What changed

- Car sound that silently stops: on 2026-10-24 the YU7 showed the song playing but played nothing, although the phone was sending sound (AAC −14 dBFS) and had sent START; only a reconnect helped. Before that, five voice prompts went to the driver's headrest (STREAM_TTS) while music was stopped. Now Play pressed on the car screen after a pause re-announces the sound to the car (STOP, then START on the next report), and after a run of headrest prompts with no music playing the app sends one STOP so the next song starts clean. Not checked in the car yet.
- Accessibility shortcut warning: Android turned the Accessibility service off through its shortcut (floating button, two-finger gesture or volume keys) — `dumpsys accessibility` shows `performAccessibilityShortcutTargetService` for every drop. The phone app now warns when XiaoDroidLink is assigned to any of these shortcuts and opens Accessibility settings. The warning is phone-only, not a banner in the car.
- Docs: new pages "All features" and "Home screen widgets" (English and Ukrainian) describing every widget and feature, and the English and Ukrainian presentation videos in the README.

## Verified

- Core tests: 16 passed. Emulator smoke test: 87 passed, 1 failed, 2 skipped. The failure is the pixel-9-pro-xl touch check: the touch landed exactly in the centre (1496,672 on 2992×1344) while the emulator was rotating; touch mapping was not changed in this release.
- Not checked in the car.

APK SHA-256: `b2111f1584d39e1c059e3df0e458d91d8070e4dd33e8af088ec03d19b24d7271`

AAB SHA-256: `bc49c10166786fe031c435829a5956820a7086c3fc71b58f653a1555c37f7529`
