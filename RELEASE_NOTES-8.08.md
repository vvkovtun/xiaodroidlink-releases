# XiaoDroidLink 8.08 (versionCode 154)

Includes 8.07 (internal only): Yandex/2GIS routes from the map bar, Yandex yellow arrow, phone widget instead of the empty air alert abroad, camera widget translations.

## What changed

A user asked to use one phone with several cars, connecting automatically to whichever car they sit in.

- Auth keeps each car's key (`car_auth_pk:<BT address>`) and pass (`car_auth:<BT address>`); `selectCar` loads the near car's keys into the working fields before connecting, `rememberCar` stores them back after a successful AuthResponse / issued authentication.
- A key saved by an older version has no owner: it is tried with the first car and becomes that car's.
- A car whose key we don't have: PIN once (no wasted quick attempt with another car's key). In background auto-connect such a car is skipped quietly (parking lots).
- Background auto-connect starts if any car is known (`knowsAnyCar`).
- Car Bluetooth addresses were checked in all user logs: stable per car.

## Verified

- Core tests 17/17. Not checked in a car: YU7 must still connect without a code after the update.
