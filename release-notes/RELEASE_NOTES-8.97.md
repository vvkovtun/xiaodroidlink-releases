# XiaoDroidLink 8.97 (versionCode 243) — internal

## What changed

- **One failed Wi‑Fi Direct no longer switches a car to ordinary Wi‑Fi for good.** After 3 failed Wi‑Fi Direct tries the app joins the car network as ordinary Wi‑Fi and remembered "ordinary Wi‑Fi first" for this car. Vlad (Haval Xiaolong MAX + S25 Ultra, 22.11): one failure right after the car started — and every next session hung 30–55 s on ordinary Wi‑Fi, although Wi‑Fi Direct connects for him in about 1 s. Now the mark is kept only for a car with which Wi‑Fi Direct never worked (Roman, Haval + Honor: only ordinary Wi‑Fi connected). Within one session the fallback after 3 tries stays. Old marks are reset (new key `p2p_as_ap2:`), so every car tries Wi‑Fi Direct once again; a car where it never works spends ~18 s once and gets the mark back.

## Verified

- Core tests 65/65, build OK.
- Not checked in a car.
