# XiaoDroidLink 7.55 (versionCode 101)

## What changed

- New "⚡ Request" button for the Quick actions widget: one tap on the car screen sends a web request, for example to open gates or a garage, or to run a smart-home scene (IFTTT Webhooks, Home Assistant and similar). Add it on the phone in Settings → "Requests for Quick actions": a name, an `https://` address and POST or GET. The car shows "sending…", then "done" or the reason it failed (HTTP code or no connection). The request goes over the phone's mobile internet, not the car Wi‑Fi. The address stays on the phone and is never written to the log, because it often contains a secret key. Only `https://` addresses work: Android blocks plain `http://`. IFTTT Webhooks need IFTTT Pro.
- Docs: the cover and the song title do reach the car screen over CarLink (the "Bluetooth music only" note was wrong and is removed). Ukrainian pages show the Ukrainian video, all other languages the English one.

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- The Request button on the emulator: a POST that returned 200 showed "done", a GET that returned 401 showed "failed (HTTP 401)"; the log showed only the button names.
- Not checked in the car.

APK SHA-256: `5395c4409e622dd3705f448c9eaa793906804831fba12b93897fd6ba5cc1557c`

AAB SHA-256: `6da317058f6864f83520166197b2b4a07a8c4253133f2264a88a301d3c2454a8`
