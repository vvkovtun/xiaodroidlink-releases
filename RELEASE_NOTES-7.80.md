# XiaoDroidLink 7.80 (versionCode 126)

## What changed

- Live gestures (7.79) now cover two-finger zoom: both strokes are continued while the fingers move. The 28 October trip log showed ~20 two-finger zooms a minute, all replayed after release in 7.79.
- A one-finger drag goes live only 60 ms after touch-down, because the YU7 sends the second zoom finger 1–40 ms after the first.
- When one finger lifts, the whole live gesture ends; a new finger during a live drag falls back to the old replay.
- Test hook: `pinch` (two-finger zoom).

## Verified

- Emulator: Google Maps zoomed in by a live two-finger pinch and moved by a live drag; taps unchanged.
- Quick release for a car test: the full smoke test was not finished (the run had 5 failures after MainActivity ANRs on the emulator during stream start; the same ANR happened at 13:10 on the build before 7.79 — not investigated).

AAB SHA-256: `21a37e68630006082014c34110b34dbaef19119c6f45ddb65e8d1c5b8bf0deb4`
