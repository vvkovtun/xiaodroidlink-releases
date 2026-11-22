# XiaoDroidLink 8.98 (versionCode 244) — internal

## What changed

- **Google Maps or Waze over a built-in route.** Choosing a phone map in the car while the built-in route was running left the widget on OpenStreetMap (Vadym, YU7, 22.11: "whatever I choose, Google or Waze, the widget stays OpenStreetMap"). Now everything switches to the chosen map — the widget, the instrument panel guidance (from the map's notification) and voice. The built-in route is not dropped: it keeps following silently on OpenStreetMap (rerouting included, no voice) and takes the screen, panel and voice back when OpenStreetMap is chosen again. A new route started from the built-in planner shows OpenStreetMap as before. "Stop navigation" stops the route of the map on screen; stopping a Google/Waze route also stops the waiting built-in one. `DashboardState.phoneMapOverRoute` / `nativeRouteShown()`.

## Verified

- Core tests 65/65, build OK.
- Not checked in a car.
