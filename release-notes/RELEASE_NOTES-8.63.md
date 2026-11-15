# XiaoDroidLink 8.63 (versionCode 209) — internal

## What changed

- **Built-in map: vector tiles from OpenFreeMap** (free, no key, OSM data, OpenMapTiles schema, up to z14; z15–18 drawn from a magnified z14 tile). Drawn in-app (`MvtTile`, `MapPainter`, `AndroidMapSurface`) in a Google-like style: white streets with casing, yellow highways, green parks, blue water, buildings, house numbers from z17; separate night palette. Names in the app language (`name:<lang>`). Old OSM PNG cache stays as offline fallback; a custom `map_tile_url` keeps the raster mode.
- **Navigator view**: labels drawn over the map (always upright, not cut at tile edges); tilted heading-up driving view; real turn arrows in the maneuver card (straight, slight, turn, sharp, U-turn, roundabout, arrive) plus a small "then" arrow when the next maneuver is closer than 400 m; trip card shows minutes left in green, distance and arrival time; travelled part of the route grey, white turn arrow on the route line, red destination pin; Google-blue route line.
- Test hook `heading` (`--es value <deg> --es at <lat,lon>`).

## Verified

- Core tests 58/58, build OK; emulator frames day/night, heading 72° and 250°.
- Not tested in a car (drawing speed while driving).
