# XiaoDroidLink 7.66 (versionCode 112)

## What changed

- Weaker H.264 encoders (many MediaTek and Unisoc phones): the frame is fitted to what the encoder accepts — same aspect as the car screen, aligned to the encoder (MediaTek: multiples of 16, up to 2560 wide). Before, "Preview without car" halved 2764×1426 down to 172×88 and the encoder refused (Infinix Hot 40, Android 13, mt6789). The car now gets the largest frame the phone can encode instead of none; touches scale from the car's own size (UIBC source=2764x1426). Phones whose encoder takes the full frame (Galaxy S25 and other flagships) are unchanged.
- Android 13: opening apps from the car screen called an Android 14 method and would crash; now only on 14+.
- The smoke test stream uses the full car frame, so weaker encoders go through the same path as in the car.

## Verified

- Infinix Hot 40 (Android 13, MediaTek): "Preview without car" opens, 2560×1312 on c2.mtk.avc.encoder.
- Android 13 emulator: preview works.
- Quick emulator smoke test (Android 16): 48 passed, 0 failed, 2 skipped; the emulator encoder sent 2016×1040 for 2764×1426 and touches worked.
- Not verified in the car: whether YU7 shows a smaller frame full screen.

AAB SHA-256: `b489bb54e29247ca9dbaba4d6843c26ea5d4aa55ad54f61504ce05b43b722eb4`
