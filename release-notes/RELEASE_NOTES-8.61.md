# XiaoDroidLink 8.61 (versionCode 207) — internal

## What changed

- **Built-in navigation ends on arrival when the address is off the road** (`NavigationEngine.arrived`). Vadym (8.52, 12.11, Hatne): the route ended on the road ~110 m from the geocoded house, the car stopped there and went to P, and «You have arrived 110 m» stayed until the end of the session with the same distance and time. Now arrival is within 30 m of the address **or** of the route end, or the car on P within 300 m of either.
- **GPS jump filter uses the car's own speed** (`NavigationEngine.gpsJumpLimitMeters`). A new GPS point is accepted only if the car could reach it: 1.5× the highest car speed since the last trusted point (at least 54 km/h) + 300 m. Before: 500 km/h + 2 km, so after a 4.5-min GPS gap (12.11, 12:30–12:35) a spoofed point ~40 km away passed. Cars that send no speed keep the old limit.
- **No re-routing while GPS is lost or spoofed** (`state.gpsUntrusted`): navigation follows the old route with the dead-reckoned point. Possible cause of a 40–50 km route instead of 5 km (Vadym, Stepana Bandery; no log of that trip).
- **Navigation takes only the map arrow's point** (trusted GPS or dead reckoning), even if it is up to 30 min old; Android's last raw point (without the spoof filter) only when there is no arrow yet.
- **GPS spoofing detected by the signal itself** (`GnssSpoofDetector`, deliberately high thresholds): GPS speed differs from the car's speed by > 30 km/h and > 60 % for 10 s (only after they agreed 20 times this session), or ≥ 6 satellites with C/N0 spread < 1.5 dB and only GPS left while Galileo/BeiDou/GLONASS were there in the last 10 min, for 5 s. Then the same as a GPS loss (dead reckoning, trusted place for alerts/cameras). Trust returns after 20 s with no sign. Log: `gnss:` every 30 s while driving, `gps spoof suspected` / `gps spoof over` — to tune thresholds from Kyiv trips.
- Docs: what cars really send (logs of 277 reports): YU7 sends speed in `GearInfo` field 2 (km/h, ~1/s); no car sent `GyroScope` or `Acceleration`.

## Verified

- Core tests 56/56, build OK.
- Not tested in a car.
