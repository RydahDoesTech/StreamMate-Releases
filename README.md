# StreamMate releases

Public distribution repository for StreamMate, an Android phone, tablet and TV IPTV player. Application source is maintained separately in a private repository. No playlists, subscriptions, media, provider credentials or signing keys are supplied here.

## Version 0.11.0 — build 456221

This secret-free bridge supports future in-app updates from the public `update.json` in this repository. No GitHub login or access credentials are needed. Existing app data and Android signing identity are retained. Checksum and signing fingerprints are supplied with the release.

An older app must first receive this bridge through its existing compatible update feed. Publishing here alone does not change an older installation. Build 456076's default protected feed can deliver a same-origin bridge; afterward this build migrates the old default address to GitHub. Custom addresses and update-check preferences are preserved. Device installation has not been performed or verified by these tools. Android may request its normal installation confirmation.

Validation: 79 tests passed, including two real credential-free manifest/APK checks; debug/release builds passed; Android lint zero errors and 27 warnings. APK contents were scanned for configured credentials and credential patterns, and its public download checksum and signing identity were verified. No on-device UI or installation test was performed.

Only verified secret-free APKs may be uploaded. Older credential-bearing builds must never be uploaded, even as drafts or removed assets. Signing keys remain local; this repository has no build/signing workflow. The older 456100 prerelease does not implement this GitHub transition; use the bridge build for future public-feed updates.
