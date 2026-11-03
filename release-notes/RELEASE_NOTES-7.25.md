# XiaoDroidLink 7.25 (versionCode 71)

## What changed

- **Track title for the car HUD.** After Next track the player buffers for a
  moment, so the new title went to the car marked "not playing" and was not sent
  again once the track started (phone log of 2026-10-14, YouTube Music). The
  title is now sent once more when the player starts playing.

Includes 7.24 (versionCode 70, uploaded to Google Play only): YouTube title
returns to the music card after a pause, an ad or switching apps; more sources
for the music card picture; CarLink capabilities on the car data screen.

## Verified

- Core tests: 14 passed. Emulator smoke suite on 7.24: 49 passed, 0 failed,
  2 skipped (the 7.25 change runs only with a car connected).

## Not verified

- In the car: whether the title now shows on the YU7 HUD.
- Everything listed as not verified in 7.16–7.24.

APK SHA-256: `71b4c802b074d7ee3e88074faa598af5ba03876c004c6390a7809a19430c106a`

AAB SHA-256: `17ca24183348da6d0147a412675cd2940899047cf680e0466e22493764032d16`
