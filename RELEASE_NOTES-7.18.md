# XiaoDroidLink 7.18 (versionCode 64)

## What changed

- **Dark theme colours.** Five colour sets: Ocean (the previous look), Graphite,
  Bronze, Emerald, Amethyst. Background, cards, borders and the accent of
  buttons and switches change; warning colours (yellow, green, red) stay the
  same. Choose on the car screen (gear → "Dark theme colours") or in the phone
  app. The car settings panel now has six rows, so its buttons are a bit lower.
- **New look.** Widget cards have a soft shadow, an accent glow from the corner
  and a glass edge; tiles, the dock, map buttons and the air alert card follow
  the same style. The dock highlights the selected app in the accent colour.
  The rail in phone-screen mode has icons instead of letters.
- **Rotate button** on the rail when the car shows the phone screen: switches
  the current app between landscape and portrait and remembers the choice (the
  same setting as ↔/↕ in the phone app's list). Needs the "Modify system
  settings" permission.
- **Reading a message aloud without music.** While the player is paused the car
  keeps our audio stream paused, so the phrase was not heard. A spoken phrase is
  now reported to the car as playing, and the phrase starts 0.9 s later to let
  the car switch. The same applies to voice warnings.

## Verified

- On the emulator: all five colour sets and the light theme on the home screen,
  the settings panel, tapping a colour set, the Rotate button (the phone
  switched to portrait and back).

## Not verified

- Anything in the car: the new colours on the real screen, the Rotate button,
  and the message-reading fix (the emulator has no car audio; the cause is
  inferred from the code).
- Everything listed as not verified in 7.16 and 7.17.

Local verification: emulator smoke suite on Android 16 — 89 passed, 0 failed,
2 skipped (ChatGPT listening and music controls need a real phone). It covers the
Road layout and the pre-existing controls; it does not cover the car connection,
audio or Bluetooth.

APK SHA-256: `f6fc3659ff1074164f74735cbbf009df2ba3fc42e5f54dcde4c02c7d2e52d8f9`

AAB SHA-256: `9699b23f238f71f2b2af4aba23e9a258e3f242000ea43b3722372b94fc6528ce`
