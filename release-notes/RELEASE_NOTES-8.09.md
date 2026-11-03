# XiaoDroidLink 8.09 (versionCode 155)

Includes 8.08 (internal only: several cars).

## What changed

- Favourite contacts: up to 8; with more than four the widget shows two rows of four (a low widget shows the first four).
- Car Wi-Fi (Alexey, YU7 + Fold6, Samsung kept "searching devices"; Vadym often at home on his Wi-Fi): one more WifiNetworkSpecifier request in the same login before giving up — a fresh scan, no new BLE/PIN. Applies to cars with their own access point (Xiaomi, Geely, GAC, Toyota…), not Wi-Fi Direct cars.
- Auto-connect backoff 20/20/20/40 s, then 2 and 10 min (was 20/45 s/2/10 min).
- GAC (01.11): with Bluetooth A2DP connected the car paused players a second after start; a one-time hint on the car and a phone notification to turn off Bluetooth "Audio" for the car.
- Language changed from the car screen is applied to the phone screen at once (half the phone screen stayed in the old language).
- Preview / share-to-car labels translated (ru, uk); share target no longer says YU7.

## Verified

- Core tests 17/17, translations 820/820. Not checked in a car.
