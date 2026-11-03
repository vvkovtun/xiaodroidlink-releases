# XiaoDroidLink 7.49 (versionCode 95)

## What changed

- Voice song search with YouTube Music: XiaoDroidLink queries YouTube Music search itself (the unofficial youtubei endpoint the music.youtube.com site uses) and gets title, artist and videoId, because the app's own result page does not expose titles to accessibility services. If every word of the top song's title and artist is in the spoken text (one-letter recognition slips allowed), it plays `music.youtube.com/watch?v=<id>` in YouTube Music; otherwise the car card asks "Which one?" with the top three songs. If this search fails, the 7.47 path (search intent + pressing Play) remains.
- The phone map is back to the pre-7.48 default: landscape, cropped to fill the widget. A Rotate button in the map bar switches to portrait and back; the choice is remembered. The automatic choice by widget shape and the 25 % crop limit from 7.48 are removed.

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- On the emulator: "Океан Ельзи" gave three choices, "Океан Ельзи Я на небі" matched "На небі — Океан Ельзи" exactly; Rotate turned the phone. Playback itself was not checked (YouTube Music is not signed in there).
- Not yet checked in the car.

APK SHA-256: `fe386dcf3fdea76b51207848407254e9121bf4408e989c0b2963d6c43e3487cd`

AAB SHA-256: `a020b410e01a75d5320aef3e6283226c404be1b2f2136e12b2389bd47edd8283`
