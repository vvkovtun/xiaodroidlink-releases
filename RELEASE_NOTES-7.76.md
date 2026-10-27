# XiaoDroidLink 7.76 (versionCode 122)

## What changed

- Calls by voice (verified in the car on 27 October on 7.73: the call went through the car's Bluetooth) are now in the car assistant commands list on the car and the phone (14 languages) and in the guide table (5 languages). The guide says to allow access to contacts and phone calls.
- `VoiceCall` recognizes call requests in Kazakh, Azerbaijani, Uzbek, Tajik and Kyrgyz (verb after the name: «Оленаға қоңырау шал», «ба Олена занг зан») and in Georgian and Armenian (დაურეკე, զանգիր). Before, these languages did not call at all.

## Verified

- Emulator: every guide phrase in 14 languages (546) matches as before; call phrases in all 14 languages are recognized as calls.
- Smoke test: 88 passed, 0 failed, 2 skipped (first run had one flaky touch check on the simulated Redmi 13C screen; the rerun passed).

AAB SHA-256: `a49a99de162d007507ef0411a10cc010c59db7cef0e71b2afdb7d9a59bf575c4`
