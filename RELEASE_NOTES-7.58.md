# XiaoDroidLink 7.58 (versionCode 104)

## What changed

- Car sound: a prompt sent to the driver's headrest (STREAM_TTS on 57229) while the music is stopped makes the YU7 stop playing the phone's music (AAC in the stream) until reconnecting; STOP/START, a new capture and another prompt do not bring it back. Reproduced in the car on 2026-10-25 with a test build. Now prompts go to the headrest only while music plays; otherwise they play through the regular CarLink sound (cabin speakers). The 7.54 STOP-after-prompt step is removed. Raw PCM music on 57229 (Samsung's alternative path) was tried in the car and rejected: it plays but crackles.
- Built-in OpenStreetMap map:
  - after a route is built the map shows the whole route for 7 s, then zooms in on the car;
  - auto zoom while following, like Google Maps: 17 in town (< 35 km/h) and within 250 m of a turn, 16 up to 75 km/h or within 700 m, 15 up to 105 km/h, 14 above; zooming out at most every 6 s;
  - `+`/`−` keep the chosen zoom; "Where am I" returns to the car with auto zoom;
  - up to 8 tiles of the road ahead (1–4 km, along the route or the heading) are downloaded in advance if not cached; the tile check runs every second.
- TestHook `audiotest` (adb only) for in-car sound diagnostics.

## Verified

- Core tests: 17 passed. The emulator smoke test (88 passed, 0 failed, 2 skipped) ran on this code before the tile prefetch and the sound change; not re-run for the final build at the owner's request.
- In the car: the silence after a headrest prompt with music stopped was reproduced; the regular music path sounds clean.
- On the emulator: route overview, auto zoom, "Where am I", prefetch along the heading.

APK SHA-256: `ec6b27e4ee6b837645984d955fbb3ab9618772b1dc0804faf05fe9cf8a36ab49`

AAB SHA-256: `92f75526cda17fe4b644aff18499c66572f453a961a48205e368b959a26a9aa9`
