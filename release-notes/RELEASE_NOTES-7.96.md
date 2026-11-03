# XiaoDroidLink 7.96 (versionCode 142)

## What changed

User reports from the support mailbox (26–29.10), none of them from a YU7: Toyota bZ3X, GAC Aion Y Plus, Deepal S05, Haval Xiaolong Max.

- Toyota bZ3X and GAC Aion Y Plus (car protocol version 1537) answered AuthResponse result=4 — the work modes we ask (769: normal cast, mirror window, simple launcher) are not supported — and the connection stopped at 40–50 %. Now the auth is repeated at once with 5 (normal cast + app full screen, what CarWith asks on older setups), then 1, and the accepted value is remembered.
- Deepal S05 (CarLink 3.2) asks get_app_list_request right after PLAY and shows endless loading without an answer. We now answer get_app_list (one app, XiaoDroidLink), get_app_detail_info (with the icon) and invoke_app (app_state_changed, landscape full screen). Replies carry the request's seqId with message type RES, as in CarWith.
- Haval Xiaolong Max uses Wi-Fi Direct (server info type 1001, no port): after the P2P group formed we connected to port 0. Now the same AUTH as over the car's access point runs against the group owner's 57209.
- Send report: a short form first — what isn't working or could be better, the car (prefilled from the last car certificate) and up to 3 photos (system photo picker, scaled to 1600 px JPEG), attached with the log.
- Stale core test fixed (German has a translation now).

## Verified

- Core tests 17/17. On Vadym's S25 with the XDL test build: the report form, the photo picker and the photo count.
- Not checked: any of the car fixes (no such car here; built from the users' logs and CarWith's code), photos actually attached in the mail. YU7 is not affected: it neither answers 4 nor asks for the app list.
