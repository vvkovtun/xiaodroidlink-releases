# XiaoDroidLink 8.67 (versionCode 213) — internal

## What changed

- **"No GPS" for the whole trip** (Vadym, 8.66 report 15.11: GPS lost at 10:05:27 and never back, though the phone used 16–54 satellites). Two bugs in `RoadSafetyServices.trustedLocation`:
  - `trust()` stamped the trusted point with the tick time, so a repeated old fix looked fresh; after a few seconds without new fixes the next real fix (~800 m on) looked like a 2-second jump → `gps jump … holding last place`. Now the trusted time is the fix's own time.
  - While holding after a jump, a real fix was accepted only if it jumped *back*; smooth real fixes waited the full 20 min (`held 20 min, accepting` at 10:25, then again at 10:26). Now any fix the car could have reached from the last trusted place (car speed × 1.5 + 300 m) ends the hold.
- **GPS-lost badge shows since when** — "10:05 · GPS втрачено · …".
- **−100 m / +100 m buttons** next to the badge, only while GPS is lost (not when the position "gave up"): move the reckoned position along the route (or along the heading without a route). `DeadReckoner.shift`, `NavigationEngine.backAlongRoute`; log `gps lost: driver moved the position ±100 m`.
- **Smaller trip card** on the built-in map: 560×116 instead of 646×154 ("the black card takes a lot of space").
- **OpenStreetMap dock icon opens the built-in map full screen** (only the dock stays), like Google Maps; tap it again or Home to go back. Editing is blocked while it is full screen so the map-only grid is never saved as a home screen.
- Docs only: Lynk & Co 06 row and bZ3X "disconnect Bluetooth" dialog analysis in `docs/31-car-connection-knowledge.md`; `scripts/car_profiles.*` know Lynk 06.

Note: "dark Google map in daytime" — the built-in map was day (by the sun); the dark one was the Google Maps app, which follows its own/phone theme and cannot be changed from XiaoDroidLink.

## Verified

- Core tests 60/60 (new: back along the route, round the corner, stops at the start). Build OK. Not tested in a car or on screen.
