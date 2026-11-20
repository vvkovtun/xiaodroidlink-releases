# XiaoDroidLink 8.75 (versionCode 221) — internal

## What changed

- **Smart-home request with a full Quick actions widget** (Settings → "⚡ Requests: smart home, IFTTT" → "+ Add request"). Before: the request was saved, but with eight buttons already in the widget a two-line toast said "remove one on the car screen" — Android 12+ cut the text off and the button never appeared (Evgeniy, Toyota bZ3X, Xiaomi, 18.11). Now the phone asks right away which of the eight buttons the request should replace; Cancel keeps the request in the "+" list on the car screen.

## Verified

- Core tests 61/61, build OK.
- The dialog is not checked on a phone yet.
