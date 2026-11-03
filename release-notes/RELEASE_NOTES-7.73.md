# XiaoDroidLink 7.73 (versionCode 119)

## What changed (after the 27 October trip on 7.72, `capture/probe-2026-10-27-0833.log`)

- Calls by voice: CALL_PHONE is requested together with READ_CONTACTS. On the trip the contact was found, but twice car Bluetooth (HFP) was not connected and then, without CALL_PHONE, only the phone dialer opened.
- Car reply: the recognizer starts 0.7 s before our own phrase ends (it missed the start of replies, "…功能喔", and about half were "not recognized"); our own phrase does not leak into the phone microphone (checked on the S25), anything that does is dropped. The Chinese reply shows at once, the translation replaces it when it arrives. Recording the reply ourselves was tried: a background app gets silence from AudioRecord without a microphone foreground service, so it was dropped.
- "Air to the face" removed: the car needs a Xiaomi account login.
- Results table updated with the trip.

## Verified

- Smoke test: 88 passed, 0 failed, 2 skipped. All 468 guide phrases unchanged.
- Not verified in the car: the new reply listening and calls with the call permission.

AAB SHA-256: `c9092c7fae0a9330b64b2c3bde550e8f0f62027e6a3da59bc0968a723179a765`
