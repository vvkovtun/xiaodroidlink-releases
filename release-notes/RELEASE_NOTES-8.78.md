# XiaoDroidLink 8.78 (versionCode 224) — internal

## What changed

- **Built-in map: smooth two-finger zoom** (Vadym, 18.11: "like in Google"). Before, the car screen passed only the first finger to the built-in map, so a pinch did nothing; zoom was only `+`/`−`. Now the map scales smoothly with the fingers; every ×2 of finger distance loads the next tile zoom level and the pinch goes on; on release the map settles on the nearest whole zoom level (tiles exist only for whole levels). Range 11–18, as for the buttons; like `+`/`−`, the chosen zoom stays until "Where am I". A pinch is never taken as a tap or a pan. Phone maps (Google, Yandex, Waze) get the pinch as before.

## Verified

- Core tests 61/61, build OK.
- Not checked in a car or on the emulator.
