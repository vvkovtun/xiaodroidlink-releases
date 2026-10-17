# XiaoDroidLink 7.43 (versionCode 89)

## What changed

- Voice route: a microphone button on the map widget (built-in map, when no route is running) and in the address field of the route planner on the car screen. Tap it and say the address; the screen shows "Say the address…" and the music pauses. The recognised text goes into the same search as "Find": with Google Maps or Waze the route starts right away, with the built-in map you pick from the found addresses. The app asks the car for its microphone and passes its sound to the phone's speech recognizer; if the car's microphone does not answer, the phone's microphone is used.
- Music keeps playing when the car switches to its own menu. Since 7.42 the car shows the song in its own player and plays CarLink sound there too, so the old pause is gone.
- "Disconnect" now tells the car first, as Samsung CarLink does: CarLink simply closes on the car screen instead of showing a lost connection.

## Verified

- Core tests: 16 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped.
- In the car (test builds, 2026-10-17): music continues in the car menu; clean disconnect; the car microphone delivers speech while the phone reports an active voice assistant.
- Not yet checked in the car: recognising an address spoken into the car's microphone (on the emulator the recognizer starts in Ukrainian and returns to the keyboard when it hears nothing).

APK SHA-256: `57c8c2adfc72b35cc4ab4fd3955caae87f40e5ab91206b158dc6834fe6d8bb05`

AAB SHA-256: `e74cc43ea4b8164daab62cc66fa51ef3f32aa6f293c57a3f3403815a72d8ff00`
