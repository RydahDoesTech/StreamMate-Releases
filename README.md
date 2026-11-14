# StreamMate releases

Public, secret-free release artifacts for StreamMate on Android phones, tablets and TV. Source is maintained separately in a private repository. No playlists, subscriptions, provider credentials or signing keys are included.

## Startup repair: 0.11.0 build 456257

**Build 456221 is withdrawn. Do not install it.** It omitted generated database code and crashes at startup. Build 456257 restores that code and adds compile-time and APK-class checks to prevent incomplete releases.

If StreamMate cannot open, download the 456257 APK from Releases and install it **over the existing app** using Android's installer. Do not uninstall or clear data. The crashed app cannot run its own updater. This one-time repair retains the app's signing identity and data; normal credential-free GitHub updates work afterward. Working older installations can use Check now when their feed advertises the repair.

Validation: reproduced 456076 -> 456221 failure on an isolated Android 15 emulator, then tested an in-place repair. Synthetic provider/login, channel, favorite, watch-progress and settings records survived. Final release passed repeated phone/tablet starts, rendered the retained content, and opened Settings. 78 offline tests, debug/release builds, lint (zero errors, 27 warnings), credential scans and DEX implementation gates passed. Real-device/TV confirmation remains pending.

Checksums and the unchanged signing certificate fingerprint are supplied with the release. Only verified secret-free APKs may be uploaded. Signing keys stay local; there is no signing/build workflow in this public repository.
