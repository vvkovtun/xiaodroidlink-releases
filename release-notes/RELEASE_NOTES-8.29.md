# XiaoDroidLink 8.29 (versionCode 175)

Includes 8.28 (internal).

## What changed

- VPN check: `CarSession.vpnCoversApp()` looks at the app's own active network (`ConnectivityManager.getActiveNetwork()` is per-UID), not at every network on the phone. A per-app VPN that does not include XiaoDroidLink, or a VPN with XiaoDroidLink excluded, is no longer blamed.
- AUTH: if the car answered with `ECONNREFUSED`, the network to the car works, so the VPN error is not shown and the normal retries continue (`Auth.refused`).
- Main screen warning and the `vpn (bad)` line in reports use the same check.
- Case: Mikhail, Jetta VS8 + realme RMX5051, VPN proxy for 6 selected apps — on 03.11 20:21 the car refused port 57209 twice and the app stopped with "VPN blocks the connection"; 35 s later it connected with the same VPN on.

## Verified

- Core tests 47/47. Not checked in a car or with a VPN on a phone.
