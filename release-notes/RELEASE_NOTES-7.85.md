# XiaoDroidLink 7.85 (versionCode 131)

## What changed

Usability release after reviewer complaints ("no sound in Spotify", "feels like a 10-year-old navigator", "picture not full screen").

- **Setup wizard** on the phone: one step at a time (connection + microphone, touch from the car, notification access, rotation, battery), progress bar and one big "Allow" button. Rotation permission (WRITE_SETTINGS) is now required: without it the phone stays portrait and the car shows black side bars. The car shows "Picture is not full screen" only while it shows the phone, after the sound warning.
- **Send report**: one tap shares a text file (permissions, phone, Android, connection, VPN, problems, log tail) through mail or Telegram; own `ReportProvider`, read-only.
- **Bigger phone picture**: the phone status bar and navigation bar (found through Accessibility windows) are cropped; the left rail in phone mode is narrower (156 instead of 276 units).
- **Car keyboard**: app language + English, more layouts can be added on the phone ("Keyboards in the car", 14 layouts); keys about 40% taller; `,` `-` `/` and a clear-all key; Ukrainian layout gains `Ґ` and `'`.
- **Large keyboard over other apps**: when the phone keyboard opens in Google Maps, Waze, Spotify etc., the car shows its own keyboard over the phone picture and types into the focused field (ACTION_SET_TEXT, ACTION_IME_ENTER).
- **Music widget**: "Player ▾" opens a picker of installed players (chosen one becomes default and starts), "Choose a song" opens the player full screen; the empty state no longer says "turn on music on the phone". Option "Player name" removed.
- **Map choice**: "Map ▾" at the top of the map bar opens installed maps (Google Maps, Waze, others) plus built-in OpenStreetMap, with a short note under each.
- **Destination**: when a route is started from XiaoDroidLink, the turn hint and trip card show "🏁 place · ETA".
- **Routes start without taps**: Home, Work, recent places and voice are geocoded first (nearest result, under 300 km), so Google Maps gets coordinates instead of text; for 15 s after launch Accessibility presses "Start"/"Go" in Google Maps or Waze; if the small map widget still is not navigating after 8 s, the map opens full screen.
- Only one charger request at a time (they piled up while the server did not answer).
- Build: `probe/build.sh` no longer overwrites `release/` for test builds.
- Smoke test: the touch check in other screen sizes taps the new phone-area centre and expects the centre of the visible (cropped) phone screen; test state reports `phoneBars`.

## Verified

- Emulator: setup wizard, report chooser, keyboards (layouts, typing into Google Maps search), player and map pickers, auto-press of "Start" in Google Maps, full smoke 89/0/2.
- Not verified in the car: picture crop, both keyboards, pickers, destination line, route auto-start. Spotify sound not investigated (S25 not connected).
