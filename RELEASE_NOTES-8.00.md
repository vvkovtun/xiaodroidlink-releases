# XiaoDroidLink 8.00 (versionCode 146)

## What changed

GAC Aion Y Plus on 7.99 (report 31.10): authorization passed (result 0) and video went at 1920×976, but the car chose work modes 4 (app full screen), asked the app list and details, got no app state and tore the stream down after 30 s with nothing on screen.

- When the car itself chose app-full-screen mode (AuthResponse work modes bit 4), after answering the app details the phone tells the car XiaoDroidLink is shown full screen: app_state_changed, state 0, show, rotation 0, DisplayMode LANDSCAPE_FULLSCREEN (3), visible region 0,4 – w,h−4 — as CarWith does in that mode. Cars on the normal cast (YU7) never get it.
- invoke_app is answered with LANDSCAPE_FULLSCREEN (3), not 2 (PORTRAIT_FULLSCREEN).

## Verified

- Core tests 17/17. Not checked in a car: GAC (no such car here). YU7 is not affected (it never asks for the app list and does not choose mode 4).
