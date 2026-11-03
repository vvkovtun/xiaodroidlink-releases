# XiaoDroidLink 8.20 (versionCode 166)

Includes 8.19 (production).

## What changed

- Map widget "fill" (Jetta / vivo, 03.11 «Яндекс навигатор очень крупный, плохое качество»): a portrait phone map is zoomed at most 1.7x of "fit" instead of 2.5-3x, centred with moderate margins (taps in margins are ignored). Landscape phone maps (YU7 Google ~2x) keep exactly the previous crop.
- Yandex yellow arrow detection accepts a blob only near the centre of the map (it jumped to corners and pulled the view).
- Car Wi-Fi (Alexey, YU7 + Fold6: iPhone sees DIRECT-Xiaomi_YU7_Max_306184, Samsung never finds it): after an unsuccessful request the log records whether the phone's scan results contain the car SSID and with which BSSID/frequency/RSSI/age (no password, no other networks). Only if the SSID is seen with another BSSID than SERVER_INFO, one more request by SSID + WPA2 without the BSSID filter.

## Verified

- Core tests 47/47, translations 822/822. Not checked in a car.
