# XiaoDroidLink 7.86 (versionCode 132)

## What changed

- **Map picker shows only maps.** Before, every app that opens a `geo:` address was listed, so Bolt, Uber and Flightradar appeared. Now: known navigators (Google Maps, Waze, Yandex, 2GIS, Organic Maps, OsmAnd, HERE, Sygic, Petal, Magic Earth, TomTom, …) plus apps that both open `geo:` and declare the Maps category.
- **Player picker shows only players.** Before, every app with a `MediaBrowserService` was listed, so Bixby and WeChat appeared. Now: known players (Spotify, YouTube Music, Samsung Music, Mi Music, Deezer, Apple Music, Yandex Music, VK, SoundCloud, Tidal, Poweramp, Musicolet, VLC, podcasts and audiobooks, …) plus apps in the Audio category or the default music app.
- **"Other…" tile** at the end of both pickers opens the list of all phone apps; the chosen app becomes the map (panel, "Maps" button, Home/Work routes) or the player (starts at once). It then appears in the picker with a check mark.

## Verified

- Emulator: both pickers, "Other…" for map (Chrome) and player, return to the dashboard; full smoke 89/0/2.
- Not verified on the phone: that Bolt, Uber, Flightradar, Bixby, WeChat are gone from Vadym's lists.
