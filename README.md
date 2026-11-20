# StreamMate releases

Public, secret-free release artifacts for StreamMate on Android phones, tablets and TV. Source is maintained separately in a private repository. No playlists, subscriptions, provider credentials or signing keys are included.

## Current update

StreamMate **0.11.0 build 463933** adds a centered navigation rail for wide touch windows, pairs the wide Live guide preview with programme details, and offers two Backup & Restore formats. The password-protected transfer can include provider logins. The password-free format covers settings and favorites.

Open **Settings → Updates → Check now** in StreamMate, or [download the APK](https://github.com/RydahDoesTech/StreamMate-Releases/releases/download/v0.11.0-463933/streammate-463933.apk). The [release page](https://github.com/RydahDoesTech/StreamMate-Releases/releases/tag/v0.11.0-463933) includes the build-specific checksum file. The anonymous APK and its signing certificate were verified, and an emulator updated in place from 463755 with its synthetic provider, favorites and reminder data intact.

APK SHA-256: `d976e62b1fdf26b26a57da4d06e638f8194eec7a07d6e21c63e0543a96217bf7`

The private source snapshot for this release was pinned after publication at `ad75234c95b2b8638802e46acbd92b5640259738`. See [release metadata](release-metadata.json) for the checks and signing fingerprint.

## Startup repair: 0.11.0 build 456257

**Build 456221 is withdrawn. Do not install it.** It omitted generated database code and crashes at startup. Build 456257 restores that code and adds compile-time and APK-class checks to prevent incomplete releases.

If StreamMate cannot open, download the current verified APK from Releases and install it **over the existing app** using Android's installer. Do not uninstall or clear data. The crashed app cannot run its own updater. This one-time repair retains the app's signing identity and data; normal credential-free GitHub updates work afterward. Working older installations can use Check now when their feed advertises the repair.

Validation: reproduced 456076 -> 456221 failure on an isolated Android 15 emulator, then tested an in-place repair. Synthetic provider/login, channel, favorite, watch-progress and settings records survived. Final release passed repeated phone/tablet starts, rendered the retained content, and opened Settings. 78 offline tests, debug/release builds, lint (zero errors, 27 warnings), credential scans and DEX implementation gates passed. Real-device/TV confirmation remains pending.

Checksums and the unchanged signing certificate fingerprint are supplied with the release. Only verified secret-free APKs may be uploaded. Signing keys stay local; there is no signing/build workflow in this public repository.
