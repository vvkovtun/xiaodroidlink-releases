# XiaoDroidLink 7.41 (versionCode 87)

## What changed

- Resize a widget by dragging: in edit mode the selected widget has a round handle in its bottom-right corner. Drag it and the frame jumps between the sizes this widget supports, showing the size (for example "2×2").
- If the new size would cover another widget, the frame turns red and says "occupied"; the widget keeps its size when you let go. The "Size" button still works too.
- Most widgets got more sizes: big clock, weather and speed up to 3×4 or 4×4, full-width strips for turn-by-turn, notifications and recent places, music up to 4×4, map 4×2 and 6×2. Every widget was checked at every size; sizes where text got too small or the layout broke (music 1×1 and 3×4, map and routes 1×1) are not offered.
- The widget catalog shows the size range instead of a long list.

## Verified

- Core tests: 15 passed. Emulator smoke test: 89 passed, 0 failed, 2 skipped.

APK SHA-256: `abffb2370a42c07783a44c887cba54fd38352a8fed67069d4bd069c46d30101f`

AAB SHA-256: `b110de252431f217ff0de8b638857d4c0debb7ea9a14a31ff8d8c6eaa75ae85f`
