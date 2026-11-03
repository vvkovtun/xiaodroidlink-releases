# XiaoDroidLink 7.56 (versionCode 102)

## What changed

- Built-in OpenStreetMap map, reworked:
  - the same button strip as next to the phone map: Address, Route, Home, Work, Where am I (follow the car again) and Compass (north up or direction of travel up); `+`/`−` stay on the map and no longer stop following the car or reset the chosen zoom;
  - night map: tiles are inverted with the hue kept (dark ground, light labels, blue water, green parks) instead of being dimmed fourfold;
  - a smaller Google-style arrow; while driving heading-up it sits below the centre so more of the road ahead is visible; no thin lines at tile seams;
  - the tile cache keeps everything already seen, up to 300 MB with no expiry (it was 600 tiles); without a connection a missing tile is drawn from a cached coarser zoom; after a zoom change the old tiles stay scaled until the new ones arrive. Nothing is bulk-downloaded ahead: the tile.openstreetmap.org policy forbids it.
- Driving without GPS (jamming or spoofing, `DeadReckoner`): when no satellite fix has come for 6 s, the fix froze while the car moves, or a spoofed jump is held, the arrow turns grey and keeps moving at the car's speed from CarLink. With a route it follows the route line from the current segment (U-turns and crossings do not pull it back), so turn distances and voice directions continue; without a route it goes by heading plus the phone's gyroscope around the gravity axis (the phone may lie on the charger), and stops after 3 min or 3 km with "position unknown". A note at the bottom of the map says GPS is lost. Cell-tower fixes no longer count as GPS. Trip distance keeps counting.
- The live phone map no longer covers speed camera warnings, message banners, problem banners and hints: those panel rectangles are drawn again on top of the phone layer.

## Verified

- Core tests: 17 passed (new: moving along a route without GPS, including a U-turn route). Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- On the emulator: night and day map, button strip, zoom while following, GPS loss with and without a route (route followed through the turn, banner shown), banners above the live phone layer.
- Not checked in the car or under real jamming; the gyroscope was not checked on a real phone.

APK SHA-256: `a9347edb8bbb63dfabd055ce108a5858e661993085333fc09031d8bd3f71f7d5`

AAB SHA-256: `f8a44ba3df295755a850bfd503c603988387ef2ccdbb810b9b3f2c654f759bf9`
