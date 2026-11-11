# XiaoDroidLink 8.59 (versionCode 205) — internal

## What changed

- **Toyota bZ3X: 8.58 change reverted.** Chura (8.58, 11.11 17:11): the car answers the normal-cast-only request (work mode 1) with `result=4` (workmode err), `workModes=0` and never connects. Back to the 8.55 behaviour: the cast starts, the picture opens from the ICCOA tile.
- **After a call through the car: no hanging «Waiting…»** (`CarSession.SERVICE_WAIT_AFTER_CALL_MS`, `serviceWaitSlow`). Vlad (Haval, 8.58): after a 16 s call the car brought its CarLink BLE service back only 3 min 20 s later; we gave up at 90 s and the background scan picked the car up 96 s after that. Now: 10 s of quick retries (1.5 s), then the phone shows «The car is still turning CarLink back on after the call — we'll connect by ourselves» (10 languages) and checks the car every 10 s for up to 5 min, so CarLink returns ≤ 10 s after the car is ready.

## Verified

- Core tests 54/54, build OK, translations complete.
- Not tested in a car.
