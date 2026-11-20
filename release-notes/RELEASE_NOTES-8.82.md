# XiaoDroidLink 8.82 (versionCode 228) — internal

## What changed

- **Black phone picture is explained on the car.** Screen casting can work (video to the car, touches back) while Android gives an all-black picture of the phone. The phone map in the widget then showed a black field. Now a 240 px copy of the phone frame (already taken every 0.4 s) is also checked: if it stays fully black for 6 s while the phone map is on the home screen, the layer is hidden and the map widget lists the known causes (one app chosen in the casting request, the phone hides content while casting, the map app forbids capture, another app already records the screen). The picture comes back by itself. Log line `phone screen picture is all black`, report line `phone screen black (bad)`. Case: Kirill, Xiaomi YU7 + Honor X9b (Android 15), 19.11.
- **Navigation info sent like CarWith 4.0.14.** `NotifyNavigationInfo` now carries fields 1–8 only (no field 9), the turn icon as PNG at its own size (was scaled to 160 px), and the built-in OpenStreetMap navigation now sends its turn arrow too (was text only). YU7 HUD shows arrows only from its own navigation, so this is for other cars' clusters.

## Verified

- Core tests 61/61, build OK, translations 938/938.
- Not checked in a car or on a Honor phone.
