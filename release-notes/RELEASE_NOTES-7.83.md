# XiaoDroidLink 7.83 (versionCode 129)

## What changed

- Video bitrate ~0.17 bit/pixel/frame instead of ~0.08: 19.7 Mbps for the YU7 screen (2764×1426@30), was 9.85 Mbps (formula unchanged since 2 October). Capped at 20 Mbps and at the encoder's own bitrate limit (weak phones). The map was blurry while scrolling and sharpened after it stopped.
- Key frame every 5 s instead of every 1 s (RTP over TCP does not lose frames; the app still requests key frames on reconnect and theme change).
- Encoder setup falls back step by step: low-latency + new bitrate → new bitrate → the pre-7.83 settings (9.85 Mbps, key frame every second).
- Theme-change bitrate boost: 1.5× the base, at most 24 Mbps and the encoder limit.

## Verified

- S25 Ultra (dev build, test stream without the car): c2.qti.avc.encoder started at 19.7 Mbps with low latency on the first attempt.
- Not run: smoke test, weak phones, car test.

AAB SHA-256: `518c489cce07b92b8ff92faa8efd70f057c9fd62c043c3c3a2564d9bfc5b20f8`
