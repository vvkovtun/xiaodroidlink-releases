# XiaoDroidLink 7.16 (versionCode 62)

The home screen on the car display is now built from widgets that each user
arranges. Reason: users said the fixed layout with a landscape phone window was
inconvenient. Plan and working notes: `docs/17-widget-dashboard-plan.md`.

## What changed

- **Widget grid.** The area above the dock is a 6×4 grid. Each widget takes whole
  cells and has several sizes. Up to three screens; swipe sideways on a widget
  without its own gestures, tap the dots in the dock, or tap Home again.
- **First start:** three screens — Road (map, clock, weather, air alert, music,
  messages, assistant), Drive (next turn, speed, Home/Work routes, cameras,
  chargers, trip, car charge), Contact (phone window in portrait, last message,
  contacts, calendar, music). Five ready-made layouts in total.
- **Setup on the car screen:** gear → Widgets, or a long press on a widget (not
  while moving faster than 5 km/h). Drag a widget, or use the buttons: Move,
  Size, Configure, Remove, Add widget, Screens & presets, Done.
- **19 widgets:** map, phone screen, next turn, routes, music, messages, last
  message (read aloud), contacts, calendar, assistant, speed, cameras, trip, car
  charge, chargers nearby, clock, weather, air alert, phone status.
- **Phone screen widget** can be bound to an app from the dock or the Apps menu.
  The app is opened on the phone when its screen is shown; a 1×4 column turns the
  phone to portrait, a panel to landscape. One live app per screen, because the
  phone gives a single picture.
- **Widget settings:** per-widget switches (date, forecast, rain warning, like
  buttons, progress bar, message text, gear, contact names and others).
- **Incoming call card** over any screen, with Answer and Decline taken from the
  phone's call notification. Call audio still follows Bluetooth.
- **Dock** shows only installed apps; the settings gear moved into the dock.
- **Text** wraps or shrinks before it is cut.
- **Look:** gradient cards, thin numerals, one caption style, words instead of
  "AIR" in the air-alert widget, drawn Home and Apps icons, short animations
  (screen slide-in, menus, hints, press feedback).
- **On the phone:** choose a layout, set Home and Work addresses, pick favourite
  contacts, allow the calendar.

## New permissions

- `CALL_PHONE` — a tap on a favourite contact starts the call. Requested when
  the first contact is added; without it the dialer opens on the phone.
- `READ_CALENDAR` — the Calendar widget. Requested from its button in the app.

The Google Play Data safety form needs the two new rows listed in
`docs/PLAY_CONSOLE_FORM.md`. `PRIVACY_POLICY.md` is updated.

## Not verified

**Nothing in this release was tested in the car.** It was checked on an Android
emulator and in the phone preview only. Specifically not verified:

- the live phone picture inside the phone-screen widget (sharpness, touches,
  turning the phone to portrait) and the map in its new, narrower rectangle;
- speed and gear from the car, the camera and trip widgets while driving;
- starting a route in Google Maps or Waze from Home/Work and from a charger;
- reading a message aloud; calling a contact; the Answer button of the call
  card (Decline was tried on the emulator); the calendar with a real event;
- how the animations look at the car's frame rate.

## Not done

Quick actions, alerts along the route, music queue, speed limit in the speed
widget, voice reply, fuel stations, arranging widgets on the phone with a
preview, two apps side by side.

Local verification: emulator smoke suite on Android 16 — 89 passed, 0 failed,
2 skipped. It covers the Road layout and the pre-existing controls; edit mode,
screens, the new widgets and the call card were checked by hand through the test
hook. It does not cover the car connection, audio or Bluetooth.

APK SHA-256: `1d76b284569fbf80aeaff1cd11e3a0c1aa0602d9e7804ca17f62f2ea36d6ffca`

AAB SHA-256: `555e411a07a5f8ab7d9794396c5094e8f569a637e568626fc182441988ea6b2b`
