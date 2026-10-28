# KC Player

**Local Hardware-Accelerated Media Engine**

An offline video and music player for Android with a customizable video player, synced lyrics, stories-style short videos, a private folder and built-in media tools.

- **Version:** 1.0.0 (build 1)
- **Platform:** Android (Kotlin)
- **Developer:** Sujeet Gautam
- **Contact:** sujeetgautam563@gmail.com

---

## Download and Install

1. Open the [Releases](../../releases) page and download `kcplayer.apk` from the latest release.
2. Open the file. When Android asks, allow **Install unknown apps** for your browser or file manager.
3. Install and open KC Player. Grant media access once when asked.

Updates: KC Player checks `version.json` once a day, on start and when you tap **Check for updates** in About. If a newer version exists it shows the release notes, downloads the APK, verifies its SHA-256 and opens the installer.

> Only install the APK from this repository's Releases page.

---

## Features

### Videos
- Thumbnails, duration, resolution and format badges
- Resume playback with a progress line on each thumbnail
- Folders view, list or grid, sort and live search
- **Small Videos** row: clips under 30 seconds play in a full-screen, story-style viewer
- Multi-select with long press (Select all, Private, Share, Delete, Favorite)
- Folder view position is remembered

### Video Player
- Gestures: brightness, volume, seek, double-tap seek, long-press 2x
- Icon-only shortcuts: Subtitle, Audio, Speed, Aspect, PiP, Rotate, Sleep timer
- Customizable control layout (separate for portrait and landscape)
- Auto rotation (Auto / Portrait / Landscape)
- Aspect modes: Fit, Fill, Crop, Zoom, 16:9, with width and height adjustment on long press
- Slider controls for speed, brightness, volume and subtitle settings
- Video mirror and video enhancer
- Picture-in-Picture and optional background audio with notification and Bluetooth controls
- Support for very large files

### Music
- Now Playing page with seekbar, shuffle, repeat, queue and sleep timer
- Synced lyrics over the album art: only the current line is highlighted, tap a line to seek
- Lyrics actions: show or hide, search, edit, switch style
- Artist, Album and Genre artwork (embedded art first, then automatic online lookup, cached)
- Tag editor with thumbnails and image picker
- System equalizer integration

### Others
- **Network Stream:** play from a URL (HTTP, HLS, DASH) with recent history --coming soon
- **Status Saver:** WhatsApp statuses in one grid, pull down to refresh, folder access asked once
- **Video Downloader:** direct media links only, with a progress notification
- **Share & Receive:** send media over Wi-Fi using a QR code and PIN

### Private Folder
- Locks automatically when you leave the tab
- Restore returns files to their original folder

### Profile and Settings
- Profile photo and name
- Settings on separate pages: Appearance, Video Player, Music Player, App and Storage, About, Donate, Contact
- Light, Dark and System themes, accent colors and optional AMOLED Black
- Grid and layout options (2 to 6 columns, thumbnail size, badges)

---

## Permissions

| Permission | Why |
|---|---|
| Media / storage access | Find and play your videos and music |
| Notifications (Android 13+) | Playback and download notifications |
| Install unknown apps | Install updates from GitHub Releases |
| Folder access (SAF) | Read the WhatsApp statuses folder, asked once |
| Nearby Wi-Fi devices, Camera | Share & Receive and QR scanning, asked only when used |
| Internet | Network Stream, downloads, artwork lookup, update check |

---

## Known Issues

- Video Downloader: needs a device test and fix (URL validation, redirects, MediaStore save, service)
- App folder in `Android/data` may not appear until the app uses its external files directory
- Video enhancer and mirror: confirm both work on and off
- Landscape layouts: confirm Play/Pause and all buttons fit on small screens
- Background audio with the screen off may behave differently across phone brands
- Status Saver thumbnails and folder access persistence: verify after restart

---

## Responsible Use

The Video Downloader supports direct media links only. Download only content you own or have permission to use. KC Player does not include any site-specific bypass or DRM removal.

---

## Support the Developer

If you like KC Player, you can support its development.

- **UPI ID:** `8303660710@upi`

## Contact and Feedback

- Email: sujeetgautam563@gmail.com
- Subject for bug reports: `KC Player Feedback`

---

## Changelog

### 1.0.0
- First public release: redesigned interface, rebuilt video player, new Now Playing screen, Stories row, Private folder, Others tools, themes, and GitHub-based self-update.

---

## Release Process (for the developer)

1. Increase `versionCode` and update `versionName` in `app/build.gradle.kts`.
2. Commit and push to the private source repository.
3. Push a tag, for example `v1.0.0`.
4. GitHub Actions builds and signs the APK and publishes `kcplayer.apk` and `version.json` here.
5. Install the APK on a phone and test before sharing the link.

Never commit the keystore (`*.jks`), passwords or tokens. Keep two offline backups of the keystore.
