# XiaoDroidLink 7.48 (versionCode 94)

## What changed

- The phone's map in the map widget follows the widget's shape. When the space left of the button bar is narrower than a square, the phone is turned upright (portrait); otherwise it stays landscape. The service re-applies the rotation when the widget changes shape (`DashboardLayout.onMapShapeChanged`).
- With "fill" on, the phone picture is cropped by at most 25 % of its width or height; the rest of the widget is letterboxed. Before, full cropping could leave only a thin strip of a landscape map in a narrow widget.
- In a low map widget the bar buttons show icons only.

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- On the emulator, map widgets 2×4 (portrait, fills), 3×4 (portrait, side margins) and 4×2 (landscape, fills) captured with `glshot`.
- Not yet checked in the car.

APK SHA-256: `d609821950b2a642cf603b2e2844cfde2a3cf9154b0e0f1ed001cc36c38f70a8`

AAB SHA-256: `86b47c5213a825882d90008d50a0a552750d4b7d3229485e37d55786d708f8c5`
