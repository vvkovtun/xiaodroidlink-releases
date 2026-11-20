# XiaoDroidLink 8.86 (versionCode 232) — internal

## What changed

- **ANR fix: app names off the main thread.** When a notification arrived, the app read the sender app's name (`getApplicationLabel`) on the main thread; on Redmi Note 13 Pro+ with HyperOS this loads the other app's resources and theme and took seconds — two Play ANRs (18–19.11, 8.60 and 8.73). Names are now cached for the whole process; notifications and the car's media player label read them in the background and show a fallback (Telegram, Viber, WhatsApp, Instagram are known; others briefly show the package) until the name is loaded.
- The other four ANRs of the last 28 days (Yandex Navigator text reading, app list in the map chooser, projection start) were already fixed in 8.83, in production since 8.84.

## Verified

- Core tests 65/65, build OK.
- Not checked on a phone with real notifications.
