# XiaoDroidLink 8.07 (versionCode 153)

Includes 8.06 (internal only): camera widget status and light names translated, inverted Russian permission text fixed.

## What changed

- Map bar with Yandex Navigator / Yandex Maps / 2GIS (GAC owner, 31.10): Home, Work and Route started our own navigation; now they open the route in the selected map app (`yandexnavi://build_route_on_map`, `yandexmaps://…?rtext=`, `dgis://2gis.ru/routeSearch/…`; text queries → search). Yandex says Navigator needs an access key for coordinates — not verified in a car.
- Map widget follows Yandex's default yellow arrow (colour detection only when a Yandex map is selected); car cursors can't be detected — widget stays centred.
- "Where am I" with no matching button logs the map's clickable labels, to learn Yandex's wording.
- Abroad (Deepal in Minsk, 31.10): the empty air-alert tile is replaced once by the phone widget where the screen has none.

## Verified

- Core tests 17/17, translations 817/817. Not checked in a car; Yandex parts need an owner with Yandex.
