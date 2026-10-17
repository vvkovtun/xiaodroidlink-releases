# XiaoDroidLink 7.44 (versionCode 90)

## What changed

- Voice route fixed. In 7.43 the car's microphone worked and Google's speech recognizer heard the address, but with sound coming from the car (not the phone's own microphone) it hands over the text only when listening is stopped, so the app waited 15 seconds and got nothing. Now listening stops 0.7 s after you finish speaking (it waits if you keep talking), and partial or per-phrase results are used as a fallback. The address search starts in about a second after you stop speaking.
- Google Play uploads to internal testing are now done by a script with a service account (`scripts/play_upload.py`).

## Verified

- Core tests: 16 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped (a first run failed once on the known emulator rotation issue).
- Voice route on the emulator through the same path as the car microphone: the phrase "Київ, Хрещатик 22" was recognised in about 4 seconds and the address list was shown.
- Not yet checked in the car.

APK SHA-256: `1efa1ed0972205dbbb206895b7cee4cfdef7420dbde1b3e6a6f610575829401d`

AAB SHA-256: `7d10f5e7a5ed3c2c470a8188def12ad76f6daf0ca343a1517d022c129ad33cfb`
