# XiaoDroidLink Privacy Policy

Last updated: 2026-11-21

XiaoDroidLink is developed by Salon Lifestyle. It connects an Android phone to a compatible Xiaomi YU7 CarLink screen. XiaoDroidLink is an independent project and is not an official Xiaomi, Samsung, Google, Android Auto, or ICCOA product.

## Data handled by the app

XiaoDroidLink processes the following data only when the user enables the related feature:

- Bluetooth and nearby-device information to discover and connect to the car.
- Precise location for the embedded map and navigation, weather, speed-camera warnings, air-alert region, and Android Bluetooth/Wi-Fi requirements.
- Address search text and route endpoints when the user searches for or starts a route.
- Screen content after the user accepts Android's MediaProjection prompt, to show a selected phone app or the phone screen on the paired car display.
- Notification content after the user grants notification access, to show media state, navigation directions, and selected messenger status on the car dashboard.
- Incoming call notifications (caller name and the notification's Answer/Decline actions), to show a call card on the car dashboard. Nothing is stored or sent to the developer.
- Favourite contacts: only the name and number of each contact the user picks in the system contact picker (up to four), stored on the phone for the Contacts widget.
- Contacts (optional, read-only): when the user asks by voice to call someone ("call Olena"), the app searches the phone's contacts for that name to start the call. Contacts are read only on the phone at that moment; they are not stored by the app and not sent to the developer or any service.
- Phone call permission (optional), so a tap on a favourite contact starts the call. Without it the phone's dialer opens instead.
- Phone call management (optional): to answer, decline and end an ordinary call from the car screen and to know when the phone is ringing or in a call. The app does not read call history or phone numbers for this, and nothing is stored or sent to the developer.
- Calendar (optional, read-only): the title, time and location of the next event within 24 hours, shown on the Calendar widget. It is read on the phone and not stored or sent to the developer.
- Microphone, only after the user taps a voice button on the car screen or presses the assistant button on the steering wheel: speech is turned into text by the phone's speech recognition service (for example, Google speech services) to search for an address or a song, to call a contact, or to repeat a car command in Chinese. After a car command, the microphone briefly listens to the car assistant's spoken reply to show it as text.
- Audio after the user enables optional audio through CarLink, to play phone audio through the paired car.
- Accessibility window information and gestures after the user enables the service, to forward user-initiated touches from the car display and launch apps selected by the user.
- Installed app names and icons to let the user choose apps for the car dashboard.

The app does not use advertising SDKs, analytics SDKs, or crash-reporting SDKs, and does not sell personal data.

## Anonymous usage statistics

To learn which cars work, where connection fails and which features people use, the app sends anonymous usage statistics to Google Analytics (Google Analytics 4 Measurement Protocol, sent directly over HTTPS without a Google SDK). It is on by default and can be turned off at any time in the app settings ("Anonymous statistics"); turning it off also deletes events not yet sent.

What is sent:

- A random app-instance number created on the phone (not linked to the user's name, Google account, phone number or advertising ID).
- App version, app language, phone manufacturer and model, Android version, and the country code of the SIM card.
- Car identification from the car's CarLink signal and certificate: manufacturer and model codes and the car's model name.
- Chosen design and theme, map app, list of widget types on the dashboard, and whether optional features (Accessibility, audio through CarLink, auto-connect, computer helper) are enabled.
- For each connection attempt: how far it got (search, code, Wi-Fi, login, streaming), the reason shown to the user if it failed, whether a code was needed, and how many seconds it took.
- After each trip: its length in minutes, the number of connection drops, whether audio and screen casting worked, the package name of the music player, and how many times routes, voice, quick actions, manual position and car calls were used; and once a day whether the app was used in the car for at least five minutes.

What is never sent: location, addresses or routes, contacts, call or message content, notifications, screen content, Wi-Fi network names, Bluetooth or MAC addresses, phone numbers or e-mail addresses.

Google processes this data under the Google Analytics terms and the Google Privacy Policy (https://policies.google.com/privacy); Google may see the phone's IP address when it receives a request. Event-level data is kept for two months (the Google Analytics default); only aggregated reports are kept longer.

## Online services

The following optional functions send encrypted HTTPS requests to third-party services:

- OpenStreetMap tile servers for map images.
- Nominatim for user-initiated address searches.
- OSRM for route calculation and rerouting.
- Open-Meteo for weather near the current location.
- Overpass API for speed-camera data near the current location.
- lrclib.net for song lyrics: the title, artist and length of the track that is playing are sent, only while the Lyrics widget is on a home screen.
- YouTube Music (music.youtube.com) for user-initiated song searches by voice: the spoken song title and artist are sent.
- Google Translate (translate.googleapis.com) to translate the car assistant's spoken reply into the app language: only the text of that reply is sent, nothing about the user.
- Tryvoha.online for current air-alert information. The alert feed itself does not receive the phone location; region matching is performed on the device. When Tryvoha.online is unavailable, the same public alert list is requested from ubilling.net.ua.

Location and route requests are used only to return the requested feature. These public service providers may process technical request information, including the IP address, under their own privacy policies and retention rules. Users may configure self-hosted Nominatim and OSRM endpoints in the app.

## Local car connection

Screen, audio, notification-dashboard information, and touch commands are sent only during a user-started CarLink session to the paired car over the local Bluetooth/Wi-Fi connection. XiaoDroidLink does not send that content to the developer.

## Storage, retention, and deletion

The app keeps preferences, diagnostic logs, pairing credentials, and limited map, weather, route-search, radar, and alert caches locally on the phone. This local data remains until Android clears it, the user clears app storage, or the app is uninstalled. The developer does not maintain user accounts or a server-side user database and therefore has no account data to delete.

## Security

Online service requests use HTTPS. Car pairing uses cryptographic authentication. Users control sensitive access through Android permissions, notification access, Accessibility settings, and the MediaProjection confirmation dialog.

## User choices

Users can disable permissions and special access at any time in Android settings, and turn off anonymous statistics in the app settings. They can stop a CarLink session in the app or its notification. Disabling access may disable the related feature.

## Contact

Privacy and support contact: xiaodroidlink@lifestyle.salon
