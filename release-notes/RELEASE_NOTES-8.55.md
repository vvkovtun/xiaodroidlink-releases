# XiaoDroidLink 8.55 (versionCode 201)

## What changed

- **Steering wheel voice button for non-Xiaomi cars** (`Prefs.otherWheelVoice`, `CarLinkService.appVoiceByWheel`, `AppVoiceCommands`). Since 8.23 the 8107/8108 keys on non-Xiaomi cars were left to the car's own assistant (Jetta: two assistants at once, our XiaoAI translator heard an empty microphone). Haval does nothing on that key, so after the car was recognised as non-Xiaomi the button went silent (Vlad, 10.11: «с руля говорила, а сейчас только микрофон на экране»; in 8.44 it still opened the phone assistant). New switch «Кнопка голосу на кермі — XiaoDroidLink» on the phone (Settings) and on the car screen (Settings, where Xiaomi has «Команди помічника»). On by default only for Haval Xiaolong Max (001B/0011, from the saved car name); other cars keep the car's assistant unless switched on. Listens with the phone microphone; understands route («Поїхали до …», «Додому», «На роботу»), calls («Подзвони …»), music (next / previous / pause / play, «Увімкни <song>» via the existing song search) and «Штучний інтелект»; anything else opens the phone assistant. No XiaoAI car commands. Second press cancels listening. 4 new strings, 15 languages.
- Includes 8.54: Haval waits 35 s for the car to take the call.

## Verified

- Core tests 54/54 (new: music command parsing uk/ru/en), translations 886/886, build OK.
- Not tested in a car; the car-screen switch was not looked at on screen.
