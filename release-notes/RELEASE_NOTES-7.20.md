# XiaoDroidLink 7.20 (versionCode 66)

## What changed

- **Sound from YouTube and other apps.** The car plays the phone's sound only
  while the app reports "player is playing". Until now that followed only the
  player shown on the dashboard, so YouTube or any other app stayed silent
  unless music was playing too. Now "playing" is also reported whenever the
  phone actually produces sound, whichever app plays it; "pause" is sent after
  4 seconds of silence.
- **Documentation.** Car-screen screenshots retaken in the Ocean design; the
  phone main-screen screenshot shows the current version.

## What to expect

- The first second or two of sound in YouTube may be lost while the car
  switches to the phone's sound.
- After music is paused the car stays on the phone's sound for about 4 more
  seconds.

## Verified

- The build compiles; core tests: 13 passed, 0 failed.

## Not verified

- The fix itself: it needs the car. The emulator smoke suite was not run for
  this release (it does not cover car audio).
- Everything listed as not verified in 7.16–7.19.

APK SHA-256: `d88a0ba233be35bb1d2d2b4643334b8f1b286a8dfb1bfeb20d4c3752f0355bd7`

AAB SHA-256: `6f0d65c0a3027ffe644f3e2391153fab6b52d15d4c6803dc4dfdec3dbbddc0d2`
