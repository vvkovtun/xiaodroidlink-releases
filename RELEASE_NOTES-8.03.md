# XiaoDroidLink 8.03 (versionCode 149)

## What changed

Reports 31.10 from Wuling Starlight 730 (8.00), GAC Aion Y Plus and Deepal S05 (7.99), Haval Xiaolong Max (8.00); full comparison with CarWith in docs/30-carwith-protocol-diff.md.

- Cars that choose app-full-screen mode (AuthResponse work modes 4) show the phone's apps as icons in their own menu and send invoke_app when the user taps one. We now send app_state_changed only in answer to invoke_app — 8.00 sent it unasked and Wuling dropped the session in 0.1 s — as SEND_SYNC, with the state by the requested action (START/UPDATE → STARTED, PAUSE → PAUSED, RESUME → RESUMED, STOP → STOPPED) and the display mode the car asked for, visible region 0,4 – w,h−4, as CarWith.
- Wi-Fi Direct (Haval): server info carried port 0, so the app still dialled ":0"; port 0 now means "no port" and AUTH runs on the group owner. The log lists the server info keys.
- Also contains 8.01–8.02 (Calls button in the dock, crash fixes).

## Verified

- Core tests 17/17. Not checked in a car. YU7 does not choose mode 4 and never sends invoke_app — Vadym checks YU7 before production.
