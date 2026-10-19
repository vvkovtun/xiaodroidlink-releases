# XiaoDroidLink 7.51 (versionCode 97)

## What changed

- The Wi-Fi Direct (P2P) MAC that the phone gives the car during the Bluetooth handshake (characteristic 103 and the client-info `mac` field) was a hard-coded address of the developer's phone, the same in every install. The original CarLink sends the phone's real P2P MAC, which a non-system app cannot read (Android returns 02:00:00:00:00:00). Now each install generates a random locally administered unicast address once, stores it and keeps sending it. YU7 connects over its own SoftAP and does not advertise P2P, so this field is most likely unused there. A manual value in Diagnostics still overrides it.

## Verified

- Core tests: 16 passed. Emulator smoke test: 88 passed, 0 failed, 2 skipped.
- Not yet checked in the car.

APK SHA-256: `5660577b00f95ab1c5c4d03d9cdf31845125f01559f6f228db196d6cd8282158`

AAB SHA-256: `67f7851e44be47847e316bb8fda1b187ca0f7aa366d01a488ca4ed5bbcad6642`
