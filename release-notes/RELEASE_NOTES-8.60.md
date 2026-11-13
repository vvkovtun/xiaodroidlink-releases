# XiaoDroidLink 8.60 (versionCode 206) — internal

## What changed

- **Leapmotor B10: subscribe to server info before the code** (`CarSession.onServicesDiscovered`, only vendor 0028). Kichatov (8.40–8.58, vivo V2353A): the car accepts the code (`write done status=0`) and then sends nothing; our late subscription (8 s after the code) was never confirmed, the next write got 201 (Bluetooth busy) and the car dropped the link after 30 s. Now the phone subscribes right after the services are found and sends the code after the car confirms (or after 6 s). Other cars unchanged (YU7 hangs after a subscription).
- **Haval after a call through the car: no giving up while the car turns CarLink back on.** Vlad (8.59, 12.11 07:35): 33 s after the call the car did not accept Bluetooth at all (`status=147`, connect timeout); we treated it as «Bluetooth connection lost», searched for 30 s and stopped; reopened 1.5 min after the call, the new session waited only 20 s and showed «The car does not answer as CarLink». Now a Bluetooth timeout during the after-call wait means trying again every 10 s up to 5 min, and the after-call window (10 min) survives a new session (`afterCarCallUntil` is static).

## Verified

- Core tests 54/54, build OK.
- Not tested in a car.
