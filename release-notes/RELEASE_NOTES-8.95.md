# XiaoDroidLink 8.95 (versionCode 241) — internal

## What changed

- **Music after a call through the car.** Android pauses the player a moment before the app learns about the call, so the app did not remember what was playing and did not resume it (Toyota Camry 80, Yandex Music / Radio). The app now remembers the player that stopped up to 60 s before the call (ringing included) and resumes it when CarLink audio is back.
- **Car silent after the code.** In every report where the car did not answer a code, it never answered on the same Bluetooth session; 13 reports recovered only after a new connection (YU7, Jetta VS8, Aion Y, RAV4, Xingyue L, Lynk & Co, Haval). Xiaomi YU7 + Redmi Note 13 Pro+ sent 6 codes into one stuck session. Now:
  - the GATT service cache is cleared on every connection, as CarWith does (`gatt.refresh` on connect);
  - when the car is silent after the code, the app reconnects Bluetooth and asks for a fresh code (up to 3 tries) — CarWith resets the whole connection after 10 s.
- **Report:** a `rom:` line with the phone firmware (HyperOS/MIUI version, CN or global, region, build).

## Verified

- Core tests 65/65, build OK.
- Not checked in the car yet.
