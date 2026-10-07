# Local Cast

Local Cast is a privacy-focused Android app that shares media from your phone with compatible players on your local Wi-Fi network. It advertises a browsable UPnP/DLNA media library and provides HTTP streaming with byte-range support for seeking.

## Features

- Select and share multiple media files at once
- Browse Local Cast from compatible UPnP/DLNA players, including VLC
- Stream files over HTTP with byte-range support for seeking
- Open a local web library or LAN remote from another device on the same network
- Light, dark, and system appearance options
- No account, cloud storage, or media uploads

Local Cast only shares files you select. While the server is running, those files are accessible to devices on the same local network. Use a trusted Wi-Fi network.

## Requirements

- Android 8.0 (API 26) or later
- Phone and receiving device on the same Wi-Fi network
- A player that supports UPnP/DLNA browsing or HTTP media URLs, such as VLC or Nova Player

Some guest Wi-Fi networks block local device discovery. If Local Cast does not appear in the player immediately, wait a few seconds or use the HTTP library link shown in the app.

## How to use

1. Install Local Cast on your Android phone.
2. Connect your phone and TV or player to the same Wi-Fi network.
3. Open Local Cast and choose one or more media files.
4. Tap **Start Local Cast**.
5. On the TV, open VLC or another compatible player and browse **Local Network → Local Cast**.
6. Choose a file from the library and play it.
7. Tap **Stop Local Cast** when you are finished.

The app also shows an HTTP address. With multiple files selected, opening that address displays the library; with one file selected, it opens that file directly. Each media URL supports HTTP byte ranges so compatible players can seek within the file.

## LAN media remote

While Local Cast is running, open the remote URL shown in the app from a browser on a device on the same Wi-Fi network. The remote can browse the selected library, move between files, and open the selected file.

It does not control a TV's volume, channels, or another app's playback. Those features require a TV- or player-specific control API and are not available through generic UPnP media-server discovery.

## Screenshot of app in Light Mode

<img width="1224" height="5091" alt="Screenshot_20261007-173407" src="https://github.com/user-attachments/assets/63711590-a8d5-4257-abf1-97bfad171957" />

## Screenshot of app in Dark Mode

<img width="1224" height="5091" alt="Screenshot_20261007-173356" src="https://github.com/user-attachments/assets/54daab49-0e3c-40c7-a991-60f861d20a08" />


## Install

Download the latest APK from [GitHub Releases](https://github.com/rishabhnjadhav/Local-Cast/releases).

For an APK installed outside Google Play, Android may ask you to allow installs from the browser or file manager you use to open it. Review the prompt and approve the install to continue.

## Update checks

Local Cast supports update checks for APK releases. In **Settings → Update source**, enter the HTTPS URL of a JSON manifest and tap **Check for updates**. The manifest publisher must host both the JSON file and APK. For example:

```json
{
  "versionCode": 4,
  "versionName": "1.3.0",
  "apkUrl": "https://your-release-host/LocalCast-1.3.0.apk",
  "releaseNotes": "What changed in this release"
}
```

When a newer version is found, Local Cast opens the APK link in the browser. Android requires the user to install the downloaded APK; updates are not installed silently. The APK must use the same package ID and signing key as the installed app. Version 1.1.0 does not include the update checker, so users on 1.1.0 need to install version 1.2.0 from the Releases page once before using in-app checks.

If Local Cast is distributed through Google Play, use Google Play's update flow instead of sideloaded APK updates.

## Font

Local Cast uses Android's system `sans-serif` font family. Devices with Oh My Font installed can apply their system sans-serif font to the app. Local Cast does not bundle Oh My Font's typeface files.

## Build from source

1. Install Android Studio, JDK 17, and Android SDK Platform 35.
2. Open the `LocalCast-MVP` project folder in Android Studio and sync Gradle.
3. Run the `app` configuration on an Android device or build an APK from Android Studio.

## Version

Current version: **v1.2.0**

## Developer

Made by **Rishabh Jadhav**❤️.
