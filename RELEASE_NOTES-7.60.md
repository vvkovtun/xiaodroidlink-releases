# XiaoDroidLink 7.60 (versionCode 106)

## What changed

- Car voice (`CarVoiceCommands`): the YU7 assistant (XiaoAI) understands only Chinese, so the phone speaks car commands to it in Chinese through the phone's own speaker (ALARM stream: not captured into the CarLink audio, not muted during a session). Sound from the car's speakers would be cancelled by the car's echo cancellation.
- New phone switch "Car assistant in your language" (off by default): the steering wheel assistant button (custom_key_event 8108) wakes the car assistant, the phone listens to the driver in the app language and repeats the command in Chinese within ~3 s. "Artificial intelligence", "AI", "ChatGPT" or "Gemini" sends "退出小爱" to the car assistant and opens the phone AI instead. Switch off: the wheel button opens the phone AI as before.
- Quick actions: new "🗣 Car voice…" cell with 43 commands from the car's own Voice Skills menu (climate, seats, windows, front and rear trunk, charge port, mirrors, suspension, wipers, lights, ambient light, drive modes, regeneration, volume, brightness) on two pages. A button beeps, the driver presses the wheel button, the command follows 2.5 s later.
- Close windows uses "把车窗关上" (the car did not act on "关闭车窗").

## Verified

- In the car (test build, 2026-10-25): front trunk opened, wipers and windows worked through the wheel button; the car replied "前备箱开了，注意安全" and "关闭了". The car does not accept "小爱同学" from the phone (only a short flash), with or without wake-free modes — hence the wheel button. The front trunk cannot be closed by voice.
- Not verified in the car: the "artificial intelligence" phrase and the phone switch in the release build.
- Emulator smoke test: 88 passed, 0 failed, 2 skipped.

APK SHA-256: `c0a7e6de411602e1e5ef3db667ef4cde802230c9c804b687150d4583a7a4de93`

AAB SHA-256: `7d14a91e1acfaa2444aded01798808ee6866609792a17eeb37afd4a1a06c46cf`
