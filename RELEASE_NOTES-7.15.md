# XiaoDroidLink 7.15 (versionCode 61)

Faster return to the car screen, and results of the Bluetooth test on the YU7
on 2026-10-11 (full record: `docs/16-bluetooth-wifi-test-2026-10-11.md`).

## What changed

- The app keeps the car's Wi-Fi during the Bluetooth pause (up to 90 s) and for
  20 s after a dropped session, and reuses it on the next connection when the
  car reports the same access point. Before, it released the network, the phone
  joined the home Wi-Fi within a second, and Android then needed a Wi-Fi scan to
  find the car again: 17.7 s and 23.9 s in the phone's Wi-Fi log on 2026-10-11.
  If the car is not found or reports another access point, the network is
  released and requested again as before.
- Returning from the Bluetooth pause no longer goes through the auto-connect
  distance check. On 2026-10-11 the app gave up after the pause because the
  car's signal was −85 dBm and left the user without a session.

- User guides (5 languages) have a new section on connecting the car's Bluetooth
  for calls: use the notification, do not connect Bluetooth before CarLink, keep
  CarLink open on the car screen. The troubleshooting page no longer advises
  connecting Bluetooth before starting the app; the test showed the car drops it.

## Measured

From the developer's desk, car signal −71…−74 dBm, test copy of this build:

- first connection: 5.6 s, of which Wi-Fi 4.4 s (unchanged);
- return after a 90 s pause: 1.4 s, Wi-Fi reused at once (5–24 s on 7.14).

The car kept the phone on its Wi-Fi for the whole 90 s pause.

## Bluetooth calls: what the test showed

- The 7.14 path works: tap "The car's Bluetooth is not connected", pick the car
  in Bluetooth, the app reconnects 3 s after the call profile (HFP). The car
  kept HFP and call audio went through the car. One clean run.
- The car drops HFP that was connected separately as soon as CarLink connects,
  and within 6–7 s while its CarLink screen is waiting. HFP survived when the
  CarLink session started 4–5 s after it (3 of 3) and across later sessions.
- Sending `bluetooth_mac_info`, as the original apps do, did not change this;
  it was tried in the test copy and is not in this release.

## Not changed, not verified

- The first connection of a trip near a known Wi-Fi (3.5–7 s) and the 11–20 s
  the car sometimes takes to start advertising CarLink are unchanged.
- The Wi-Fi reuse was verified once, from the desk, not inside the car.
- The phone still does not connect to the car's Bluetooth by itself.

Local verification: emulator smoke suite on Android 16 — 89 passed, 0 failed,
2 skipped. It does not cover the car connection, audio or Bluetooth.

APK SHA-256: `5ff9026ac239b5ba5faa210922456ec5591d1ad09fe171ae8536f468f26c7f79`

AAB SHA-256: `370870de0e3c3d8a929261ac8068274bbae23c54e387a5234be390e671037671`
