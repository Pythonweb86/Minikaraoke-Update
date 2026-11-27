# 🎤 Mini Karaoke — Neon Update Center

<p align="center"><strong>🌌 Your music. Always updated. 🌌</strong></p>

<p align="center">
  <a href="https://github.com/jericlangco/Minikaraoke-Update/releases/latest"><strong>📥 Latest APK Release</strong></a>
  ·
  <a href="https://jericlangco.github.io/Minikaraoke-Website/"><strong>🌐 Official Website</strong></a>
</p>

The repository hosts Mini Karaoke Android releases and update metadata.

## Neon download page

`index.html` provides a responsive dark interface with cyan, violet and pink neon accents. Its Download APK button queries the GitHub Releases API, finds the latest `.apk` asset, and links directly to that asset's browser download URL. If the API is unavailable, it falls back to the releases page rather than guessing an APK filename.

## Important

Keep the existing update metadata files and app-facing update schema unchanged when publishing a new APK. In particular, preserve `version.json`, `manifest.json`, and any other files consumed by existing app versions unless you are intentionally updating and testing that schema.

## Publishing a new release

1. Create a GitHub Release with the new version tag.
2. Attach the signed APK file to that release.
3. Update the repository's existing app update metadata using its current schema.
4. Test the app's update check and the public download page.

Android may require user confirmation before installing an APK. In-place updates require a matching package name and signing certificate.

---
<p align="center">Maintained with 🎶 by <strong>Jeric Langco</strong></p>
