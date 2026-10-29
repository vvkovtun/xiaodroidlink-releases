# XiaoDroidLink 7.87 (versionCode 133)

## What changed

Fixes from the 7.86 drive (2026-10-29) and a user-flow review (`docs/USER_FLOW_TEST_PLAN.ua.md`).

- **Spotify and SoundCloud removed from players.** Measured on the S25 with a test stream: Spotify (plays through AAudio) and SoundCloud (no `allowAudioPlaybackCapture`) give silence (−120 dBFS) to playback capture, and the YU7 refuses A2DP. VLC (−17 dB), Samsung Music (−15), Deezer (−11…−17) and YouTube Music work. `AppLauncher.NO_CAR_SOUND`: not listed, not auto-added to the car Apps menu; picking one via "Other…" shows "%s does not allow its sound to be sent to the car". Troubleshooting docs explain it.
- **"Choose a song" opens a "Songs" panel** in the car instead of the player full screen: up to 6 next items of the player's queue (`MediaController.getQueue`, as Android Auto shows), with covers when the player provides them; one tap plays (`skipToQueueItem`). "🔍 Find in player" opens the player full screen as before. In the drive log ⏭/⏮ worked; Spotify was opened by "Choose a song".
- **YouTube full screen.** The drive log showed 25 rotate presses in 1.5 min and the auto fullscreen button never clicked (YouTube hides it until the video is tapped). Now when YouTube's `watch_player` covers the phone screen in landscape, the car shows only the 16:9 video over the whole car screen without the rail; taps on black margins do nothing; Back or YouTube's own button leaves.
- **Voice (address and song):** no early stop on the first pause before any words; one automatic retry when nothing was heard, with the phone microphone if the car microphone gave almost nothing (fewer than 5 level samples); the log shows how many frames the car sent.
- **Setup wizard:** accessibility settings open with XiaoDroidLink highlighted on AOSP-style settings (`:settings:fragment_args_key`); a per-brand path hint (Samsung, Xiaomi/Redmi/POCO, Huawei/Honor, generic) under the button and as a toast over Settings; the app returns by itself once the permission is on (accessibility, notifications, rotation, battery); "Skip — I'll do it later" on every step with a reminder card.

## Verified

- Emulator: Songs panel (sample queue), YouTube full-screen frame, setup wizard (highlight, toast, auto-return, skip), full smoke 89/0/2.
- Phone (S25, test stream): player sound measurements above.
- Not verified in the car: Songs panel with a real queue, YouTube full screen, voice retry.
