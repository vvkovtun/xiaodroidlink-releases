# XiaoDroidLink 7.13 (versionCode 59)

The settings panel on the car screen has a language row (English, Ukrainian,
Chinese, French, Spanish); the change applies at once.

Sound after unlocking the phone: in 7.11 and 7.12 screen sharing was restored
immediately after unlock, so the "start audio" message reached the car before
the "phone unlocked" message, and the car stayed silent although the phone was
capturing and sending music. The app now reports the unlock first and restarts
screen sharing and audio 1.5 s later. This ordering is a hypothesis based on
the phone log and has not been confirmed on the car.

Local verification: the sources compile and the APK and AAB were built. The
language row was checked on the Android 16 emulator (Ukrainian and French).
Host tests, the emulator smoke suite and physical YU7 validation were not run.

APK SHA-256: `f628094eb4f88856ab0f4e51053a0ebd77b3ba5dcc87623f59af523c53770feb`

AAB SHA-256: `92d4f4aacc55ce411bacdca5b73109858bae359f6667fab1f31a7a601148cd93`
