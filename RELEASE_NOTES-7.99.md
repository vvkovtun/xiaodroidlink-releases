# XiaoDroidLink 7.99 (versionCode 145)

## What changed

Wuling Starlight 730 report (31.10, on 7.98): the car answered AuthResponse 4 (work modes not supported); 7.98 switched to mode 5 but retried on the same connection, and the car had already closed 57209 (Connection reset, then refused).

- AuthRequest work modes are now 5 (normal cast + app full screen), as CarWith — Xiaomi's own CarLink client — asks. Samsung's 769 (+ mirror window, simple launcher window) is refused by every car with CarLink 1.6 in our reports (Toyota bZ3X, GAC Aion Y Plus, Wuling Starlight 730); YU7 (1.2) and Deepal S05 (1.92) accepted 769. We only use the normal cast.
- If a car still answers 4, the app reconnects from the start with the next set (769, then 1) and remembers what the car accepted. The car shows a new code for that.

## Verified

- Built only. Not checked in a car: YU7 with mode 5 (Vadym checks in his car), any 1.6 car.
