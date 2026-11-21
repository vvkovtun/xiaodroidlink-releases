# XiaoDroidLink 8.91 (versionCode 237) — internal

## What changed

- **«Back to GPS»** puts the arrow at the current GPS point at once (even if GPS has not updated for a while — the driver chose it) and, if a route is being followed, rebuilds it from there (Vadym, 21.11). Before, the arrow could stay at the manual point and the route was not rebuilt.
- **«I'm here»** rebuilds the route from the chosen point at once. While the position is untrusted (manual or no GPS) the app never reroutes by itself, so before this the old route stayed.
- **Map attribution** moves above the «Position set manually» plate and the crosshair buttons, as it already did for the «GPS lost» plate (Vadym's photo).

## Verified

- Core tests 65/65, build OK.
- On the emulator with a route in Kyiv: «Back to GPS» moved the arrow ~9700 km to the GPS point and rerouted (2.3 km, 6 min) within half a second. «I'm here» triggers the reroute (logged); not checked with a short distance or in a car.
