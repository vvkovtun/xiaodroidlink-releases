# XiaoDroidLink 7.19 (versionCode 65)

## What changed

- **Design catalog.** Eight designs: Winter, Bronze, Blue wave, Neon, Ocean,
  Sunset, Classic and Retro GT. Each sets its own background, colours and three
  home screens (map, media, trip). Choose on the car screen: gear → "Design
  catalog", tap a design to see its three screens, then "Use this design". The
  catalog replaces the separate colour-set choice from 7.18.
- **Screens 1/3 button** in the dock shows which home screen is open and
  switches to the next one. Swiping sideways still works.
- **Apps from the car screen.** The Apps menu has an Edit button: it lists every
  app on the phone, a tap adds or removes it, Done returns to the menu. Before
  this the list could only be changed in the phone app.
- **Popular apps on first start.** If the Apps list was never touched, it is
  filled with popular apps that are installed (Spotify, YouTube, Waze, WhatsApp
  and others). Existing lists are not changed.
- **Documentation.** New screenshots of the three screens, the design catalog
  and the phone app.
- The APK is about 12.5 MB instead of 1.9 MB because of the design images.

## Verified

- On the emulator: the design catalog and its detail view in Ukrainian and
  English, the three screens of Retro GT, choosing apps on the car screen
  (select, unselect, Done, open the chosen app), the first-start app list on a
  clean install.

## Not verified

- Anything in the car: how the designs and the catalog look on the real screen,
  and choosing apps by touch.
- The other seven designs were not inspected one by one in this release check.
- Page arrows in the app chooser: the emulator has fewer than 24 apps, so a
  second page never appeared.
- Everything listed as not verified in 7.16–7.18.

Local verification: emulator smoke suite on Android 16 — 89 passed, 0 failed,
2 skipped (ChatGPT listening and music controls need a real phone). It does not
cover the car connection, audio or Bluetooth.

APK SHA-256: `c59ec4db4eb5cb6389f7cefa650d7b2ea70ad117d1cd31d2b2815f029d26fbd9`

AAB SHA-256: `956684cc05389f0baa34a0ab8c0f4c6d8d2d5f92a7c9fbbf0a36e0edd91e739c`
