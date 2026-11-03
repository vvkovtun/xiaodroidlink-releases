# XiaoDroidLink 7.22 (versionCode 68)

## What changed

New widgets (the widget catalog now has 23, six in a row):

- **Lyrics.** Lines of the song that is playing, the current one highlighted.
  The text is looked up on lrclib.net by title and artist; some songs have none.
- **Notifications.** Latest notifications from all apps, not only Viber and
  Telegram. A tap opens the app.
- **Recent places.** Addresses you routed to from the car; a tap starts the
  route again.
- **Quick actions.** Buttons built from what is already set up: Home and Work
  addresses, favourite contacts and the Apps menu. Each group can be switched
  off in the widget settings.
- **Car lights** in the Speed widget (standard look only, not Neon or Retro GT).

CarLink protocol:

- The music message to the car now carries the album, favourite state, album
  cover and, with the Lyrics widget, the current lyrics line.
- Notifications sent to the car carry up to three action buttons (those that
  need no typing); pressing one in the car runs it on the phone.
- The phone state message reports when the voice assistant is listening.

## Privacy

While the Lyrics widget is on a home screen, the title, artist and length of
the playing track are sent to lrclib.net. The privacy policy lists this.

## Verified

- On the emulator: the four widgets and the catalog are drawn; a notification
  row, a recent place and an app quick action respond to a tap; the lyrics
  service answers in the format the app parses.
- Emulator smoke suite on Android 16, quick mode: 49 passed, 0 failed,
  2 skipped. Core tests: 13 passed.

## Not verified

- Everything on the car side: whether YU7 shows the cover, lyrics line and
  notification buttons, and how its own player reacts to the cover.
- Lyrics with real music (the emulator has no player), the contact call
  button in Quick actions.
- Everything listed as not verified in 7.16–7.21.

## Deliberately not done

Phone internet for the car (needs a system call that exists only in Xiaomi's
firmware), a second call window over CarLink, phone apps in the car's own menu,
a phone camera widget. Reasons are in `docs/18-protocol-and-widget-backlog.md`.

APK SHA-256: `7dd3269cc2e24c8689d227688ccce55985ed5e013c450179fa0c8e3bfc2f459f`

AAB SHA-256: `e5393d261041043c78a6cd093268d634e24ded050629ea1e8cd3f624523a6df0`
