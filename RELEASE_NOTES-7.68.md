# XiaoDroidLink 7.68 (versionCode 114)

## What changed

- Car assistant, from the car test on 26 October 2026 (`capture/probe-2026-10-26-1954.log`):
  - turning off windshield heating now says 关闭前除雾 (the car's own word; 关闭前挡除雾 was silently ignored);
  - turning off rear seat heating now says 把后排座椅加热关掉 (关闭后排座椅加热 was silently ignored);
  - "ви б не …" (how the recognizer hears "вимкни") now means "turn off" — it turned the rear heating on;
  - "світло червоне" (light + colour) sets the ambient light colour instead of the reading light;
  - white ambient colour only from whole words, so "більше світла" stays the cabin light.
- Fixed old matching bugs found on the emulator: French "température 22" did nothing, Spanish "limpiaparabrisas"/"lavaparabrisas" turned on windshield heating, Polish "nastrojowe" read as red.
- Commands list (phone, car screen, guides in 5 languages, all 14 languages): temperature as a number and ambient light colour added, both verified in the car.

## Verified

- Emulator: all 429 guide phrases in 14 languages give the same Chinese command as the Ukrainian ones (TestHook carmatch); the logged phrases give the new commands.
- Smoke test not run (Vadym: nothing to test there).
- New off phrases not yet verified in the car.

AAB SHA-256: `a885a47e94abf954b2a58cf420879045c2283eaf60f136f12d7449ca9704e63f`
