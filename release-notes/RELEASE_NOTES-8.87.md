# XiaoDroidLink 8.87 (versionCode 233) — internal

## What changed

- **New design «Модерн» (Modern)** — Kasım's (Deepal S05) Figma mockup, refined for driving: graphite cards at night, near-white by day; the left dock and the map buttons are icons in squares without labels (blue — selected dock item and navigation, grey — where am I / compass, teal «Map ▾» to change the map, «Work» is an office building); filled play button (violet at night, dark by day); bold clock. Ninth design in the catalog, which now shows five per row. Widgets and logic are the same as in every design.
- **Navigation widget without a route:** a big «Where to?» row — tapping it listens for the address at once; a keyboard button opens the route planner; chips below for Home, Work and the last place.
- **Home / Work widget:** three tiles — Route, Home, Work — each with its own icon; in a row on a wide widget, in a column on a narrow one; grey with «address not set» when there is no address.
- **Music after a call through the car:** the player paused by the call (Yandex Music, radio) used to stay paused after CarLink came back; now the app that was playing is resumed when the sound goes to the car again (Dmitry, Camry 80).
- **Player and contacts (Kasım):** equal gaps above and below the divider under the player buttons; a green handset badge on favourite contacts.

## Verified

- Core tests 65/65, translations complete, build OK.
- Modern, the new widgets and the player/contact changes checked as frames on the emulator (Modern and Classic). Taps on the new buttons, the catalog «Apply» and resuming music after a call were not checked on a phone or in a car.
