# XiaoDroidLink 8.76 (versionCode 222) — internal

## What changed

- **Haval Xiaolong Max: calls never pause CarLink.** Vlad's test of 8.75 with "Calls through the car" on (18.11, three calls): while CarLink was paused the car never connected the call Bluetooth (25–35 s), and after the pause the car's CarLink stayed busy for 2–4 minutes, so the map disappeared. Now on Haval a call always goes to the phone speaker, CarLink stays on screen, and the "Calls through the car" switch is gone from the car and phone settings. Jetta VS8 and Camry 80 keep the pause (the car takes the call in 4–5 s).
- **Smart-home requests can be edited** (Settings → "⚡ Requests: smart home, IFTTT"): tap a request → Edit / Delete. Edit opens the same form already filled in; the Quick actions button is updated in place (Evgeniy, 18.11).

## Verified

- Core tests 61/61, build OK.
- Not checked in a car or on a phone.
