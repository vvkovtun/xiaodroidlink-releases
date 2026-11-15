# XiaoDroidLink 8.66 (versionCode 212) — internal

## What changed

- **GPS in the background** (Vadym, 8.64 report 14.11: "no GPS" on the way from Kyiv while Google Maps had a fix; log `gnss: used=0`, repeated `gps lost`). CarLinkService had only the `connectedDevice` foreground type, so Android 14+ gave it no satellite fixes while the phone was locked or another app was on top. Now `FOREGROUND_SERVICE_LOCATION`; CarLinkService `connectedDevice|location`, ScreenCaptureService `mediaProjection|location`. If Android refuses the location type (background start without the accessibility service), the service falls back to `connectedDevice` and retries when the app is opened (`CarLinkService.appVisible()`). Log: `foreground: connectedDevice+location`. No background-location permission.

## Verified

- Emulator (Android 16): background start without accessibility → refused, fallback OK; after opening the app types=0x18; with the accessibility service on → 0x18 straight from the background. Build OK. Not tested in a car.
