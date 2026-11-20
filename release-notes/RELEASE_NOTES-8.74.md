# XiaoDroidLink 8.74 (versionCode 220) — internal

## What changed

- **Calls from the car screen always dial right away** (favourite contacts, quick action, voice "call …"). Before, without the car's Bluetooth call profile the app did not call and opened the Bluetooth picker ("pick the car and call again"). That rule came from 7.71, before the phone speaker fallback existed (8.45). Now: car Bluetooth connected — the call goes through the car; not connected — phone speaker plus a hint that blocks nothing: "Calls go through the phone — tap Calls in the dock".
- **Haval Xiaolong Max, Jetta VS8, Toyota Camry 80:** these cars drop the call Bluetooth while CarLink runs and never take it back, so the picker went in circles (Haval, Vlad, 18.11: pick the car → "connecting" → dropped after 6 s). Now the call starts at once: with "Calls through the car" on, CarLink pauses and the car takes the call (Haval up to 30 s); off — phone speaker.

## Verified

- Core tests 61/61, build OK.
- Not checked in a car.
