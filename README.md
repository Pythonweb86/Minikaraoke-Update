# 🎤 Mini Karaoke — Neon Update Center

<p align="center">
  <strong>🌌 Your music. Always updated. 🌌</strong><br>
  Official APK release and update information repository.
</p>

<p align="center">
  <a href="https://jericlangco.github.io/Minikaraoke-Update/"><strong>✨ Open Neon Download Center</strong></a>
  ·
  <a href="https://github.com/jericlangco/Minikaraoke-Update/releases/latest"><strong>📦 View Releases</strong></a>
</p>

## 💿 Current release

| Detail | Value |
|---|---|
| Version | **v1.14.4** |
| Android versionCode | `11404` |
| APK file | `Mini_Karaoke_1.14.4.apk` |
| Release | [Mini Karaoke v1.14.4](https://github.com/jericlangco/Minikaraoke-Update/releases/tag/1.14.4) |
| Direct APK | [Download APK](https://github.com/jericlangco/Minikaraoke-Update/releases/download/1.14.4/Mini_Karaoke_1.14.4.apk) |

## 📁 Repository files

| File | Purpose |
|---|---|
| `version.json` | Update metadata read by the Android app |
| `update.json` | Release metadata used by the public download page |
| `index.html` | Neon-themed public APK download page |
| `manifest.json` | Legacy manifest retained for older builds |
| `midi-library/` | Karaoke MIDI library |

## 🔄 How the update system works

- The Android app reads `version.json`.
- The public download page reads `update.json`.
- Both metadata files point to the APK attached to the GitHub Release.
- The download page presents a direct APK download button.

## 🚀 Publishing a new version

1. Build the APK using the same application package and signing key.
2. Set a `versionCode` higher than the previous release.
3. Create a GitHub Release with a matching version tag, such as `1.14.5`.
4. Upload the APK asset, following the filename pattern `Mini_Karaoke_<version>.apk`.
5. Update `version.json` and `update.json` with the new version, version code, APK URL and release notes.
6. Validate both JSON files before publishing.
7. Test the app's update check and the public download page.

## 📱 Installation notes

- Android requires user confirmation before installing an APK.
- In-place updates require the same package name and signing certificate.
- Only download and install APK files from sources you trust.

---
<p align="center">Built and maintained with 🎶 by <strong>Jeric Langco</strong></p>
