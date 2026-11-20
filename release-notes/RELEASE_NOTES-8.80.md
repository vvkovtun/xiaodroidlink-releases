# XiaoDroidLink 8.80 (versionCode 226) — internal

## What changed

- **Built-in map zooms out to level 3** (the whole of Europe on the car screen) instead of 7 in 8.79 (Vadym, 18.11: "why not the maximum?"). Far zoom levels need fewer tiles, so there is no network or memory cost. Pinch and `−` both go there; auto zoom while driving is unchanged (14–17).

## Verified

- Core tests 61/61, build OK.
- Not checked in a car: how the vector map looks at levels 3–10 is not seen yet.
