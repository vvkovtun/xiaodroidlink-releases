# XiaoDroidLink 8.56 (versionCode 202) — internal only

## What changed

- **«Mi Auto» widget card for Xiaomi cars** (`HomeGrid.MIAUTO`, `DashboardController.addMiAuto`). The last catalog cell adds the «Phone screen» widget with Mi Auto (`com.mi.car.mobile`) inside, or switches an existing one to it. Shown only when the car is Xiaomi. Mi Auto is also in the app list of the «Phone screen» widget.
- **Mi Auto translated on the car screen** (`MiAutoDictionary`, `CarAccessibilityService.updateMiAuto`, `DashboardRenderer.drawMiAutoTranslation`). While the widget shows Mi Auto, the accessibility service reads its visible labels with their bounds (after content changes and every 2 s); each fully translated label gets a plate in Mi Auto's own style (white, dark in night mode, same text size, short labels centered) drawn in our car frame over the phone picture (`onTop`). Nothing is drawn over Mi Auto on the phone itself. Labels left with any Chinese are not shown and are logged once as `miauto untranslated:`.
- **Dictionary**: 3,822 labels from Mi Auto 2.8.2 (`scripts/miauto_strings.py`, `scripts/miauto/translations.tsv`, `build.py` → `probe/assets/miauto/{en,uk,ru}.tsv`, 644 KB). Shop and legal texts excluded; face verification and real-name prompts kept (needed to bind the car and the phone key). Other app languages see English.

## Not for production yet

Reading Mi Auto's window continuously is a new AccessibilityService use. Before production: update the in-app disclosure and the Play Console accessibility declaration.

## Verified

- Core tests 55/55 (new: dictionary whole/longest-piece/half-translated), build OK.
- Not verified on screen: plate placement on the car emulator or in the car.
