# XiaoDroidLink 8.53 (versionCode 199)

## What changed

- **Calls: phone speakerphone by default for every car** (`NotifySettings.on`, `call_via_car` default off). With «Calls through the car» CarLink pauses for the whole call and the car screen loses the map and navigation — inconvenient while driving (Vadym, 10.11). Now the stream keeps running and the call goes to the phone speakerphone; «Calls through the car» (Jetta VS8, Camry 80, Haval) is an opt-in switch in Notifications and calls. People who already switched it keep their choice.
- **Haval: warning when calls go through the car** (`CarSession.slowCarCallPickup`). Vlad (8.52, 10.11 19:59): the car connected the call profile 28 s after CarLink paused (Jetta: 4–5 s). The car screen now says «The car picks up the call after up to 30 s — until then the call is on the phone» (15 languages). The 8 s fallback stays (one case so far).

## Verified

- Core tests 53/53, build OK.
- Speakerphone path for Haval confirmed in Vlad's 8.52 report (call at 19:56, stream kept, speaker on).
- Not tested in a car.
