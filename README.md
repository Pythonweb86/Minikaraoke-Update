# Mini Karaoke GitHub updater starter

Repository: https://github.com/Pythonweb86/Minikaraoke-Update

## Files
- `index.html` — simple public download page (GitHub Pages).
- `update.json` — provisional update metadata template.

## Current release
- Tag: `1.14.2`
- APK asset: `Mini_Karaoke_1.14.2.apk`
- Current APK URL: `https://github.com/Pythonweb86/Minikaraoke-Update/releases/download/1.14.2/Mini_Karaoke_1.14.2.apk`

## IMPORTANT: updater integration is not complete yet
The uploaded APK contains an updater implementation, but the exact configuration format and update-check URL must be confirmed from its DEX code before this `update.json` can be treated as compatible. Do not paste the JSON URL into MT Manager blindly.

The APK also contains a MediaFire URL for `Mini_Karaoke_1.17.4.apk` in its compiled strings. That is evidence of a URL embedded in this APK, not proof that it is the only update source or that it uses this JSON schema.

## Recommended process for future releases
1. Build the new APK with the same application ID/package name and the same signing certificate as the installed app.
2. Increase Android `versionCode`.
3. In GitHub, create a new Release with a higher tag, e.g. `1.14.3`.
4. Upload the new APK. For a stable latest-download URL, name the release asset exactly `Mini_Karaoke.apk` in every release. If you keep versioned filenames, the URL must change each time.
5. Update `update.json` and `index.html` with the new version, versionCode, and APK URL.
6. Publish the release and verify the download on a device before announcing it.

## Enable GitHub Pages
In the repository, open Settings > Pages. Choose Deploy from a branch, select `main` and `/ (root)`, then Save. The site should appear at:
https://pythonweb86.github.io/Minikaraoke-Update/

The raw JSON URL (once committed to the `main` branch) is:
https://raw.githubusercontent.com/Pythonweb86/Minikaraoke-Update/main/update.json
