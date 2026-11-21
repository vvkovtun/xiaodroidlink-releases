# XiaoDroidLink 8.92 (versionCode 238) — internal

## What changed

- **Anonymous usage statistics** to Google Analytics 4 (Measurement Protocol over HTTPS, no Google SDK; `Stats.java`). Events: `app_daily` (once a day: version, phone, language, SIM country, car, design, theme, map app, widget types, enabled features), `connect_attempt` (car codes, furthest stage, failure reason shown to the user, PIN or not, seconds), `first_success` (once per car), `trip_end` (minutes, drops, audio and screen casting, player package, use of routes, voice, quick actions, manual position, car calls), `drive_day` (≥5 min in the car that day). A random app-instance number; never location, addresses, contacts, notifications, Wi‑Fi names, MAC, phone numbers or e‑mail. Events queue on the phone and go over the internet network, not the car Wi‑Fi.
- **Switch** «Anonymous statistics» in the Diagnostics card at the bottom of the app page (on by default; turning it off deletes unsent events). Test builds send only to the Google validation endpoint.
- **Privacy policy**: new section «Anonymous usage statistics».

## Verified

- Core tests 65/65, build OK.
- On the emulator `app_daily` reached the Google validation endpoint with no messages. Connection and trip events are not checked with a real car yet.
