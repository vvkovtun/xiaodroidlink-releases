# XiaoDroidLink 7.14 (versionCode 60)

Calls and ChatGPT voice through the car. The YU7 rejects music over Bluetooth
(A2DP) from this phone, so music travels over Wi-Fi with the picture, while
calls and assistant voice need the Bluetooth call profile (HFP). The phone's
Bluetooth log showed that the car itself drops HFP when CarLink audio is
already running, and a manual test in the car on 2026-10-10 worked only in
this order: CarLink audio off, connect the car's Bluetooth, connect the app,
turn CarLink audio on.

The app now follows that order by itself:

- If the call profile is connected when the picture starts, audio over CarLink
  starts 10 s later instead of immediately. Without Bluetooth it starts at once,
  as before.
- If the call profile is not connected, the notification says "The car's
  Bluetooth is not connected" and explains that calls and ChatGPT play from the
  phone. Tapping it ends the CarLink session and opens Bluetooth settings; once
  the call profile connects, the app reconnects in 3 s. If nothing connects in
  90 s, it reconnects anyway.
- The notification about the missing music profile (A2DP) no longer appears
  while music goes over CarLink.

The 10 s delay is a guess, and reconnecting right after the session is dropped
was not tried in the car; both need validation on the YU7. The delay reacts to
any connected call-profile device, not only the car.

The user guides now explain how to install from Google Play (closed testing:
join the testers group first).

Local verification: the emulator smoke suite on Android 16 passed on this build
(89 passed, 0 failed, 2 skipped: ChatGPT and music control need a real phone).
The Bluetooth paths cannot be exercised on the emulator. Not validated on the
car.

APK SHA-256: `ed98a16c4e330193843faacf25d082c789f567faf4216d8e9d32b89c5d7905e3`

AAB SHA-256: `dd2fcf0d4720603568290623057922dbccdd2caa3e2180771a0d3aaa0582edf0`
