# XiaoDroidLink 8.10 (versionCode 156)

Includes 8.08 and 8.09 (internal only).

## What changed

- Client info `band` / `channel` as in CarWith (`BtController.M/N`): `band` = phone supports 5 GHz; with band 1 and AP mode (1002) the phone keeps its 5 GHz channel, and from 2.4 GHz, 6 GHz or no Wi-Fi asks for channel 36. Before: band always 1, a 2.4 GHz channel was sent as is and 6 GHz as channel 1, so the car could raise its CarLink network in a band the phone can't use alongside home Wi-Fi (Alexey's Fold6 kept searching; Vadym at home). The log shows the phone frequency and the channel sent.

## Verified

- Core tests 17/17. Not checked in a car: YU7 at home on Wi-Fi and without Wi-Fi; Wi-Fi Direct cars (Haval, Wuling) get the new channel too.
