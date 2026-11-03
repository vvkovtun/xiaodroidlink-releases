# XiaoDroidLink 7.89 (versionCode 135)

## What changed

Vadym on 7.88: YouTube opened "like a phone", the automatic full screen hid the menu, and leaving it was awkward.

- YouTube is always landscape in phone mode (`AppLauncher.isPortrait` ignores a saved portrait for YouTube); the rail keeps its menu.
- Full screen only on request: while YouTube is in front, the 4th rail button is "⛶ Expand" instead of "Rotate". It hides the rail and shows YouTube over the whole car screen (only the 16:9 frame when YouTube itself plays the video full screen). "✕ Exit" stays in the top-right corner on top of the video (taps there go to the car, not YouTube); the wheel Back button also leaves. Leaving YouTube resets it.
- "Expand" also asks YouTube for its own full screen: if the button is hidden, the player is tapped first to show it (up to 3 tries).

## Verified

- Emulator (S25 size): rail with Expand → full screen with Exit → back to the rail; quick smoke 49/0/2. Full smoke not run (Vadym: release quickly).
