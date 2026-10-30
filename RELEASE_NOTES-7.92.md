# XiaoDroidLink 7.92 (versionCode 138)

## What changed

Vadym: "Expand" like YouTube, for every app, and on the map widget too ("handy while driving"); "Exit" goes back where you came from.

- The phone-mode rail has six buttons: Dashboard, Maps, Music, Rotate, Expand, Back. "⛶ Expand" works for any app: the rail hides and the app fills the whole car screen (phone status and navigation bars cropped, fitted without cropping the app). "✕ Exit" in the top-right corner hides after 10 s and shows again on a touch; the wheel Back button also leaves. Switching to another app on the phone leaves full screen by itself. In YouTube Expand also asks YouTube for its own full screen, as before; "Rotate" is dimmed there (YouTube is always landscape).
- The map widget bar has "⛶ Expand" second from the top (only when the widget shows the phone map): the phone map opens on the whole car screen. Exit returns to the dashboard; Expand from the rail returns to the rail.
- Map bar labels stay visible with nine buttons (label threshold 120 → 104 px).

## Verified

- Emulator (S25 size) with Google Maps: Expand from the rail and from the widget, touches on the expanded map (Gas chip), Exit, auto-exit on leaving the app, a portrait app on full screen, return to the dashboard / rail. Quick smoke 49/0/2. Not checked in the car.
