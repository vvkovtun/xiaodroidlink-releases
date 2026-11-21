# XiaoDroidLink 8.88 (versionCode 234) — internal

## What changed

- **Set the position by hand on the built-in map** (Vadym, 21.11: GPS was lost or wrong while driving, and there was no way to tell the app where he was). After «Where am I» a blue «Not here? Set position» chip shows for 5 s — always, even with GPS, because GPS can lie. It opens a crosshair mode: move the map until the crosshair is where you are, or find the address by voice or keyboard (the map moves there), then «I'm here». Nothing changes until «I'm here», so a stray touch can't move the position.
- **After «I'm here»** the arrow starts at that point and is dead-reckoned from the car's speed and heading (along the route if there is one). A plate «Position set manually» offers «Change» and «Back to GPS». GPS takes over again by itself only after it agrees with our position within 50 m for 10 s, so a GPS that is off by a few hundred metres or spoofed to another city does not overwrite the manual point.
- Google Maps and Waze are not affected (they use the phone's own location).

## Verified

- Core tests 65/65, translations complete, build OK.
- On the emulator: «Where am I» → «Not here?» → crosshair → pan → «I'm here» moved the arrow by 155 m (logged), «Back to GPS» cleared it.
- Not checked: address search for «I'm here», GPS taking over by itself, driving in a car.
