# XiaoDroidLink 7.27 (versionCode 73)

## What changed

- **Light designs.** Every one of the eight designs has a daytime version
  (own background and catalog previews). Car settings → Auto / Dark / Light;
  Auto follows sunrise and sunset, or 07:00–19:00 without location.
- **Edit button and a fourth screen.** "Edit" next to "Screens" opens the
  widget editor (while parked). A blank fourth screen is there for your own
  widgets and is kept when the design changes.
- **Settings on the car screen.** The player for the Music button and the
  apps in the bottom dock can be chosen in the car settings.
- **Share and Rate** buttons at the bottom of the phone app, and a short hint
  about editing under "Preview without car".
- **No extra pause on track change.** 7.26 told the car "pause" while the
  player switched tracks, hoping the YU7 would show the track title on its
  panel. It did not. The early logs show the title on the panel came from the
  phone's Bluetooth audio (AVRCP), which the YU7 refuses while CarLink is
  running. The pause is removed; the title is still re-sent once the track
  starts playing (7.25).

## Verified

- Core tests: 14 passed. The light designs, Edit button, fourth screen and
  car settings were checked on the emulator while they were made. The pause
  removal runs only with a car connected.

## Not verified

- In the car: the light designs, the Edit button and the fourth screen.
- Everything listed as not verified in 7.16–7.26.

APK SHA-256: `e3c3abdb208838c68959cfe5e10b8b03e79da04cc40c57bd15fe2d899128772e`

AAB SHA-256: `f332637a2dba303231909b88bf965bc1ebbc175fa03647cf331218eb8ce6edbd`
