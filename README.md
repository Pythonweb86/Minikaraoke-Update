# Mini Karaoke – GitHub Update Repository

This repository hosts the Mini Karaoke APK releases, the update information read by the app, and a public download page.

- Repository: https://github.com/Pythonweb86/Minikaraoke-Update
- Download page (GitHub Pages): https://pythonweb86.github.io/Minikaraoke-Update/

## Files

| File | Purpose | Used by |
|---|---|---|
| `version.json` | Latest version information | **The Mini Karaoke app** (Settings, Check for App Update) |
| `update.json` | Same information for the website | `index.html` (download page) |
| `index.html` | Public APK download page | Browsers |
| `manifest.json` | Legacy manifest (kept for older app builds) | Not read by v1.14.4 |
| `README.md` | Documentation | People |

## Current release

- Version: 1.14.4 (Android versionCode 11404)
- Release tag: `1.14.4`
- APK filename: `Mini_Karaoke_1.14.4.apk`
- APK download: https://github.com/Pythonweb86/Minikaraoke-Update/releases/download/1.14.4/Mini_Karaoke_1.14.4.apk

## What the app reads

The app reads only this file:

https://raw.githubusercontent.com/Pythonweb86/Minikaraoke-Update/main/version.json

Fields: `version` (text), `versionCode` (whole number, no quotes, must be higher than the installed app), `apkUrl`, `sha256` (optional, 64 hex characters of the APK), `releaseNotes`, `releasePage`.

GitHub may cache the raw file for up to about 5 minutes after you edit it.

## Publishing a new version

1. Build the new APK with the same package name (`app.jerics.karaoke`) and the same signing key.
2. Use a higher `versionCode` than the previous release.
3. Create a GitHub Release whose tag is the version, e.g. `1.14.5`.
4. Upload the APK named `Mini_Karaoke_<version>.apk`.
5. Compute its SHA-256 (`sha256sum Mini_Karaoke_<version>.apk`).
6. Update `version.json` and `update.json` (version, versionCode, apkUrl, sha256, notes). Keep `manifest.json` in step if you want.
7. Check each JSON file is valid (no missing commas, `versionCode` is a plain number).
8. Wait about 5 minutes, then test Check for App Update on a phone with the previous version.

## Installation requirements

- Same package name and the same signing certificate as the installed app.
- A higher `versionCode`.
- Android 8.0 (API 26) or newer.

Android always asks the user to confirm an installation.
