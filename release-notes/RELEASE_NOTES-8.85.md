# XiaoDroidLink 8.85 (versionCode 231) — internal

## What changed

- **Car Wi‑Fi on channel 149 in countries that do not allow it.** Cars with CarLink (YU7, Lynk & Co, Jetta…) always run their Wi‑Fi on channel 149 (5745 MHz). The advice «airplane mode with a restart» used to appear only in Belarus; now it appears in every country without 5725–5850 MHz in the wireless-regdb frequency database (41 countries: Belarus, Egypt, Turkey, Japan, Georgia, Azerbaijan, Uzbekistan, Saudi Arabia, Morocco…). Case: YU7 Max + Galaxy S25 Ultra in Egypt (19.11) — the phone never saw the car network. The hint text no longer names Belarus.
- **«More: why, and other ways»** button under the steps opens the troubleshooting section `#channel-149` in the app language (Ukrainian, Russian, otherwise English). The section now lists every such country.
- New texts in 15 languages.

## Verified

- Core tests 65/65 (new: Egypt → channel 149 advice, Russia → plain advice), build OK, translations 941/941.
- The workaround is confirmed by users in Belarus only; Egypt — waiting for the user's answer.
