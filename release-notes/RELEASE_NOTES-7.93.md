# XiaoDroidLink 7.93 (versionCode 139)

## What changed

Vadym: in the small map widget the navigator arrow sits "anywhere", keep me centered like in a navigator, for other maps too; no cropping jumps, smooth.

- The phone map in the map widget (with "fill" on, the default) is a crop of the phone screen. It used to be the middle, but navigators put their arrow low (Google Maps portrait 50%×77%, landscape 69%×82%; Waze portrait 49%×78%, landscape 74%×74% on the S25), so the arrow ended up at the widget edge or outside it.
- Now, every 0.4 s the compositor renders the visible part of the phone frame into a 240 px texture and reads it back; the arrow is found as the largest compact blob of its colour: Google Maps #0D53FE (day) / #4080F8 (night), Waze #00B0C0. The route line is more violet or cyan and elongated, the Gemini button is small, Waze street names are lighter.
- The crop window follows the arrow like a camera behind the car: the arrow at the horizontal centre and 62% of the height. A calm zone (12%) keeps it still; outside it the window glides there in about 0.5 s; no zoom change. Without an arrow (no navigation) — the middle, as before.

## Verified

- On Vadym's S25 Ultra with the XDL test build: Google Maps day portrait and landscape, Google Maps night, Waze day — the arrow is centred in the widget. Not checked: Waze night, motion during a real drive, the car. Smoke test not run (emulator does not have enough memory on this PC; the phone has the Play build with another signature).
