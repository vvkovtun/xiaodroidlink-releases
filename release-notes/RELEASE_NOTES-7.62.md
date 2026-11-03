# XiaoDroidLink 7.62 (versionCode 108)

## What changed

- Car voice, battery and range: "battery level" / "range" (also in Ukrainian and Russian) asks the car "告诉我电池电量" / "我的车还能开多远", the phone listens to the spoken answer in Chinese and shows the numbers ("Battery 72%, range 350 km"); the battery goes into the widgets (CarLink never sends it). Chinese numerals are converted ("百分之六十五", "三百二十公里"). Also as Quick action buttons.
- Driver / passenger: seats, windows, temperature and the reading light get 主驾 / 副驾 when the driver says "driver" or "passenger" (the car otherwise picks the zone the phone's voice comes from).
- Ambient light colours (氛围灯调成…色, as in the car's menu), plain "light" turns on the cabin light.
- More verbs: Ukrainian and Russian words for off/close (виключи, відключи, вируби, зупини, погаси, зачини, стоп, выключи, закрой…) and Russian noun roots (окно, сиденье, руль, дворники, свет…).
- Fixes from the 2026-10-25 trip log: "Не почув адреси" (shown when nothing was heard) is now a neutral "Didn't catch that"; "підігрів руля" turned on seat heating; "ви не підігрів…" (misheard "вимкни") turned heating on; "клоузи Windows" opened the windows.
- User guide: battery/range, driver/passenger, colours and the verb list.

## Verified

- Emulator: all 197 guide phrases unchanged, the trip phrases and the new verbs give the expected commands; reply parsing tested on sample answers (TestHook carmatch "reply:…").
- Quick emulator smoke test: 48 passed, 0 failed, 2 skipped.
- Not verified in the car: driver/passenger, colours, battery and range answers.

APK SHA-256: `89837cb1a377aa038c9b88c57d2eda466d63acd07f7cca0fa6640e80908dc970`

AAB SHA-256: `c3ac77cb2f2a3b51a50ab4edee619f6657bfabefd204af37e59a8a771bf509e2`
