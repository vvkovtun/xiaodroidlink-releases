# XiaoDroidLink 7.90 (versionCode 136)

## What changed

Vadym on 7.89: "Expand" did not make the YouTube video full screen, "✕ Exit" stayed on top all the time, and the car keyboard was not needed in ChatGPT.

- "⛶ Expand": YouTube ignores ACTION_CLICK on its full-screen button, so the button is now tapped with a real gesture. If the button is not found after 3 tries, the app swipes up on the player (YouTube's own gesture). Until YouTube goes full screen itself, the car already shows only the player area of the watch page (16:9 crop).
- "✕ Exit" hides after 10 s without touches; any touch on the car screen shows it again for 10 s. A hidden button does not catch taps: they go to YouTube.
- ChatGPT: the big car keyboard is not shown (voice is used there). Other apps keep it.

## Known

- The YouTube home page stays portrait on phones (YouTube locks it); landscape starts on the video page. Checked on the emulator only.

## Verified

- Emulator (S25 size): Expand → video full screen on the phone and in the car; Exit hides after 10 s. Swipe fallback and player crop not exercised (the tap worked). Quick smoke 49/0/2; full smoke not run.
