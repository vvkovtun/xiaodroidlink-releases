# XiaoDroidLink 7.78 (versionCode 124)

## What changed

- Russian UI language (15th): car and phone menus, `assets/tr/ru.tsv` (729 strings), route prompts in Russian, short guide `RELEASE_README.ru.md`. Voice: «немножко» (window a little), «искусственный интеллект», «чат джипити» recognized.
- Clock on the car screen uses the phone's time zone.
- Weather uses the app's live location (or the last known one), refreshes after 20 km, place name in the app language; until the location is known no place is shown and it retries every 2 minutes.
- After the 27 October trip on 7.77 (`capture/probe-2026-10-27-1852.log`): saying "commands" / "what can you do" after the wheel button opens the commands list on the car screen (15 languages); "washer glass" turned on the windshield defog — now the washer; "Hello" turned on the reading light (German «hell») — now nothing; misheard «前途开了» translated as front defog on.

## Verified

- Emulator: 588 guide phrases in 15 languages; car screen in Russian (home, language picker); clock in the phone's time zone.
- Smoke test: 88 passed, 0 failed, 2 skipped.

AAB SHA-256: `caa61f07ce2cc4b6ccde763158cf34c3861992a88bffa86be8c36db76cbe8db2`
