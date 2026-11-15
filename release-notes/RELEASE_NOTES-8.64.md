# XiaoDroidLink 8.64 (versionCode 210) — internal

## What changed

- **Auto theme without location follows the time zone** (`SunClock`): sun position for the city of the phone's time zone (table of zones of our users; otherwise longitude from the UTC offset) instead of a fixed 19:00–07:00 (in November Kyiv is dark at 16:00). With location — unchanged, sun at the phone's position.
- **Address search with a village name** (`NavigationService.townWord`, `mentions`): "Інститутська 31 Гатне" led to Instytutska 31 in Kyiv — the geocoder found a house and stopped. If the query names a town or village, results outside it are dropped; then the geocoder retries in that village, then Nominatim ("Інститутська 31, Гатне" — finds the exact house), and as the last resort the village centre. Same point is used for Google Maps / Waze.

## Verified

- Core tests 60/60, build OK.
- Not tested in a car.
