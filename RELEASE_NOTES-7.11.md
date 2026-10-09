# XiaoDroidLink 7.11 (versionCode 57)

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

Local verification: the sources compile and the APK and AAB were built. Host
tests, emulator smoke checks and physical YU7 validation were not run for this
release.

APK SHA-256: `c872f7fdc3eb11fdce9125083d280d15d7cc46078d2f2145f42e675a1f944f0f`

AAB SHA-256: `ef7a8e49d68ee98ba9cf210f0556bf5e49e2c968354e64688449fe03b02ec7e4`
