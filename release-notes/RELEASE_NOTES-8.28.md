# XiaoDroidLink 8.28 (versionCode 174)

Includes 8.27 (production).

## What changed

- Car Wi-Fi join: when an attempt fails and the car SSID is in none of the phone's scan results, the next attempt uses `WifiNetworkSpecifier.setIsHiddenSsid(true)` without the BSSID filter, so Android probes for the network by name. Logged as `car network invisible to Android: next attempt asks for it by name (hidden SSID)` and `AP join … hidden`. Case: Alexey, YU7 Max + Fold6 / Xiaomi — PIN accepted, the car reports DIRECT-Xiaomi_YU7_Max_… on 5745 MHz, two Android phones never see it in scans, an iPhone that knew the network joins by itself. Hidden SSID is a hypothesis, not confirmed.
- Cars whose network is visible are unaffected (the first attempt is unchanged).

## Verified

- Core tests 47/47, translations 826/826. Not checked in a car.
