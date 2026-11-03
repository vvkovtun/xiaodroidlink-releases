# XiaoDroidLink 8.27 (versionCode 173)

Includes 8.23–8.26 (internal only so far). Released to internal and closed testing (alpha).

## What changed since 8.26

- Settings → Permissions: button "Extra features via a computer" opens the helper guide in the public releases repo (`docs/EXTRAS_ADB.ua.md` / `.ru.md`, otherwise English). One new string, 826/826 in all languages.

## Since 8.22 (production)

- Jetta voice search via the phone microphone; steering wheel voice keys left to the car assistant on non-Xiaomi cars; accessibility reconnect hint; Xiaomi autostart step; Bluetooth HFP/A2DP diagnostics (8.23).
- With adb grants: PROJECT_MEDIA keeps the stream when the phone is locked (verified in YU7); WRITE_SECURE_SETTINGS gives Extra dim while the phone rests (verified on S25 Ultra after the 8.26 fix) and reconnects an enabled-but-disconnected accessibility service (8.24–8.26). Helper scripts for Windows/Mac/Linux in `helper/XiaoDroidLink-Helper.zip`.

## Verified

- Core tests 47/47, translations 826/826.
