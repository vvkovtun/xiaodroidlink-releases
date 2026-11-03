# XiaoDroidLink 7.11 (versionCode 57)

The gear on the phone card now opens a settings panel drawn on the car screen
instead of casting the phone app. It has the dashboard theme (Auto, Dark,
Light), auto-connect and its distance, voice warnings, audio through CarLink,
phone dimming and inertial map guidance; "More settings" still opens the app on
the phone. The theme can also be chosen in the app. Auto follows the car's
day/night signal as before. Switching from the light to the dark theme no
longer leaves light colours on the dock and the map background.

Automatic connection no longer starts from far away, for example from home
while the car is parked in the garage. A new setting under "Auto-connect"
chooses how close the phone must be: Very far, Far, Medium, Close (default) or
Very close. The level is a Bluetooth signal threshold from -100 to -60 dBm in
steps of 10. The Connect button works at any distance.

Automatic attempts are now quiet. If the car does not answer the saved sign-in
or its Wi‑Fi does not come up, the app stops without asking for a code and
waits again; pauses between failed attempts grow from 1 to 30 minutes. When the
car ends casting and its signal is below the threshold, the app does not
reconnect.

Android stops screen sharing when the phone is locked. After unlocking, the app
now shows the screen sharing prompt again so sound and the map come back with
one tap.

The background Bluetooth scan now reports every advertisement instead of only
the first one, so the app can notice the phone getting closer. Battery impact
was not measured.

Local verification: the sources compile and the APK and AAB were built. The
settings panel was checked on the Android 16 emulator in both themes: opening
from the phone card, theme and toggle taps, the close button and the dock.
Host tests, the emulator smoke suite and physical YU7 validation were not run;
auto-connect distance and quiet mode are untested on a real car.

APK SHA-256: `ffc1cb21263be46c794eebfa136e81a1144e22d24cd5b59faf0a38a6dcef5601`

AAB SHA-256: `30f88ef5f714e6e9ed175a1def1601c3ba7fa6543ae98b98356966029b3a7b89`
