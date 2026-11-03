# XiaoDroidLink 7.77 (versionCode 123)

## What changed

- Speed cameras abroad: the whole country you are in is loaded (Overpass `is_in` → country area by ISO3166-1), refreshed daily; every 60 km a short query checks the country is the same, and crossing a border loads the new one. If the server can't return the whole country (busy, too large, mirror without areas), cameras within 100 km (was 60 km), refreshed every 60 km (was 40 km). Ukraine unchanged. Old cache (country flag only) is read as Ukraine.
- Voice warnings (cameras, air alert, route prompts, arrival): if the phone has no voice for the app language (e.g. Kyrgyz, Tajik), they are spoken in English (`Tr.inEnglish`) instead of a beep. Reading messages aloud keeps the old behaviour (no English voice for someone else's text).
- Guide (5 languages): warnings go to the driver's headrest in the app language, English if there is no voice; cameras for the whole country, abroad too.
- Test hook `warnsay`.

## Verified

- Overpass: whole France 3968 cameras, 1.2 MB, 94 s; Ukraine 686 cameras, 49 s.
- Emulator: warnings in uk spoken in Ukrainian; ky and tg (no voice) spoken in English; en in English.
- Smoke test: 88 passed, 0 failed, 2 skipped.
- Not yet tested on a real trip abroad.

AAB SHA-256: `2288b1477062a9d8a083005f599e1a9b1512d57b0b61781f147742148d731088`
