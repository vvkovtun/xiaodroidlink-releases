# XiaoDroidLink 7.91 (versionCode 137)

## What changed

Vadym: the phone screen is still visible while the car shows it; darker is wanted.

- While the car shows the phone screen ("Dim the phone" on), the phone goes to the lowest brightness the device allows (`DIM_LEVEL` 0.05 → 0, the brightness slider at its left end). The screen stays on: Android stops screen projection when it turns off. Darker is not possible from an app: Extra dim needs WRITE_SECURE_SETTINGS (adb only), and a black overlay would also go to the car.
- First release to closed testing (alpha) since 7.84: the Play notes sum up 7.85–7.91.

## Verified

- Quick smoke 49/0/2 on the emulator; the emulator has no real backlight, so the brightness was not checked. Not checked in the car.
