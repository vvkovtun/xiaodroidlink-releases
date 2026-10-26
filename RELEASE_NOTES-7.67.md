# XiaoDroidLink 7.67 (versionCode 113)

## What changed

- 9 new UI languages: German, Polish, Kazakh, Azerbaijani, Uzbek, Tajik, Georgian, Armenian, Kyrgyz (14 in total). All 720 app strings translated; translations live in `probe/assets/tr/<lang>.tsv` (key = Ukrainian text, missing ones fall back to English; `scripts/check_translations.py` lists gaps).
- Language picker on the car screen: the settings "Language" cell opens a panel with all 14 languages (they no longer fit a segment row).
- Car assistant commands in the new languages: `CarVoiceLexicon` maps word roots to the English words the existing rules already understand. All 270 guide phrases (30 per language) give the same Chinese command as the Ukrainian ones. Not tested in the car.
- Georgian is never upper-cased (Android turns it into Mtavruli); German date "Montag, 26. Oktober".
- Docs: short guides in the 9 languages with links to the full English guide; Play listings for de-DE, pl-PL, kk, az-AZ, ka-GE, hy-AM, ky-KG (uz and tg not added: Play support unsure).

## Verified

- Emulator: car screen in German, Kazakh, Georgian and Armenian (home, settings, assistant commands, language picker).
- Car voice phrases in all 9 languages on the emulator (TestHook carmatch).
- Quick emulator smoke test: 48 passed, 0 failed, 2 skipped.
- Not verified in the car; translations not reviewed by native speakers.

AAB SHA-256: `e41c9e3c9afa98f3e6b6d006e7b09ba56c3ebb4e24894f17cac64aa2bf36ee95`
