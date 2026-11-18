# XiaoDroidLink 8.73 (versionCode 219) — internal

## What changed

- **Toyota bZ3X: the phone asks the car to show the picture itself.** The bZ3X firmware (F3, CarLink v1.6.4) puts the phone's apps into the all-apps menu only when the car's language is Chinese (`AY5TShortcutConfig.isSupportLink = !isForeignVersion()`), so with Russian or any other language there was nothing to tap and the car waited forever. A tap in that menu ends with our `app_state_changed` STARTED + show, and the car's CarLink accepts it without the tap (`PhoneMgr.onAppStateChanged` → `startForeSurface` / `backToForeground`). For bZ3X (0041/0010) only: 3 s after the car takes our app details, if it has not opened us, the phone sends that state itself. Log line: `bZ3X: car did not open us`. Case: Evgeniy Chura, bZ3X with Russian language (photos 18.11).

## Verified

- Core tests 61/61, build OK.
- Path checked against the decompiled bZ3X firmware. Not checked in a car.
