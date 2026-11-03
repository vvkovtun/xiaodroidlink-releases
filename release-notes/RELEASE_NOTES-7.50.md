# XiaoDroidLink 7.50 (versionCode 96)

## What changed

- Air alert widget and GPS jamming: on 2026-10-18 near Kyiv the phone's GPS was spoofed to Lima, and the widget showed Zakarpattia. Now a position the car could not have reached (faster than 500 km/h from the last trusted place) is held off for 20 minutes; the air alert region, speed camera and charger lists keep the last trusted place, and camera warnings pause. Spoofed points follow each other smoothly, so a real point that jumps away from them and is reachable from the trusted place is accepted at once. A new place that lasts 20 minutes is accepted.
- Outside Ukraine (country from the reverse-geocoded address; Ukraine's bounding box when offline) the air alert widget stays empty.
- Backup air alert source: tryvoha.online timed out or returned HTTP 523 from 16:32 to 19:46 on 2026-10-18, and the widget showed "No data". When it fails, the oblast status now comes from ubilling.net.ua/aerialalerts (oblasts and Kyiv only, no districts).
- The air alert request runs on its own thread, so slow mobile internet no longer delays speed camera checks.

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- On the emulator: Kyiv → Lima kept "Kyiv" and logged the jump; back to Kyiv was accepted at once; a fresh start in Warsaw left the widget empty.
- The backup source was not exercised live (tryvoha.online was up). Not yet checked in the car.

APK SHA-256: `7ac9e39132bf3741a430375a07d3bcb385817e35142be24e5bba5196c896056e`

AAB SHA-256: `ef9293dc5491f10d5e41f7ce3681e2c454363cdda5b7477fb56b0a6b7aa43090`
