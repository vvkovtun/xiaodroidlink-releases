# XiaoDroidLink 7.53 (versionCode 99)

## What changed

- Speed cameras in Ukraine: the app downloads every `highway=speed_camera` in Ukraine from OpenStreetMap (one query by the country area, ~690 cameras, ~0.8 MB) and keeps it on the phone; refreshed once a day, the old base is kept when the refresh fails. Outside Ukraine — cameras within 60 km as before.
- Direction of the camera: the query also returns the roads the cameras sit on and their neighbouring nodes. `direction=forward/backward` (how all М-05 cameras are tagged) or a camera on a one-way carriageway now gives the direction of traffic it measures; cameras for the opposite carriageway are skipped. Before, `forward/backward` was ignored, so both carriageways were announced. A numeric `direction` is now only the road axis (mappers use it both for where the camera looks and where traffic goes; the old code assumed one and dropped cameras in our direction).
- The camera update has its own thread and waits up to 70 s / 200 s for Overpass (was 4 s — the server now answers in 30–40 s, so the base was often not updated), with the mirror as a fallback.
- Ukrainian voice: numbers in words ("Обмеження швидкості п'ятдесят") — TTS read "Обмеження 50" as an ordinal.
- Known gap: camera М-05 39+140 is not in OpenStreetMap.

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- Emulator: "radars updated: 685" with the country query. Direction logic checked on real data (М-05 pairs: one ~220°, one ~40°). Not checked in the car.

APK SHA-256: `b3f23d8053af22b52272b79f6bc230f6d368fa7ef4487ba6b54063a2941ae4cf`

AAB SHA-256: `f678beb84d0aaecbfb484c424afd1f77f543d84fb52f4ebdf78b162ffc883d17`
