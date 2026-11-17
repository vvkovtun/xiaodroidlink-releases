# XiaoDroidLink 8.71 (versionCode 217) — internal

## What changed

- **"Could not connect" screen with the likely cause** instead of one red line. Most support letters (reports 31.10–16.11, 42 people) were about the same few connection failures; the session now records what it saw (`ConnectionAdvice`) and the phone shows one cause with one button. The failed step chip turns red; chips moved right under the title.
  - Causes: VPN, car CarLink not ready (no ICCOA service), code not delivered, Android Wi‑Fi window not confirmed, phone held by another Wi‑Fi (shows its name), Belarus (channel 149), car network not seen, 40 % (on car Wi‑Fi but blocked), car did not start casting.
  - Same cause twice in a row: "Failed again" + other possible causes for that step.
  - Belarus and "CarLink not ready": short text on screen; the blue **Step by step** button opens a dark sheet with numbered steps (Belarus: open airplane mode, then Connect again).
- **VPN blocks connecting** instead of a warning: "Open VPN" / "Connect anyway".
- bZ3X: connected but the car never showed us within 15 s — hint to tap the XiaoDroidLink icon in the car's CarLink menu.
- Journal line `ADVICE <cause>`; `scripts/mail_digest.py` prints it, replies per cause in `docs/SUPPORT_TEMPLATES.md`.
- All new texts in 15 languages.

## Verified

- Core tests 61/61 (new: one cause per failed stage), build OK.
- Emulator smoke test 76 passed / 13 failed / 2 skipped: all 13 are “touch from the car lands in the same place” (touch lands ~300 px right of centre on every screen size). Full smoke was last run on 7.85–7.92; the touch-mapping code is not touched in this release — the test's fixed tap point is likely stale. Not investigated.
- Screens checked on the emulator via TestHook `advice` (not a real failure in a car). bZ3X hint not checked.
