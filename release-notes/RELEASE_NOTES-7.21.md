# XiaoDroidLink 7.21 (versionCode 67)

## What changed

- **Cancel in the widget editor.** A new Cancel button next to Done returns
  every home screen to what it was when the editor was opened: moved, resized,
  removed and added widgets, layout sets and the screens themselves.
- **App search.** Apps → Edit has a Search button with a keyboard: type part of
  a name, tap Show, and only matching apps stay. The "× text" button clears the
  search.
- **Keyboard layout switch.** With the Ukrainian interface the on-screen
  keyboard has an ABC / АБВ key, in app search and in the route window.
- **Route search in the selected map.** When Google Maps or Waze is the selected
  map, an address typed in the "Where to?" window goes straight to that app,
  as the Routes widget already did. With the built-in map nothing changes.
- **Stop navigation for Google Maps and Waze.** The Stop navigation button in
  the "Where to?" window (opened from the Next turn widget or the Route button)
  is now shown for their routes too. It presses the exit button of the map's
  notification; if there is none, a hint asks to stop the route on the phone.

## Verified

- On the emulator: Cancel restores a removed widget; app search by name
  (typing, Show, picking a found app, clearing).
- Emulator smoke suite on Android 16, quick mode: 49 passed, 0 failed,
  2 skipped. Core tests: 13 passed.

## Not verified

- Route search through Google Maps or Waze and stopping their route: this needs
  a real route on a phone. The exit button is found by its label, so an
  unexpected label in some language can make it fall back to the hint.
- Anything in the car, including the sound fix from 7.20.
- Everything listed as not verified in 7.16–7.20.

APK SHA-256: `8de592fced3ab571f0fc3ff2e4e97523ea76e9ca9f2a269c3ff9525a0194fe19`

AAB SHA-256: `5fe48f2d6b84b2bbcc206480f73c7987ffb399da19ad89719ca606132d4581dc`
