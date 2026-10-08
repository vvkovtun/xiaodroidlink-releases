# XiaoDroidLink 7.7 (versionCode 53)

## What's new

- See when Bluetooth is off or the car is unavailable, and retry the connection.
- Get an alert if the Accessibility service stops during a session.
- Return to the car screen with one tap after using your phone.
- Restart screen casting if it stops, with phone audio restored when capture ends.

## Technical notes

Connection recovery and clearer status during a YU7 CarLink session.

- Shows when Bluetooth is off, requests Android to enable it, and offers a new
  scan or connection retry when the car cannot be found.
- Distinguishes a disabled Accessibility permission from a disconnected
  service, warns during an active session, and logs service lifecycle changes.
- Keeps the phone awake while MediaProjection supplies the car screen or audio,
  even when the phone is in hand. Adds a clear **Return to car** action on the
  car placeholder, in the phone app, and in the session notification.
- When MediaProjection ends, restores phone speaker volume and offers a new
  casting permission request. Bluetooth A2DP/HFP warnings now distinguish car
  audio from the CarLink media stream.

Local verification: 13/13 host tests; full emulator smoke test 89/89 checks
passed, with 2 optional app-dependent checks skipped. APK and AAB were
built and signature-verified. Physical YU7 validation is still required for
Bluetooth profile drops, Wi-Fi loss, and the return-to-car flow on the car
display.

APK SHA-256: `ea456410ceb05ea836e1b874bbd2a58c1f2867e27c65c5f5686c1af8aa25d332`

AAB SHA-256: `6549932057912c4da237dece678a332b0a2c664ebb2f5f5854bf2c0a585beba2`
