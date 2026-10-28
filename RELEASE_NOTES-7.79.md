# XiaoDroidLink 7.79 (versionCode 125)

## What changed

- Phone screen on the car display (Google Maps and other apps): a one-finger drag is now passed to the phone while the finger is still moving (`continueStroke` in `CarAccessibilityService`), so the map follows the finger. Before, the whole movement was replayed only after the finger was lifted, and replayed again over the same time.
- The hold before the movement is passed too, so "press and drag" (a pin on the map) keeps working.
- Taps are unchanged (still sent after release). A second finger during a drag ends the live drag and the zoom is replayed as before.
- If Android cancels the live gesture, the rest of the movement goes the old way; after 3 cancellations live drags are turned off until the app restarts.

## Verified

- Emulator: one-finger drag went live ("UIBC live gesture done", no cancellations); taps land in the same place on 13 phone screen sizes.
- Smoke test: 88 passed, 0 failed, 2 skipped.
- Not checked: two-finger zoom (the test hook has only one finger), behaviour over the car's Wi‑Fi on the S25 Ultra.

AAB SHA-256: `45e904706affba1c036f3429ff877c4d67585763d2c75f812802dfd53f1a5f09`
