# XiaoDroidLink 8.93 (versionCode 239) — internal

## What changed

- **Touches on large car screens.** When the phone's H.264 encoder cannot produce the car screen size, the app sends a smaller frame (Toyota RAV4 0042/0010: 2422×1272 → 1920×1008). That RAV4 sends touches already in the frame's coordinates while labelling them with the screen size (all reports since 01.11: maximum 1919×990). The app rescaled them a second time, so every tap landed up and to the left (keyboard «И» → «П», «Д» → «Г»). Now, in a downscaled frame, touches are taken as frame coordinates; if a touch ever falls outside the frame, the app switches back to screen coordinates for that session (`VideoPipeline.touchesInFrame`). Cars that get a full-size frame are unchanged.

## Verified

- Core tests 65/65, build OK.
- Not checked in the car yet (waiting for the RAV4 owner's report).
