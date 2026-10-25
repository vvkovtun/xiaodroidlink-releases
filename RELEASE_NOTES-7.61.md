# XiaoDroidLink 7.61 (versionCode 107)

## What changed

- Car voice phrase matching: short English words ("off", "stop") are matched as whole words, so the French "coffre" (trunk) is no longer read as "off": in 7.60 "ouvre le coffre" (open the trunk) closed it instead. Added "liseuse" (reading light), "ventila…" (Spanish seat ventilation), "bonnet", "maletero delantero".
- The car banner shows the catalog name of the command, or the driver's own words for commands outside the catalog (e.g. "вимкни двірники"), instead of the Chinese phrase.
- User guide (all five languages): new section "Car assistant in your language" — how it works, how to turn it on, how to use it, the full list of supported phrases and the limitations.

## Verified

- All 197 example phrases from the guide tables (Ukrainian, English, French, Spanish) give the expected Chinese command on the emulator (TestHook carmatch).
- Emulator smoke test not run for this build (at Vadym's word); 7.60 passed 88/0/2 with the same code except the phrase matching.

APK SHA-256: `0d3833f85256bf458af68838fe1166c5070e4ebe2dc02ce374feaa325a8209c1`

AAB SHA-256: `9719802290203c910ad3eb33c8793d9c291c94ed0e4e53abc501d261f2fe1588`
