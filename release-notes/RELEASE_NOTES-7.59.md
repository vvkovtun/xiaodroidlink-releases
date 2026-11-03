# XiaoDroidLink 7.59 (versionCode 105)

## What changed

- Car sound, root cause: after our `NotifyAudioPlayerState` STOP (1) for the cast music the YU7 does not play our AAC again for the rest of the session; START, PAUSE/RESUME, a new capture or a prompt do not bring it back, only reconnecting. Proven in the car on 2026-10-25 (STOP → START while music played: silence). STOP was sent by Play pressed in the car (since 7.54), after headrest prompts (7.54), on phone unlock and when the audio capture restarted. Now music gets one START per session, then only PAUSE/RESUME; STOP is never sent during a session (Samsung does not send the music player state to cars with SDK < 1005001 at all; the YU7 has v1.2.14).
- Headrest prompts are back for every case: the 7.58 rule (speakers while music is stopped) was based on a wrong guess and is removed.

## Verified

- In the car with a test build: Pause → Play from the car screen keeps the sound; Pause → headrest tone → Play keeps the sound.
- Core tests: 17 passed. Emulator smoke test not run for this build.

APK SHA-256: `86174e5a55b58abb0727136bc3f5730e7f8984cfce586726708a1dbfc0ab2251`

AAB SHA-256: `88e1b89a86031bd84fbb8a8fe8f1ac6fe685699e3ffd476ee38ee4b1cfdff473`
