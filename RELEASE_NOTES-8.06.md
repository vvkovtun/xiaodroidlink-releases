# XiaoDroidLink 8.06 (versionCode 152)

## What changed

A Play review: Ukrainian letters show up in the Russian interface.

- Camera widget status (`N камер у локальній базі`, `· локальна база`, `· офлайн`, `База камер недоступна`) was built from Ukrainian literals outside Tr; now Tr.f/Tr.t with translations in all languages.
- Car light names in the diagnostics (ближнє, дальнє, габарити, задній хід, стоп) translated.
- ru.tsv: «Для з'єднання бракує дозволу Bluetooth або Wi‑Fi» was translated with the opposite meaning («не требуется»); now «не хватает».
- Not changed: Experiments section (test build only), air-alert error text (not shown on screen).

## Verified

- Core tests 17/17, check_translations 817/817 for every language. Not checked in a car.
