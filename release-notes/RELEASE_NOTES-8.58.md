# XiaoDroidLink 8.58 (versionCode 204) — internal

## What changed

- **Adaptive video bitrate on network stalls** (`NetworkStalls`, `VideoPipeline.lowerBitrateOnStalls`). Berik (Lynk & Co 08, S24 Ultra, 8.53): music stutters and then «catches up» — audio waited behind the TCP stream up to 1067 ms, 103 times in 15 min, with an excellent signal (−17 dBm, 780 Mbit/s): the car cannot keep up with 13 Mbit/s video. Now 3+ audio waits ≥ 0.3 s per minute step the video bitrate down 9 → 6 → 4 Mbit/s (once per 30 s; each session starts at full). Log: `network stalls N/min — video bitrate A → B`.
- **Haval: reconnect after a call through the car** (`CarSession.SERVICE_WAIT_AFTER_CALL_MS`). Vlad (8.55, 07:13): the car's CarLink BLE service came back ~57 s after the call, we waited 20 s and gave up. After a car call we now wait up to 90 s.
- **Steering wheel voice: «microphone held by another app»** (`CarVoiceInput.MIC_BUSY`, 10 languages). Vlad (Haval + S25 Ultra, Yandex Navigator): recognizer error 7 with a single level reading, 8 times in a row — Alice holds the mic; on 06.11 with StarLine it recognized speech. The message now says so instead of «didn't catch that».
- **Toyota bZ3X: normal cast only** (`CarSession.isBz3x`, work modes 1). With app full-screen cast (4) the car (CarLink v1.6.4) hides itself and waits for a tap on our icon in its app menu, which never appears; no picture in 8.03–8.55. Log: `bZ3X: asking for normal cast only`.
- **Dock and player spacing** (Kasım, Deepal S05, 2560×1280): bottom dock buttons centred vertically (were stuck to the bottom), icons and labels with room inside the selected plate (bottom and left dock), smaller ⏮/⏭ inside the round player buttons of day designs, dock card shadow to the right only.

## Verified

- Core tests 54/54, build OK.
- Dock/player: before/after shots on the phone (XDL test, Classic theme, 2560×1280).
- Not tested in a car.
