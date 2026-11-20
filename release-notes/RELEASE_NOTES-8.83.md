# XiaoDroidLink 8.83 (versionCode 229) — internal

## What changed

**Crashes and ANRs from Google Play (seen on 8.60 and older, still in the code):**
- Yandex Navigator screen texts were read on the main thread (ANR, Redmi Note 13 Pro+).
- Screen sharing service crashed when HyperOS refused the capture type (POCO M7 Pro); now it stops and the app asks again.
- Audio encoder stop joined threads on the main thread (ANR in `onProjectionChanged`) and could release the recorder while the capture thread still read it (SIGSEGV).

**Nothing waits on the main thread:**
- Audio start/stop after projection changes, the delayed start and the audio setting run on `carlink-stream-work` (`startVideo` holds `streamLock` up to 4–7 s while connecting).
- Accessibility window walks (speaker and end-call buttons, map recenter, Enter, clear field, projection Start, route Start, YouTube player, top search result) run on `carlink-a11y` via `CarAccessibilityService.later()`; `foregroundPackage()` never blocks.
- Phone status polling (every 5 s) on `carlink-status`; log file written in batches on `carlink-log`.
- App and map choosers list installed apps in the background.

**Memory and drawing:** only the current theme's scene stays in memory (was up to ~88 MB); catalog previews released after it closes; two-colour gradients cached (`ShaderCache`), ellipsized labels cached.

**Structure (architecture review):** `CarProfile` (every per-car quirk in one table), `CarAudioPolicy` (never STOP, PAUSE once), `StagePolicy` (connection stage reactions), `DashboardState.Action`/`Playhead` snapshots. Tests 61 → 65.

## Verified

- Core tests 65/65, build OK, translations 938/938.
- Car emulator YU7 on S25 Ultra, 4 runs each vs 8.82 with music (`scripts/perf_compare.py`): no main-thread stalls in either, CPU and frame rate the same, no STOP to the car; frame gaps and music dropouts depend on the laptop Wi‑Fi in both versions.
- Not checked in a real car: calls with speakerphone, map recenter, light theme.
