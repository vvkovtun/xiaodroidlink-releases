# XiaoDroidLink 7.94 (versionCode 140)

## What changed

Vadym after a drive (30.10): voice route went to the wrong place because it misheard; always show the found address, let me say it again by voice, add a "drive to <address>" command to the assistant, start a route only when I tap the address; the first connection sometimes shows the phone instead of the map; reconnecting takes long; continue the last song.

- Address search asks the phone's geocoder (Google) first, then Nominatim. Nominatim did not know village addresses ("Гатне гоголяй 1А"), and the app then handed the raw text to Google Maps, which started a route without showing where. Results are nearest first, with distance.
- Nothing found — no silent hand-off: "Address not found" and a "Search … in the map" button.
- The address list has a "🎤 Say again" button; tapping the heard text opens the keyboard.
- When a route starts, the full destination is shown for 10 s ("➜ Route to: …").
- Steering-wheel assistant: "Поїхали до …", "Маршрут до …", "Поехали в …", "Drive to …", "Fahr nach …", "Jedź do …", "Va à …", "Llévame a …" open the address list; "home"/"work" too — a voice route never starts without a tap.
- New trip (more than 5 min since the last stream): 2.5 s after car audio starts, the last song continues (play on the paused player, or the media key). Not during a call or the voice assistant.
- For 30 s after connecting, if the map widget shows our app or the launcher instead of the map, the map is brought back.
- Auto-connect pauses after failed attempts: 20 s, 45 s, 2 min, 10 min (were 1, 5, 15, 30 min). The log now says whether the phone was on another Wi-Fi when joining the car.
- Route card title is white in light themes too (it was dark on the dark card).

## Verified

- On Vadym's S25 Ultra with the XDL test build: "поїхали до Гатне гоголяй 1А" → list with "Hatne, Kyiv Oblast"; "маршрут до Гатне вулиця Гоголя 1А" → "Vul. Hoholya, 1A, Hatne, 08160"; nonsense → "Address not found" + map search button; "поїхали додому" does not start a route. Phrase parser checked on 17 phrases (car commands like "навігація без звуку" are not taken as routes).
- Not checked: speech in the car, song resume, map watchdog, Wi-Fi. Smoke test not run (emulator lacks memory).
