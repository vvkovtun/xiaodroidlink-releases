# XiaoDroidLink 7.95 (versionCode 141)

## What changed

Vadym (31.10): Play reviews show the app is used on other CarLink cars (Toyota RAV4 XA60, Toyota bZ3X), one says "doesn't expand to the whole car screen"; on the YU7 there are always empty strips; voice search found "Гоголя 1 Гатне" but not "Гатне Гоголя 1".

- The layout follows the car screen. The canvas keeps the height 1426 and takes its width from the car's aspect ratio (2000–4400); every rectangle is anchored to the left edge, the right edge or the centre.
- No more empty strips. The YU7 does not draw its bars over our frame — it shrinks the whole frame between them (photo 31.10), so the 116/166 margins we kept for them were empty on every car. The car now sees only the UI band 104..1270, filling the frame.
- The car is recognised from its certificate (Xiaomi: vendor 002F / 小米); it only decides whether the wheel voice assistant is on by default, because Xiao Ai exists only in Xiaomi cars.
- Address search: when a numbered address comes back as just the town or a street without a house, the phone geocoder is asked again with the street word of that country (вулиця, улица, calle, rue, Straße, ქუჩა, փողոց, ko'chasi) and the answer is kept only if it is more precise and in the same town.
- The wheel voice assistant is on by default for Xiaomi cars; without the microphone permission the wheel opens the phone AI, as before.
- "Send report" opens the mail app straight away, to the developer with the log attached; the app chooser only when there is no mail app.

## Verified

- On Vadym's S25 Ultra with the XDL test build (TestHook carsize): home, Apps, Settings, route planner with keyboard, left and bottom dock at 2764×1426, 1920×720, 1280×720, 1024×600 and 800×480 — all fill the frame, nothing cut off; at 800×480 small text is hard to read.
- Address search on the phone: "Гатне Гоголя 1", "Гоголя 1 Гатне", "Getafe Toledo 10", "Meudon Victor Hugo 10", "Teltow Goethe 5", "Rustavi Meskhishvili 10", "Kant Lenina 10", "Vahdat Rudaki 10" find the house or the street; "Кант вулиця …" went to Sevastopol, hence the word by country.
- Not checked in the car: the new full-frame layout on the YU7, touches, phone screen mode, voice default, report e-mail. Smoke test not run (emulator lacks memory).
