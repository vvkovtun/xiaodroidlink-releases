# XiaoDroidLink 7.47 (versionCode 93)

## What changed

- Voice song search, from the 7.46 trip log: recognition was right ("Океан Ельзи Я на небі"), but YouTube Music ignores `playFromSearch` from apps other than Android Auto and Assistant, and `MEDIA_PLAY_FROM_SEARCH` only opens its search results. Now the session request is skipped for YouTube Music, the search intent opens the results and the accessibility service presses the top result's "Play <title>" button (not the mini player). Checked against the real YouTube Music screen on the phone.
- Song search card in the middle of the car screen: listening, the recognised text, "Searching…", then "▶ title — artist" or why nothing started. The phone picture is hidden while it is shown.
- Route search with Google Maps or Waze first lists the addresses found; picking one starts the map app's navigation to its coordinates. If our search finds nothing, the text goes to the map app as before.
- Calls in the clock widget: a text line under the date instead of the pill — green "Calls through the car" or yellow "Connect calls ›" (tap opens the car Bluetooth picker).

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- Song card stages on the emulator (YouTube Music there is not signed in, so playback itself was not checked).
- Not yet checked in the car.

APK SHA-256: `e58c118978c5ecebe32ff1a5697aa70ab8c2deadb418a544f44ec60abee7cabb`

AAB SHA-256: `a6fedd6ac3b3020d9307569039039c79b4179657b157fa882ef4daad2c124b7f`
