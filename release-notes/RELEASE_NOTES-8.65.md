# XiaoDroidLink 8.65 (versionCode 211) — internal

## What changed

- **Built-in map day/night follows the sun, not the panel theme** (Vadym, 8.64 report 14.11 12:11: dark panel made the map dark at noon in Kyiv). `DashboardState.mapNight` = `sunIsDown()` (location; without it — city of the phone's time zone); vector style, background, night filter for raster tiles and the travelled route use it. Test commands `theme`/`appearance` put the map into the panel theme for screenshots.
- **Diagnostics**: log `dashboard theme: dark|light (Авто|Темна|Світла)` on connect and `map theme: day|night` on change; report header line `theme: … · design … · now …`.

## Verified

- Core tests 60/60, build OK. Not tested in a car.
