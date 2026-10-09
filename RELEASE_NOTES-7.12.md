# XiaoDroidLink 7.12 (versionCode 58)

The automatic dashboard theme no longer follows the car's day/night signal,
which proved unstable on the YU7. It is now dark when the sun is below the
horizon at the phone's location and light otherwise, re-evaluated every minute.
Without a location the app falls back to the phone's local time (dark from
19:00 to 07:00). The Dark and Light choices are unchanged.

Everything else is the same as 7.11: the settings panel on the car screen, the
auto-connect distance setting, quiet automatic attempts and the screen sharing
prompt after unlocking.

Local verification: the sources compile and the APK and AAB were built. The sun
formula was checked against Kyiv sunrise and sunset for 9 October 2026. The
settings panel was checked on the Android 16 emulator in 7.11. Host tests, the
emulator smoke suite and physical YU7 validation were not run.

APK SHA-256: `cbc881c44f2e41932766e5cf6704c014708ee0e100d4733c8217c1dbe7bd04a9`

AAB SHA-256: `ecbd73442f5ff1ab2553769f38f895616d077f2e716a09b8267f129ceb6e498c`
