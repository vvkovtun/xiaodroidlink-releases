# XiaoDroidLink 7.9 (versionCode 55)

First connection after installation is clearer. Android asks once to choose the
car Wi‑Fi network; the app now says so on the code card before the system window
appears and tells which network to tap. The wait for the car Wi‑Fi is 60 seconds
instead of 30, and the app no longer silently restarts the Bluetooth handshake
(which made the entered code obsolete). Errors distinguish "not approved" from
"did not connect within a minute".

The permission list has a single "Nearby devices" row, phone Wi‑Fi being off is
caught before connecting, and location, microphone and notification permissions
are requested once together with the first connection. The car Wi‑Fi password is
no longer written to the app log.

Local verification: the sources compile and the APK and AAB were built. Host
tests, emulator smoke checks and physical YU7 validation were not run for this
release.

APK SHA-256: `fe13eee5bea3b76e7eb918b7bd5bc55c38695efb5453e19e19186a25033f24f3`

AAB SHA-256: `efe2f139869348ecdc8b61a533a5298b834e20ded669c2ce5feb2b69762e2571`
