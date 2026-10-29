# XiaoDroidLink 7.88 (versionCode 134)

## What changed

- **Setup step 1 opened the app settings page instead of Android permission pop-ups** on a fresh install from Play (reported 2026-10-29 right after installing 7.87). The "already asked" flags (`requested_<permission>`) live in SharedPreferences, which Android restores from the Google backup on reinstall, so the app thought it had asked and went straight to the app details page. Now the flag is `asked_<permission>` = the package's `firstInstallTime`, valid only for the current install.
- Permissions that can still be asked are asked in Android pop-ups first; the app details page opens only when the rest are blocked by the user, with a toast naming what to turn on ("Permissions → Nearby devices, Microphone → Allow").

- Also "Skip — I'll do it later" flags are tied to the install time (`setup_skipped_<step>` = `firstInstallTime`), so a reinstall shows every step again.

## Verified

- Emulator: revoked permissions, step 1 → Android pop-up ("Allow XiaoDroidLink to record audio?").
- Full smoke before the skip-flag change: 84/5/2. The 5 failures are the first screen-size profiles of "touch from the car lands on the same spot" (touch never reached the phone, -1,-1; two could not read state). The emulator had accessibility toggled by hand just before; touch code is unchanged since 7.87 (89/0/2). Not re-run, by Vadym's decision.
