# XiaoDroidLink Privacy Policy

Last updated: 2026-10-06

XiaoDroidLink is developed by Salon Lifestyle. It connects an Android phone to a compatible Xiaomi YU7 CarLink screen. XiaoDroidLink is an independent project and is not an official Xiaomi, Samsung, Google, Android Auto, or ICCOA product.

## Data handled by the app

XiaoDroidLink processes the following data only when the user enables the related feature:

- Bluetooth and nearby-device information to discover and connect to the car.
- Precise location for the embedded map and navigation, weather, speed-camera warnings, air-alert region, and Android Bluetooth/Wi-Fi requirements.
- Address search text and route endpoints when the user searches for or starts a route.
- Screen content after the user accepts Android's MediaProjection prompt, to show a selected phone app or the phone screen on the paired car display.
- Notification content after the user grants notification access, to show media state, navigation directions, and selected messenger status on the car dashboard.
- Audio after the user enables optional audio through CarLink, to play phone audio through the paired car.
- Accessibility window information and gestures after the user enables the service, to forward user-initiated touches from the car display and launch apps selected by the user.
- Installed app names and icons to let the user choose apps for the car dashboard.

The app does not use advertising SDKs, analytics SDKs, or crash-reporting SDKs, and does not sell personal data.

## Online services

The following optional functions send encrypted HTTPS requests to third-party services:

- OpenStreetMap tile servers for map images.
- Nominatim for user-initiated address searches.
- OSRM for route calculation and rerouting.
- Open-Meteo for weather near the current location.
- Overpass API for speed-camera data near the current location.
- Tryvoha.online for current air-alert information. The alert feed itself does not receive the phone location; region matching is performed on the device.

Location and route requests are used only to return the requested feature. These public service providers may process technical request information, including the IP address, under their own privacy policies and retention rules. Users may configure self-hosted Nominatim and OSRM endpoints in the app.

## Local car connection

Screen, audio, notification-dashboard information, and touch commands are sent only during a user-started CarLink session to the paired car over the local Bluetooth/Wi-Fi connection. XiaoDroidLink does not send that content to the developer.

## Storage, retention, and deletion

The app keeps preferences, diagnostic logs, pairing credentials, and limited map, weather, route-search, radar, and alert caches locally on the phone. This local data remains until Android clears it, the user clears app storage, or the app is uninstalled. The developer does not maintain user accounts or a server-side user database and therefore has no account data to delete.

## Security

Online service requests use HTTPS. Car pairing uses cryptographic authentication. Users control sensitive access through Android permissions, notification access, Accessibility settings, and the MediaProjection confirmation dialog.

## User choices

Users can disable permissions and special access at any time in Android settings. They can stop a CarLink session in the app or its notification. Disabling access may disable the related feature.

## Contact

Privacy and support contact: xiaodroidlink@lifestyle.salon
