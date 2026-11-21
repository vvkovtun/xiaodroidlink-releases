# XiaoDroidLink 8.90 (versionCode 236) — internal

## What changed

- **Easier crosshair in «Set position»** (Vadym, 21.11: hard to aim, dragging with two fingers did not move the map). A tap on the map now puts that point under the crosshair — one touch, then «I'm here». Before, a tap on the built-in map opened the maps app.
- **The built-in map follows one finger live** while dragging, instead of jumping once the finger is lifted (everywhere, not only in «Set position»).
- **Two fingers move the map as well as zoom it**, like Google Maps.
- Hint: «Tap where you are or move the map».

## Verified

- Core tests 65/65, translations complete, build OK.
- On the emulator: a tap moved the tapped point under the crosshair; a one-finger drag moved the map. Two-finger gestures and smoothness in the car not checked.
