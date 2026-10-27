# XiaoDroidLink 7.71 (versionCode 117)

## What changed

- Calls by voice (`VoiceCall`): wheel button → "call Olena" / "подзвони мамі" / "打电话给…" → phone contacts (new READ_CONTACTS permission, asked the first time from the phone) with Ukrainian case endings ("Олені" → Олена, "Сашкові" → Сашко); one match calls, several show up to three on the car screen. Without car Bluetooth (HFP) the phone does not call (also for favourite contacts): it opens the car Bluetooth picker and asks to call again.
- Car assistant reply on the car screen in the app language (`CarReplyTranslator`, translate.googleapis.com, only the reply text).
- Car commands from the car's Voice Skills menu (not yet verified in the car): windows halfway (车窗开一半) and a little (车窗开条缝), air to the face (空调吹脸) and "don't blow in my face" (guess 空调不要吹脸), FM radio (guess 收音机: on/off, frequency, next/previous station). French «fenêtres» now matches windows.
- Full Voice Skills menu from Vadym's photos written to `docs/20-car-voice-commands.md`.
- Privacy policy: contacts, microphone, YouTube Music search, Google Translate, ubilling.net.ua fallback.

## Verified

- Emulator: all 468 guide phrases in 14 languages unchanged; new phrases in 7–8 languages; contact search and the choice card; call blocked without Bluetooth with the hint on screen.
- Smoke test: 88 passed, 0 failed, 2 skipped.
- Not verified in the car: calls, reply translation, new commands.

AAB SHA-256: `563160719297e31d157644bf926e20b6d7d21363b2bfbb2c0e3f61b83fb830bf`
