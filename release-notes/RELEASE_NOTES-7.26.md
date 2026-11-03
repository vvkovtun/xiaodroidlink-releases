# XiaoDroidLink 7.26 (versionCode 72)

## What changed

- **Pause → play on track change, as before 7.20.** 7.25 sent the new title a
  second time marked "playing", but the YU7 still did not show it (phone log of
  2026-10-14). Before 7.20 every track change also sent the player state
  "pause" and then "play", and the title was shown. Since 7.20 the sound check
  kept the state at "playing". Now, while the player switches tracks (until it
  starts, at most 3 seconds), the car is told "pause" again.

## Verified

- Core tests: 14 passed. The change runs only with a car connected, so the
  emulator cannot exercise it.

## Not verified

- In the car: whether the title now shows on the YU7 panel, and that the short
  pause does not interrupt the sound.
- Everything listed as not verified in 7.16–7.25.

APK SHA-256: `cee8b400d8812553697a4d89b361c08a444ab2ee71f228b6db284b53a411536a`

AAB SHA-256: `926654ace87e1102e0dd18f79571e1c43a402a5df1e4fcba57896804623a217b`
