# XiaoDroidLink 7.23 (versionCode 69)

## What changed

- **Music switching is fast again.** 7.22 started sending the album cover and
  the current lyrics line to the car with every music update. In the car (YU7)
  the cover was not shown and switching music became slow. The music message is
  back to what it was before 7.22: artist, title, length, position, playing.
- **Shorter sound hold.** For apps without a player on the dashboard (YouTube
  and others, fix from 7.20) "pause" is now reported after 1 second of silence
  instead of 4.
- **Quick actions are set up in the widget.** Select the widget → Configure:
  the top row holds your buttons (up to eight, a tap removes one); below are
  one-tap additions (Home, Work, favourite contacts, recent places), "App…"
  (any phone app, with search) and "New address…" (typed on the car keyboard).
  Until you change anything the widget fills itself as in 7.22.
- **Lyrics widget:** larger text. Lyrics stay in the widget only.

## Verified

- On the emulator: the Quick actions settings panel (remove, add, pick an app,
  add a typed address) and the widget with the chosen buttons.
- Core tests: 13 passed. The emulator smoke suite was not run for this release.

## Not verified

- In the car: that music switching is fast again, and how the 1-second hold
  behaves with speech that has pauses (sound may cut in and out).
- The larger lyrics text with real music.
- Everything listed as not verified in 7.16–7.22.

APK SHA-256: `fa2c547a812768a6c4780f631126eb22839da207d4bb8fb63d0c69eb454fe225`

AAB SHA-256: `b9b7f1766c94bc8260f45e954e970e16f8af9bdd3a0f939d51faaae412f409ab`
