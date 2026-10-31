# XiaoDroidLink 8.05 (versionCode 151)

## What changed

- Phone notifications are no longer sent to the car (AddNotification 36 / DeleteNotification 38) — to no car, Xiaomi included. Wuling Starlight 730 dropped the whole session 0.08 s after AddNotification (reports 31.10 on 8.03 and 8.04); the MiAuto car SDK has no such message; YU7 never showed car-native banners either — only our own banner and the Messages widget, which stay.
- Haval Xiaolong Max + Honor DNP-AN00 (report 31.10 on 8.04): the phone often got the car's GATT service list without the ICCOA service and we showed "car does not answer as CarLink" at once — the user retried 6-7 times. Now we log the services found, refresh the GATT cache and reconnect by ourselves (up to 4 attempts).
- Same Honor: apps in the phone window go black on the car while the phone shows them. The session log now records MediaProjection `onCapturedContentResize` / `onCapturedContentVisibilityChanged` to see whether Android casts the whole screen.
- docs/30-carwith-protocol-diff.md updated.

## Verified

- Core tests 17/17. Not checked in a car yet.
