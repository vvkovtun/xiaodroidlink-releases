# XiaoDroidLink 8.04 (versionCode 150)

## What changed

GAC Aion Y Plus on 8.03 (report 31.10 with two photos from the new report form): connected without a code, video at 1920×976, but the car's phone tab "SM-S928B" in its app menu was empty, so there was nothing to tap and no invoke_app.

- In the car SDK (MiAuto 0.1.1, `ControlManager.getAppDetailInfo`) app id 1 is the client's own logo and name (`onProductIconReceived`): the car always adds 1 to the detail request and never lists it as an app. XiaoDroidLink had id 1. Now the logo/name is id 1 and the XiaoDroidLink app is id 1001; the detail answer carries both (total 2).
- The car arms a 3 s timer when it starts an app and pauses the cast unless STARTED/RESUMED arrives; we answer invoke_app at once (8.03).
- docs/30-carwith-protocol-diff.md updated.

## Verified

- Core tests 17/17. Not checked in a car. YU7 never asks for the app list — not affected.
