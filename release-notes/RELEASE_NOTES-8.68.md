# XiaoDroidLink 8.68 (versionCode 214) — internal

## What changed

Vadym's 8.67 report (15.11, YU7, route to Hatne): satellites jammed most of the way (`gnss: used=0`), a real fix only every 10–30 s, reckoning along the route in between. Off the route (Instytutska → Karmeliuka, 12:21:39 the reckoner left the route) there was no reroute.

- **Reroute from sparse real GPS fixes.** The old check needed 3 ticks in a row with trusted GPS; GPS went "lost" again 2 s after every fix, so it could never fire. Now every new real fix (`state.realFix*`, set by `RoadSafetyServices` when a fix is trusted) is checked against the route; two in a row farther than 80 m + the fix's own accuracy (capped at 100 m) → reroute from the real fix. Normal GPS keeps the old rule (~6 s).
- **Reroutes are logged** (`route: … m off the route, rerouting` / `rerouted` / `reroute failed`).
- **Steady new GPS place is trusted** after a jump: 5+ fresh fixes over 8 s, each reachable from the previous by car speed, accuracy ≤ 30 m, ≤ 30 km away and not leaving Ukraine (EW spoofing stays held). Log `gps jump: new place … steady for N fixes, accepting`.
- **Arrow snaps to the route** when it is within 30 m of the line (like Google), on the built-in map.
- **OpenStreetMap credit** moves above the GPS-lost badge and −100 m / +100 m buttons instead of covering them.

## Verified

- Core tests 60/60 (snap 15 m off the route onto the line). Build OK. Not tested in a car or on screen.
