# Home screen widgets

Languages: [English](WIDGETS.md) · [Українська](WIDGETS.ua.md)

[← User guide](README.md) · [All features](FEATURES.md)

XiaoDroidLink builds its home screen on the Xiaomi YU7 display out of widgets, like a phone launcher. The grid has 6 columns and 4 rows. You get up to four screens: three ready-made ones and a fourth empty one for your own set. Switch screens with the "Screens 1 / 4 ›" button in the dock, or swipe sideways on an empty area.

![XiaoDroidLink home screen on the car display](images/xiaodroidlink-en-car-preview.png)

## Editing a screen

1. Tap "Edit" next to the screen switcher. Gear → "Widgets" or a long press on a widget does the same. Editing only works while parked: above 5 km/h the car shows "Edit the screen while parked".
2. Tap a widget to select it. The selected widget gets a "breathing" frame.
3. The buttons at the bottom:
   - **Move.** You can also drag the widget with a finger, and a yellow frame shows where it will land.
   - **Size.** Cycles through the allowed sizes. You can also drag a corner. Only sizes where the text stays readable and buttons stay at least ~1.5 cm are offered.
   - **Configure.** Toggles for this widget, see below.
   - **Remove.**
   - **Add widget.** The catalog of all 23 widgets, with one sentence about each.
   - **Presets.** Five ready-made layouts, plus adding or removing a screen.
   - **Done.**

If something goes wrong, "Presets" restores a ready-made layout, and cancel returns all screens to how they were before editing.

### Ready-made layouts

| Layout | Contents |
|---|---|
| Road | Map, music and messages |
| Driving | Next turn, speed, cameras and chargers |
| Contact | Phone, messages, contacts and calendar |
| Minimal | Clock, next turn and music, no map |
| Parking | Phone in portrait, messages and music |

## Widget catalog

Sizes are columns × rows. The first size listed is the one a widget is added with.

### Navigation

**Map** (3×4, 4×4, 2×4, 4×2, 6×2)
The map chosen in settings: the built-in OpenStreetMap, or Google Maps, Waze or another map app from the phone. A phone map is shown through screen casting, and you can pan it with a finger right on the car display. A strip of buttons sits to the right of the phone map, so nothing covers the map itself:
- "Where am I" presses the map's own "my location" button;
- "Rotate" shows the map landscape or portrait and remembers the choice;
- the microphone lets you say an address;
- "Route" opens the route planner on the car display.

The built-in map has `+` and `−`, "Driving ↑" (zoom 15, car centred, direction of travel up) and "Route".
Option: "Phone map: fill card (crop edges)".
Only one "live" widget can be on a screen: either the phone map or "Phone screen".

**Next turn** (2×1, 2×2, 4×2 and larger)
The next manoeuvre in large letters, such as "In 300 m turn left", plus distance and arrival time. It takes directions from the built-in navigation or from the Google Maps notification. Tap it to open the route planner.
Option: "Distance and time to arrival".

**Routes** (2×1, 1×2, 2×2 …)
Two buttons, "Home" and "Work". One tap starts the route. You set the addresses in the phone app.

**Cameras** (1×1, 2×1, 2×2 …)
Distance to the nearest speed camera ahead in your direction of travel. Cameras on the opposite lane are not shown. Camera data comes from OpenStreetMap for all of Ukraine and is refreshed once a day. It works together with the spoken warnings (turned on in settings).

**Chargers** (2×2, 3×2, 4×2)
The three nearest charging stations with their distance. Tap one to route to it.

**Recent places** (2×2, 3×2 …)
Places you have routed to before. Tap one to go there again.

### Music

**Music** (3×2, 2×2, 4×2, 5×2, 6×2, wide strips, 4×4)
Cover art, title, artist and big buttons: previous track, play/pause, next track. Tap the progress bar to seek. A small equalizer runs while music plays. The microphone on the card lets you search for a song by voice: in YouTube Music an exact title-and-artist match starts right away, otherwise you get three choices. With no active player, a tap opens the phone's last player.
Options: "Like buttons", "Progress bar and time", "Player name".

**Lyrics** (3×2, 2×2, 3×1, 4×2, 6×1, 3×4)
The lines of the current song, in sync with the music. Lyrics come from the open lrclib.net database, so rare songs may have none.

### Communication

**Messages** (2×1, 2×2 …)
How many new messages you have in Telegram, Viber and other messengers. Tap to open the messenger on the car display. The "private mode" button hides message text and senders when you have passengers.

**Last message** (2×1, 3×1, 2×2, 4×1 …)
Who sent the latest message, and its text. The speaker button reads it aloud. Tap the text to open the chat.
Option: "Message text".

**Contacts** (2×1, 4×1, 2×2 …)
Up to four favourite contacts. One tap calls. Without the call permission, the dialer opens instead. You pick the contacts in the phone app under "Favourite contacts".
Option: "Names under the buttons".

**Calendar** (2×1, 3×1, 4×1, 2×2, 3×2)
The next event from the phone calendar. If the event has a location, a tap routes there.

**Assistant** (1×1, 2×1, 3×1 …)
The phone's voice assistant, such as Google Assistant, Gemini or ChatGPT, in one tap.

**Notifications** (2×2, 3×2, 2×4 …)
The latest notifications from all phone apps.
Option: "Notification text".

**Quick actions** (2×1, 3×1, 4×1, 2×2 …)
Up to eight buttons: Home, Work, favourite contacts, addresses, map points and apps. Until you change anything, the buttons fill themselves from your addresses, contacts and the "Apps" menu. Build your own set in edit mode, where you can also type an address on the on-screen keyboard.

### Drive

**Speed** (1×1, 2×2, 3×2, 3×4)
Speed and gear (P, R, N, D), as sent by the car itself.
Options: "Gear", "Car lights".

**Trip** (1×1, 2×1, 3×1 …)
Time on the road, distance and average speed for this trip.
Option: "Average speed".

**Car** (1×1, 2×2)
The car model and its battery charge, if the car sends it. The Xiaomi YU7 does not send its charge over CarLink, so the widget says "The car does not report charge".

### Time and status

**Clock** (1×1, 2×2, 2×1 … 4×4)
A large clock and the date. A handset icon next to the clock shows whether calls are connected through the car's Bluetooth. Tap it to open the phone's Bluetooth car picker right on the car display.
Options: "Date", "Car charge".

**Weather** (1×1, 2×2, 3×2 … 4×4)
Weather now and for the next days. A separate line warns about rain within the hour. Data comes from Open-Meteo for the phone's location.
Options: "Forecast for the coming days", "Rain warning".

**Air alert** (1×1, 2×2, 3×2)
The air-raid alert for your district and region: "Air alert" or "All clear". Data comes from tryvoha.online, with ubilling.net.ua as a fallback. If GPS jumps because of jamming (more than 500 km/h from the last trusted point), the new location is ignored for 20 minutes. Outside Ukraine the widget is empty.

**Phone** (1×1, 2×2, 3×2, 4×2)
Phone battery, mobile network, Wi‑Fi and Bluetooth. Tap to open settings on the car display.

### Phone screen

**Phone screen** (1×4, 3×4, 4×4)
A live picture of the phone right on the home screen: portrait at 1×4, landscape at 3×4 and 4×4. Touches on the car display go to the phone through Accessibility. You can bind the widget to an app: after adding it, pick an app from the list, and that app starts by itself whenever you open this screen. Different screens can show different apps.
Needs screen casting and Accessibility.

## Other parts of the screen

- **Dock** on the left or at the bottom: five app shortcuts, "Music", "Apps", the settings gear and "Screens 1 / 4 ›". Change the shortcuts in gear → "Bottom dock".
- **Incoming call card** appears over any screen, with "Answer" and "Decline".
- **Notification banner** briefly shows a new message. Tap it to open.
- **Red "!" banner** appears when something isn't working, such as Accessibility or notification access being off. See [on-screen errors](TROUBLESHOOTING.md) for what to do.
