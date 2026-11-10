# XiaoDroidLink 8.54 (versionCode 200)

## What changed

- **Haval: 35 s for the car to take the call** (`CarLinkService.holdCarLinkForCall`, `CarSession.slowCarCallPickup`). Vlad (8.53, 10.11 21:26): with «Calls through the car» CarLink paused, the car did not connect the call profile in 8 s, CarLink came back and the car answered «not a CarLink» until the call ended. Haval needs ~28 s (8.52 report). Jetta and Camry 80 keep 8 s.
- **Toyota Camry 80 in the confirmed cars list** (README, 17 languages).

## Verified

- Core tests 53/53, build OK.
- Not tested in a car.
