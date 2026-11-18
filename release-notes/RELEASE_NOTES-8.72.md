# XiaoDroidLink 8.72 (versionCode 218) — internal

## What changed

- **Built-in map without internet says so** instead of a black map. When OpenStreetMap tiles are neither cached nor downloadable, the car shows "The map isn't loading — no internet. Fix the internet or choose another map"; with a phone map chosen and the phone in hand — "…Put the phone down or tap the screen to bring back the phone's map". Case: Lynk & Co 10 EM-P + Honor (17.11) in a region where mobile internet opens only whitelisted sites — the phone's Yandex Maps worked, our map stayed black every time the phone was picked up.
- Confirmed cars in the README: Geely Xingyue L, Changan Nevo Q05, Lynk & Co 06 and 10.
- TestHook `shot` gets `mapoffline` / `inhand` extras.
- New texts in 15 languages.

## Verified

- Core tests 61/61, build OK.
- Emulator: car frame with the offline map text (phone in hand and not) via TestHook `shot`. Not checked in a car without internet.
