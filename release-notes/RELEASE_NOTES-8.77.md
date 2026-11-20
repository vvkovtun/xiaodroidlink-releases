# XiaoDroidLink 8.77 (versionCode 223) — internal

## What changed

- **Built-in map: picking a route goes straight to follow mode ("Where am I").** Before, the map showed the whole route for 7 s and only then followed the car; a touch during those 7 s, or no GPS fix yet, left it stuck in the overview and "Where am I" had to be pressed by hand (Vadym, 18.11). The route is already seen while picking a variant, so now the map follows the car with auto zoom right away, even before the first GPS fix.

## Verified

- Core tests 61/61, build OK.
- Not checked in a car.
