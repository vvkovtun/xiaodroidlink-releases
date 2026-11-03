# XiaoDroidLink 7.74 (versionCode 120)

## What changed (after the 27 October trips on 7.73: `capture/probe-2026-10-27-0914.log`, `capture/probe-2026-10-27-0924.log`)

- Every car assistant reply goes through translation, also battery/range answers without numbers (the range answer «目前暂不支持该功能» was shown in Chinese). Translation is retried once; without internet the screen says so.
- Car words the phone mishears are fixed before translating (`CarReplyTranslator.MISHEARD`: 前臂→前备箱, 选假→悬架, 后备灯→后备箱, 护士进→后视镜, 景光灯→近光灯…), and the reply recognizer gets car words as biasing strings.
- Wheel button: if the phone heard no words (09:22 — four times in a row, microphone not silenced by Android), it listens once more by itself with "Didn't hear you — say it again, louder"; the log now has the loudest level heard.
- Commands list (car and phone, 14 languages) and guide (5 languages): windows halfway / a little, volume, snow mode (verified in the car). Battery and range moved to "not by voice". Volume words for the new languages; Uzbek «ovoz» no longer read as the assistant voice volume.

## Verified

- Emulator: 520 guide phrases in 14 languages; the logged replies now translate correctly; the retry fires after "no match".
- Smoke test: 88 passed, 0 failed, 2 skipped.

AAB SHA-256: `36e05eabf24078769feef43a69c8c940361c7da4214db206b81e4d28cb84d66f`
