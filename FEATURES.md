# XiaoDroidLink features

Languages: [English](FEATURES.md) · [Українська](FEATURES.ua.md)

[← User guide](README.md) · [Widgets](WIDGETS.md)

## Videos

Presentation in English (49 s):

[![XiaoDroidLink — presentation in English](https://i.ytimg.com/vi/3C1UO75dUE4/hqdefault.jpg)](https://www.youtube.com/shorts/3C1UO75dUE4)

Short demo (13 s) of the home screen, music, messages, assistant and navigation: [youtube.com/shorts/pdWGhQM3KLc](https://www.youtube.com/shorts/pdWGhQM3KLc). All videos are on the [@XiaoDroidLink](https://www.youtube.com/@XiaoDroidLink/shorts) channel.

## Connecting

- **No code after the first time.** After the first sign-in, the car lets the phone in without a code. You only need the 6-digit code from the car display once.
- **Auto-connect.** When you open CarLink in the car, the phone finds it and connects by itself. How far away the phone "sees" the car is set in settings, from "Very far" to "Very close". The default is "Close".
- **Recovery.** If the car's Wi‑Fi drops for a moment, the app reconnects by itself and shows what is happening, such as "Open CarLink on the car screen" or "Connecting calls to the car…".
- **Disconnect** from the app or from the notification.
- Each phone gets its own random Wi‑Fi Direct address, so two people with XiaoDroidLink don't get in each other's way.

## Home screen and designs

- A home screen made of widgets: 4 screens, 23 widgets, 5 ready-made layouts. Details are on the [Widgets](WIDGETS.md) page.
- **Eight designs:** Winter, Bronze, Blue Wave, Neon, Ocean, Sunset, Classic, Retro GT. Each has a day and a night version, with glass over a photo. Pick one in gear → "Design catalog", which shows map, media and drive samples.
- **Dashboard theme:** "Auto" (day and night by sunrise and sunset), "Dark" or "Light".
- **Dock** on the left or at the bottom, your choice. Change its five shortcuts and the player for the "Music" button in gear → "Bottom dock".
- Languages: English, Українська, 中文, Français, Español. The phone's language is used by default.

## Phone apps in the car

- **"Apps" menu** on the car display. "Edit" adds or removes apps right from the car. On first start, popular installed apps are added automatically.
- **"Phone screen" mode** shows any app on the car display. Each app can remember whether it is shown landscape or portrait.
- **Touches** on the car display go to the phone through Android Accessibility. The app only taps what you touched in the car. It does not read or send anything.
- While the phone is showing its picture in the car, its own screen can be dimmed so it doesn't heat up or drain.

## Music

- Control any phone player: play and pause, previous and next track, seeking, likes.
- Cover art and title show in the "Music" widget, in the car's player and on the strip at the bottom of the windshield (HUD).
- **Voice song search:** tap the microphone on the card and say the song. In YouTube Music an exact match starts right away, otherwise you get three choices.
- **Lyrics** in sync with the music, in the "Lyrics" widget.
- **Sound over CarLink (Wi‑Fi).** Music goes to the car over Wi‑Fi, and the phone speaker is muted meanwhile. If the car goes silent, tap pause and then play on the car display: the phone hands its sound to the car again.

## Navigation

- **Any phone map**, such as Google Maps or Waze, right in the panel through screen casting. You can pan it with a finger on the car display, and the "Where am I" and "Rotate" buttons sit next to the map, not on top of it.
- **Built-in navigation on OpenStreetMap**, no screen casting needed:
  - address search (Nominatim) with up to five matching addresses;
  - several routes to choose from (OSRM);
  - next turn, distance and arrival time;
  - automatic rerouting if you leave the route;
  - spoken turn directions;
  - a blue car arrow even without a heading from the phone.
- **Route from the car display:** "Route" on the map, then type the address on the on-screen keyboard or say it through the car microphone, then pick the address and route.
- **Home and Work** in one tap, plus recent places, calendar events with an address and the nearest chargers.
- **Inertial map tracking** smooths GPS jumps. If GPS drops out or is spoofed (jamming), the arrow keeps moving at the car's speed: along the route line with directions when a route is set, otherwise by heading and the phone's gyroscope for up to 3 minutes.
- **Map without a connection:** the built-in map keeps the places you have already driven (up to 300 MB) and has a night look with readable street names.
- You can point address search and routing at your own servers in settings.

## Safety on the road

- **Speed cameras** across Ukraine from OpenStreetMap, only those in your direction. A voice warns ahead of time.
- **Air-raid alerts** for your district and region, with a spoken warning. Protection against GPS jamming: if the location suddenly jumps far away, it is ignored for 20 minutes.
- **Voice in the driver's headrest.** While music plays, warnings and route directions play as a separate stream, like the YU7's own prompts, and don't stop the music. When the music is stopped they come from the cabin speakers: a headrest prompt at that moment makes the YU7 drop the phone's music until reconnecting.
- **Private mode** hides message text and senders when you have passengers.
- The home screen can't be edited while driving.

## Calls, messages, assistant

- **Incoming call card** with "Answer" and "Decline" over any screen.
- **Calls through the car's Bluetooth.** The handset next to the clock shows whether calls are connected. Tap it to open the phone's Bluetooth car picker right on the car display. The [user guide](README.md) explains why it works this way.
- **Favourite contacts:** one-tap calling, up to four contacts.
- **Messages:** a counter of new messages per messenger, the last message with read-aloud, and a banner for new notifications.
- **Voice assistant** of the phone in one tap.

## What the app needs from the phone

| Permission | What for |
|---|---|
| Nearby devices (Bluetooth) | Find the car and join its Wi‑Fi |
| Location | Map, cameras, alerts, weather, chargers |
| Notification access | Music, Google Maps directions, messages, calls |
| Accessibility | Touches from the car display into phone apps |
| Screen casting | Phone map, "Phone screen" and sound over CarLink |
| Microphone | Voice song and address search |
| Calls, calendar | The "Contacts" and "Calendar" widgets. The app only asks from their buttons, when needed |
| No battery restriction | So Android doesn't cut the connection in the background |

Tip: don't turn on an Accessibility **shortcut** for XiaoDroidLink (the floating button, the two-finger gesture or the volume keys). One accidental touch turns the service off mid-drive. If a shortcut is on, the app will warn you.

## What doesn't work, and why

- **Car battery charge.** The Xiaomi YU7 doesn't send it over CarLink.
- **Calls over Wi‑Fi.** That needs Android system permissions, so calls go through the car's Bluetooth.
