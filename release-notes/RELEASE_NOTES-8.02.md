# XiaoDroidLink 8.02 (versionCode 148)

## What changed

Crashes from Google Play vitals (Reporting API, enabled 31.10):

- BLE scan without the "Nearby devices" permission threw SecurityException in the service and the app closed (10 reports, Android 16–17, up to 7.59). Now the stage shows "Nearby devices access is missing".
- The app list sorted with loadLabel inside the comparator (n·log n calls); on Samsung with an enterprise policy that froze the UI (ANR, Galaxy A51). Labels are read once.
- Also contains 8.01 (Calls button in the dock, explained Bluetooth window).

The Android 13 crash (NoSuchMethodError, setPendingIntentBackgroundActivityStartMode) was already fixed; the reports came from 7.53 still sitting in open testing — open testing now goes with production.

## Verified

- Core tests 17/17. Not checked on a phone.
