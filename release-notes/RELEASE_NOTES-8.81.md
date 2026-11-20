# XiaoDroidLink 8.81 (versionCode 227) — internal

## What changed

- **Quick actions widget: 17 sizes instead of 7** (Evgeniy, 18.11: "it only grows sideways, not down"). Any width (1–6 cells) in one or two rows, 1–3 wide in three rows, 1–2 wide in four rows; 4×1 can now be stretched down to 4×2. Buttons are laid out in as many rows as the widget is tall (a three-row widget used to squeeze them into four small rows), and a row holds no more buttons than eight need (4×2 = 4 + 4, not 5 + 3). 1×1 fits two buttons; the rest show when the widget grows.

## Verified

- Core tests 61/61, build OK.
- The new sizes are not checked on screen yet.
