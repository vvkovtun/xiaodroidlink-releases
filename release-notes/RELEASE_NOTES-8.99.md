# XiaoDroidLink 8.99 (versionCode 245) — internal

## What changed

- **Freeze fix (Play, 21.11, Redmi Note 13 Pro+, HyperOS, 8.84).** The app updated its status notification on the main thread and waited for the system (`onProjectionChanged → NotificationManager.notify`). All notifications (status, code from the car, Bluetooth, screen sharing permission, accessibility) are now handed to the system on a separate thread `carlink-notify`, in the same order; only the newest status is posted.
- **Other places where the main thread could wait.** The audio watchdog restarts stuck audio capture off the main thread (it needs the stream lock, which the video start can hold for 4–7 s while connecting). App lists in the phone settings (the app chooser and the list of chosen apps) show rows at once and load icons and names in the background.
- **Auto-connect decisions in the report.** The report had nothing between sessions, so it could not show whether the phone heard the car while the person was waiting (Vadym, 24.11). Now each decision is written: background scan started, car seen but too far (with signal level), pause after a manual disconnect or a failed try, signal from an unknown car, scan error, connection start. The same reason is written at most once per 5 minutes.

## Verified

- Core tests 65/65, build OK.
- Not checked on a phone or in a car.
