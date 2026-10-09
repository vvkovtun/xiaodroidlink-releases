# XiaoDroidLink 7.10 (versionCode 56)

Reconnection after walking away from the car and coming back now works without
pressing Disconnect and Connect. When the saved sign-in is used and the car
Wi‑Fi is not in range yet, the app keeps retrying (up to 10 times) instead of
stopping with an error. When the Wi‑Fi comes up too late and the car refuses
the sign-in, the app starts a new handshake at once instead of waiting 20 s.

Diagnostics has a new "Copy log" button: it puts the last part of the app log,
with the app version and phone model, on the clipboard. The error shown when
the car Wi‑Fi fails to connect no longer claims the network was not approved
if it had been approved before.

Local verification: the sources compile and the APK and AAB were built. Host
tests, emulator smoke checks and physical YU7 validation were not run for this
release.

APK SHA-256: `b58565b8a6dea0f99a094e9415a5b3ebb217ca4fbd4c750a9efbbe97c6e944ea`

AAB SHA-256: `46f812a15b47893cb9cf27d0d8468fdcb012a0c97e4826ee4ba1acec93436631`
