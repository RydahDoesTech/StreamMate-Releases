# StreamMate releases

Public distribution repository for StreamMate, an Android phone, tablet and TV IPTV player. Application source is maintained separately in a private repository. No playlists, subscriptions, media, provider credentials or signing keys are supplied here.

## Version 0.11.0 — build 456100

The release contains a secret-free APK signed with the existing StreamMate identity. SHA-256 and signing certificate fingerprints are recorded in `SHA256SUMS` and `release-metadata.json`. Android will ask for installation approval where required.

**Updater transition is pending.** This build retains its previously configured protected update endpoint. Publishing it here does not automatically migrate existing installations to GitHub. Do not change an installed app's update URL to this repository: this version does not support GitHub release download redirects. It is not yet a guarantee of future credential-free in-app updates.

Validation: 67 unit tests passed; debug/release builds passed; Android lint had zero errors and 27 warnings. No on-device installation or TV/phone interaction test was performed for this release. APK contents were scanned for configured credentials before publication.

Only verified secret-free APKs may be uploaded. Older credential-bearing builds must never be uploaded, even as drafts or removed assets. Signing keys remain local; this repository has no build/signing workflow.
