# XiaoDroidLink 7.57 (versionCode 103)

## What changed

- The Request button in Quick actions (webhooks: IFTTT, Home Assistant, Shelly) is easier to find:
  - the phone settings button is now "⚡ Requests: smart home, IFTTT: N" (was "Requests for Quick actions");
  - the car's Quick actions editor has a "⚡ Request…" cell that says where on the phone to add one (typing a URL with a key on the car screen is impractical);
  - when the widget already has eight buttons, the request is still saved and shows up in "+".
- Requests are kept in their own list: a request button removed from the widget stays in the car's "+" offers and comes back with one tap. The phone list marks requests that are not in the widget and deletes a request everywhere. Requests already in the widget are moved into the list on first start.

## Verified

- Core tests: 17 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- On the emulator: adding a request, removing it from the widget and adding it back from "+", the "Request…" hint, the phone button label and the add form.
- Not checked in the car.

APK SHA-256: `77e0f4eca2d1786e2513c98df87296e63b870a3357f15523478fa835ddd2d2bb`

AAB SHA-256: `f7a1c522f98e73adddcc1acb38fed788ee1e87270439a51e4734c0d125c8c0b5`
