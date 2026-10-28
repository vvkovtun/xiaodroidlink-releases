# XiaoDroidLink 7.82 (versionCode 128)

## What changed

- Video delay: the GL compositor draws a fresh phone frame as soon as it arrives (no more than once per 3/4 of a car frame) instead of waiting for the next 30 fps timer tick (was 0–33 ms extra, ~16 ms on average).
- H.264 encoder: Qualcomm low-latency mode (`vendor.qti-ext-enc-low-latency.enable`) and no B-frames; if the encoder rejects the configuration it starts without them.
- Live gestures: a second finger that touches after a one-finger live drag started is added to the live gesture (new stroke starts 1 ms into the continuation, as Android's MotionEventInjector requires); a lifted finger ends only its own stroke. No more 50 ms wait before a one-finger live drag. 7.81 trip log: 2 of 134 zooms fell back because the second finger came 54–87 ms late.
- Test hook: `pinch --ei lag <ms>` (second finger later).

## Verified

- S25 Ultra (dev build, test stream without the car): c2.qti.avc.encoder accepted the low-latency configuration, 30 fps.
- Not run: full smoke test, emulator gesture check (emulator MainActivity ANR during stream start), car test.

AAB SHA-256: `f1efca3ae177ed61c364d59f1cb38655f669c1a3dbe2eaeda1d42dfc6920038c`
