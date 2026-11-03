# XiaoDroidLink 7.75 (versionCode 121)

## What changed

- Regeneration (能量回收) is no longer sent to the car by voice: on 27 October it changed the car's braking while driving. Any phrase about regeneration now matches nothing (the screen says it did not understand). Removed from the commands list, the "still testing" line (14 languages) and the guide (5 languages); `docs/20` marks it as never by voice.

## Verified

- Emulator: regeneration phrases in several languages match nothing; 520 guide phrases in 14 languages unchanged; translations 728/728.
- Smoke test: 88 passed, 0 failed, 2 skipped.

AAB SHA-256: `83d597565ca4aac72f7cdb8d77e44218e9bf1cb1a92960046fad7677c5b9f244`
