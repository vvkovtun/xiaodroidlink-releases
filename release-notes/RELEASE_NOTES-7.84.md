# XiaoDroidLink 7.84 (versionCode 130)

## What changed

After the 28 October test on 7.83 (`capture/probe-2026-10-28-783.log`): one wheel command worked («Відкрий багажник»), then 12 attempts in a row failed — the first with error 11 three ms after the car-reply recognizer was destroyed, the rest with error 7: Google got 5 s of loud audio (10 dB) and returned "no speech detected" (online recognizer, uk-UA).

- After stopping the car-reply recognizer, the wheel recognizer starts 400 ms later; the retry after "heard nothing" also waits 400 ms.
- Retry also after error 11 (server disconnected) and error 9 (no microphone access yet).
- `EXTRA_SPEECH_INPUT_*_SILENCE_LENGTH_MILLIS` passed as int: the Google service read the long value as 0 (ClassCastException in the service log), so the 2 s pause was ignored.
- Recognizer error log adds quietest / average RMS, callback count and whether speech started.

## Verified

- Builds. Not run: smoke test, car test. Root cause of the error-7 series is not confirmed.

AAB SHA-256: `2a2b8fea5919c7a79ada7b3f74532ac4cf927c3bed6d4f1c6033d3f0c82946b7`
