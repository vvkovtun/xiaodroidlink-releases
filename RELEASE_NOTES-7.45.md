# XiaoDroidLink 7.45 (versionCode 91)

## What changed

- Find a song by voice. A microphone button on the music card (medium and large sizes) listens through the car's microphone, and the recognised text goes to the music player: through its MediaSession `playFromSearch` when the player supports it (YouTube Music does), otherwise as a standard `MEDIA_PLAY_FROM_SEARCH` request to YouTube Music. Music pauses while listening; a second tap cancels.
- Dock on the left. A new phone setting, off by default, puts the apps in a column on the left of the car screen, so widgets use the full height. Apps, Settings, the widget catalog and the route planner open to the right of the dock.
- The Calls button next to the clock is now a large pill with a handset and the word "Calls": green when calls go through the car, grey and crossed out when they stay on the phone. The whole button is tappable.
- Voice address: parts of the phrase are now collected and the text is handed over after 1.5 s of silence (was 0.7 s). The 2026-10-17 trip log showed 7.44 hearing only "Київ 34" from a longer address.
- Play release notes can be uploaded in several languages (`scripts/play_upload.py` picks up `PLAY_RELEASE_NOTES-X.Y.<lang>.txt`); only languages that have a Play store listing are sent.

## Verified

- Core tests: 16 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped.
- Voice song search on the emulator: the phrase went through the car-microphone path and the request reached YouTube Music (playback not checked: YouTube Music is not signed in on the emulator).
- Left dock, panels and touches checked on the emulator.
- Not yet checked in the car.

APK SHA-256: `c11fbc2049531b16cac17c6d99b268270080f5301c63f2a63938cace6e6a618e`

AAB SHA-256: `2a86412b240c9376f268e5420f31de22db7ac2ce1eb213a05ac77e6df14e8a71`
