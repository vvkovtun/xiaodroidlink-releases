# XiaoDroidLink 7.27 (versionCode 73)

## What changed

- **No extra pause on track change.** 7.26 told the car "pause" while the
  player switched tracks, hoping the YU7 would show the track title on its
  panel. It did not. The early logs show the title on the panel came from the
  phone's Bluetooth audio (AVRCP), which the YU7 refuses while CarLink is
  running. The pause is removed; the title is still re-sent once the track
  starts playing (7.25).

## Verified

- Core tests: 14 passed. The change runs only with a car connected.

## Not verified

- In the car: everything listed as not verified in 7.16–7.26.

APK SHA-256: `e3c3abdb208838c68959cfe5e10b8b03e79da04cc40c57bd15fe2d899128772e`

AAB SHA-256: `f332637a2dba303231909b88bf965bc1ebbc175fa03647cf331218eb8ce6edbd`
