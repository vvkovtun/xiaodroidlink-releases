# XiaoDroidLink 7.81 (versionCode 127)

## What changed

- Faster live gestures after the 7.80 car test (`capture/probe-2026-10-28-780.log`: 77 live gestures, the phone finished the movement 151 ms after the finger lifted, 270 ms at p90, up to 990 ms):
  - the hold before the movement is replayed only when it is a long press (≥ the system long-press timeout); otherwise the live gesture starts with a 16 ms stroke;
  - live chunks are at most 32 ms (was 100 ms), so the phone catches up with the finger;
  - one-finger live drag waits 50 ms for a second finger (was 60 ms).

## Verified

- Emulator: live two-finger pinch and one-finger drag on Google Maps, tap unchanged. Quick release for a car test, full smoke test not run.

AAB SHA-256: `a2c1e74036e4a728468a576572192ef2218ef67c3e4f77958be3e472199d07fa`
