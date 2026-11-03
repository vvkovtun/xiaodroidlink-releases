# XiaoDroidLink 7.46 (versionCode 92)

## What changed

- Side bar next to Google Maps. When the map widget shows the phone's map, the phone picture is fitted left of a 168 px bar instead of being covered by car buttons: Address (voice route), Route (planner), Home, Work, Where am I, and End (only while navigating). "Where am I" clicks the map app's own re-center / your-location button through the accessibility service.
- The route planner is no longer hidden under the phone picture: the phone layer is not drawn while the planner is open.
- Voice song search: the MediaSession `playFromSearch` request is checked after 4 s; if the track did not change (YouTube Music ignored it in the car), `MEDIA_PLAY_FROM_SEARCH` opens YouTube Music and the map is brought back once music plays. The microphone is now also on the short music card.
- Left dock is the default and shows Home, Maps, one more app, Music and Apps, with icons up to 100 px. "Dock on the left" replaces "Audio through CarLink" in the car settings panel.
- "Audio through CarLink" is removed from the phone and the car: audio always goes through CarLink (YU7 does not accept Bluetooth audio from this phone).
- Test hook `glshot` saves the real composed frame (with the phone picture).

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped (the check for the removed audio switch was replaced).
- On the emulator: bar buttons drawn beside Google Maps, Address opens "Say the address…", Where am I clicked the Google Maps button after the map was moved.
- Not yet checked in the car.

APK SHA-256: `3f57c179a0fd3c9606d1a5424190b9ee343136614a4c8d2ff805ae7e2d71fabd`

AAB SHA-256: `ecc7c79edd830aa43a3e789bcef2aa4743092872c2eee18318259b95618da21e`
