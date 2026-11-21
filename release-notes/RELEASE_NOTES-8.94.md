# XiaoDroidLink 8.94 (versionCode 240) — internal

## What changed

- **Chosen map opens right away.** Picking a map in the car's «Choose a map» window only saved the setting; the map widget mirrors the phone screen, so it kept showing the previous map (Google chosen, Waze shown) until the next return to the home screen. Now the chosen phone map is brought to the front immediately (also after «Custom…»), and the choice is logged (`map chosen in the car: …`).
- **Bigger map tiles.** The window used the 8-per-row app grid; a tap 30–40 px past the edge of the Google tile landed on Waze (Xiaomi YU7 report, taps at x≈420 while Google ends at x=379). Map tiles are now 6 per row and taller, with bigger icons.
- **Pages.** More than 12 tiles (6×2, «Custom…» last) — ‹ › and «1 / 2» in the header.

## Verified

- Core tests 65/65, build OK; rendered on the emulator (few maps, and 2 pages with 12 test maps).
- Not checked in the car yet.
