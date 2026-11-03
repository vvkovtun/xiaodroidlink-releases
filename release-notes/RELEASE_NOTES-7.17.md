# XiaoDroidLink 7.17 (versionCode 63)

Fixes found while using 7.16. No new widgets.

## What changed

- **Air alert widget stayed green.** Two causes. The oblast identifiers did not
  match what tryvoha.online returns (21 of 25 differed), and Android's geocoder
  still reports pre-2020 districts ("Kyievo-Sviatoshynskyi"), which never match
  the service's current ones ("Bucha", "Fastiv"). The district now comes from
  OpenStreetMap (Nominatim), is cached within 3 km, and Kyiv is treated as its
  own region. Each change is written to the log as `air alert: ...`.
- **Home/Work started the built-in navigation instead of Google Maps.** Google
  Maps was used only when "map from the phone" was on. Now the chosen map app
  (Google Maps or Waze) is always used and shown on the car screen. The same
  applies to routes from the Chargers widget.
- **Chargers widget.** Searches 4 km first and 20 km only when little is found,
  on its own thread; falls back to a mirror server; says so when the map server
  does not answer instead of "none found". A second line shows network, number
  of points, 24/7 and fee when OpenStreetMap has them. Power and tariffs are
  rarely present in the data for Ukraine.
- **Drive layout:** air alert instead of the car charge widget, because the YU7
  does not report charge over CarLink. Screens already saved on a phone are not
  changed.
- Test copy (`scripts/build_dev_apk.sh`) now carries a build stamp in its version.

## Verified

- On the developer's phone (test copy, real location): the district resolved to
  "Fastivskyi district, Kyiv oblast"; chargers loaded (15 found) after two
  server errors; a route to a test address opened Google Maps.
- On the emulator with live alert data: Vyshhorod showed "Caution", Kharkiv
  "Alert!", Kyiv "All clear", matching the service at that moment.

## Not verified

- The widget during a real alert in the user's own district.
- That Google Maps actually started guidance (the phone screen was off), and the
  route buttons in the car.
- Everything listed as not verified in 7.16 that was not retested here.

Local verification: emulator smoke suite on Android 16 — 89 passed, 0 failed,
2 skipped (ChatGPT listening and music controls need a real phone). It covers the
Road layout and the pre-existing controls, not the fixes above, the car
connection, audio or Bluetooth.

APK SHA-256: `802e2778fe9f95126afa28eb6f90096c7a999ad2f457b0525eed0d8a01936ee7`

AAB SHA-256: `6bebd745511f9826227a702ba0499e5c6c852a865376767873ef736bb5589ac5`
