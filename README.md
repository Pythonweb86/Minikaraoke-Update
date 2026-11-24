Mini Karaoke – GitHub Update Repository

This repository hosts Mini Karaoke update files, APK releases, and the public download page.

Repository: https://github.com/Pythonweb86/Minikaraoke-Update

GitHub Pages: https://pythonweb86.github.io/Minikaraoke-Update/

Repository Files

File| Purpose
"README.md"| Project documentation and update instructions
"index.html"| Public APK download page
"update.json"| Update information for the application
"version.json"| Version information
"manifest.json"| Repository manifest

Current Release

- Version: "1.14.4"
- Release tag: "1.14.4"
- APK filename: "Mini_Karaoke_1.14.4.apk"
- APK download:

https://github.com/Pythonweb86/Minikaraoke-Update/releases/download/1.14.4/Mini_Karaoke_1.14.4.apk

Update Configuration

Raw update JSON:

https://raw.githubusercontent.com/Pythonweb86/Minikaraoke-Update/main/update.json

Version JSON:

https://raw.githubusercontent.com/Pythonweb86/Minikaraoke-Update/main/version.json

The update configuration must match the format expected by the updater inside the installed APK. These URLs alone do not guarantee that automatic updating is functional.

Publishing a New Version

Follow these steps whenever a new Mini Karaoke version is released:

1. Build the new APK.
2. Keep the same Android application package name.
3. Sign the APK using the same signing certificate as the installed application.
4. Increase the Android "versionCode" using a valid integer.
5. Create a new GitHub Release with the corresponding version tag.
6. Upload the APK using the correct versioned filename.
7. Update "update.json" with the new version, versionCode, APK URL, and release notes.
8. Update "version.json" if required by the application.
9. Update the download page if necessary.
10. Test the download and installation on an Android device.

Important Installation Requirements

- The package name must match the installed application.
- The signing certificate must match the installed application.
- The Android version must be supported.
- The new APK must have a higher versionCode.
- The APK must be a valid, correctly signed Android package.

GitHub Pages Setup

If GitHub Pages is not enabled:

1. Open repository Settings.
2. Select Pages.
3. Choose Deploy from a branch.
4. Select branch "main".
5. Select folder "/ (root)".
6. Save.

Public website:

https://pythonweb86.github.io/Minikaraoke-Update/

Testing

Before announcing any update, verify:

- The update JSON loads successfully.
- The APK download URL works.
- The downloaded APK is valid.
- The new APK installs over the existing application.
- The in-app updater correctly detects and downloads the new version.

Note: Hosting an APK and configuring update metadata are separate from implementing the automatic updater inside the Android application.

---

Mini Karaoke Update Repository
Maintained by Pythonweb86
