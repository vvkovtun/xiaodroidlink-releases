# XiaoDroidLink 7.36 (versionCode 82)

## What changed

- Connecting no longer waits 10 s for the car's Bluetooth: the Xiaomi YU7 never connects it on its own.
- When the phone locks and Android stops screen sharing, music now pauses instead of playing from the phone speaker, and resumes in the car when sharing returns.
- Experiment: before connecting, the app knocks on the car's Bluetooth (an SDP query and a short connection to the car's service channel) and waits up to 6 s to see whether the car connects calls by itself. If it does, CarLink connects right after it.

## Verified

- Core tests: 15 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped.

## To verify in the car

- Whether the log shows "car Bluetooth answered the wake" and the handset icon turns green without touching Bluetooth settings.

APK SHA-256: `3e1c16ffee4920698b6e00bd87d4d5df55053d8d90364d0a8c66d1c5f209b673`

AAB SHA-256: `414a5b10c92d4506dcd0b54c11895b5adcef5014c3fb705c80bbc8a0118e09e9`
