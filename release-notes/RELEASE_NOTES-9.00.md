# XiaoDroidLink 9.00 (versionCode 246) — internal

## What changed

- **Haval/GWM, every model (vendor 001B).** Haval Big Dog 2 (001C) drops CarLink when the phone's Bluetooth call profile connects, like Xiaolong Max. Calls now stay on the phone speaker for every Haval/GWM model; our action on the steering-wheel voice button stays only on Xiaolong Max (Big Dog 2 opens its own assistant there).
- **Settings scroll (Haval Big Dog 2 report, video 25.11).** After a touch on the selectable "Car data" text, the page kept pulling back to it and the end of the car-apps list could not be reached. Car data and log text are no longer selectable; a long press on car data copies it.
- **Music after a call on Huawei (Camry 80, 25.11).** The notification listener was unbound for the whole trip although access was granted, so no player was seen and the radio did not resume after 10 calls. When CarLink audio starts without the listener, the app asks Android to rebind it and, if it is still off after 5 s, re-enables the component. Listener connect/disconnect is written to the report.
- **Car names in statistics:** Haval Big Dog 2 (001b/001c), Geely Galaxy Starshine 7 (0014/001a), Changan Eado Plus (0010/0021).

## Verified

- Core tests 65/65, build OK.
- Settings scroll: reproduced and fixed on the emulator (16 apps, tap on car data, page scrolls to the end).
- Listener rebind: not checked on a Huawei phone (the emulator does not allow unbinding it from outside).
