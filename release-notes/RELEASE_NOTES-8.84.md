# XiaoDroidLink 8.84 (versionCode 230) — internal

## What changed

- **Up to 16 favorite contacts** (was 8; request from Vladimir, S24 Ultra, 19.11). With more than 8 the Contacts widget lays buttons out by its size (at least 150×150): 3×2 and 6×1 show all 16.
- **«More +N».** When not all contacts fit, the last widget button becomes «More +N» and opens a sheet over the screen (same size as the Bluetooth sheet) with every contact as a big button; a tap calls and closes it, «Close» or a tap outside closes it, and it closes by itself after 15 s. Private mode and «names under buttons» apply. No paging: swiping already switches screens.
- Test points `contacts_more` and `sheet_contact_N` for TestHook.

## Verified

- Core tests 65/65, build OK, translations 939/939.
- Not looked at on the car emulator or in a car (the phone was disconnected).
