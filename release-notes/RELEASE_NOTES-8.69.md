# XiaoDroidLink 8.69 (versionCode 215) — internal

## What changed

- **Lynk & Co 06 picture shifted right/down** (Olga, vivo I2405, 8.60, photo 13.11): the frame showed ~15% right and ~20% down with colour garbage at the top/left. 1920×1080 is not a multiple of 16; the car's decoder apparently ignores the H.264 crop of the 8 padding rows (Lynk & Co 08 at 2160×1216 is fine). For vendor 0023 / product 0015 we now send 1920×1072 (`Prefs.carIsLynk06`, `VideoPipeline`); touches are rescaled from the car's size as before. Log: `Lynk & Co 06: sending 1920x1072 (multiple of 16)`. Hypothesis — waiting for her photo.
- **Music stutter on slow car Wi‑Fi** (Berik, Lynk & Co 08, 8.60): link 6–13 Mbit/s, audio waited up to 3 s even at the 4 Mbit/s video floor. Stall steps now go 9 → 6 → 4 → 3 → 2 Mbit/s.

## Verified

- Core tests 60/60, build OK. Not tested in a car.
