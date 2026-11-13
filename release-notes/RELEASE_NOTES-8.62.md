# XiaoDroidLink 8.62 (versionCode 208) — internal

## What changed

- **Built-in navigation goes quiet when CarLink ends** (`NavigationService.tick`). Vadym (8.60, 13.11, Hatne): GPS was jammed, dead reckoning pushed the arrow along the route ~450 m away from where the car really stood, so arrival never fired; after the car was switched off the route stayed alive in the app process (kept by the accessibility service) and kept talking and polling GPS every 2 s. Now, while CarLink is not running, navigation neither speaks nor reads the location; if the car reconnects within 10 minutes the route continues, after that it is dropped.
- **Shorter log** (`probe.log`): `CAR gear` is written only when the gear or the speed in 10 km/h steps changes (it was almost every second while driving); `gnss:` every 3 minutes instead of 30 s; standing with weak GPS no longer writes a `gps lost` / `gps back after 0 m` pair every minute.

## Verified

- Core tests 56/56, build OK.
- Not tested in a car.
