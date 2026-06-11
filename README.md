# T-Viewer

Lightweight Unicode text file viewer for Android — companion app to [LSP D-Planner](https://github.com/Three-Cats-LSP/LSP_D-planner).

## Download

**[⬇ Download T-Viewer.apk](https://github.com/Three-Cats-LSP/T-Viewer/raw/main/Android%20Apk/T-Viewer.apk)**

> Sideload only — not on Google Play. Enable *Install unknown apps* in Android settings before installing.

## Web Version

**[🌐 Open in Browser](https://three-cats-lsp.github.io/T-Viewer/)**

Works on desktop and mobile browsers. Drag & drop a file or tap **OPEN FILE**.
Can also be installed as a PWA (Add to Home Screen on iOS/Android, or install from Chrome on desktop).

## Features

- Open `.txt` / `.log` / `.plan` files via native Android file picker
- Accept files shared directly from LSP D-Planner via Android **Open with / Share**
- Drag & drop on desktop browser
- Full UTF-8 / Unicode support
- Font size zoom: slider, `+`/`−` buttons, pinch-to-zoom
- Zoom preference saved between sessions
- Share text via Android native share sheet
- Copy full text to clipboard
- Dive-plan syntax highlighting (headers, depths, warnings, labels)
- PWA installable — works offline
- Zero external dependencies — single `index.html`

## Install (Android)

1. Open the **Download** link above in Chrome on your Android device
2. Tap **Download** when prompted
3. Go to *Settings → Apps → Special app access → Install unknown apps → Chrome* → enable
4. Open the downloaded APK and tap **Install**

## Stack

| Package | Version |
|---|---|
| Capacitor | 6.2 |
| `@capacitor/android` | 6.2.0 |
| `@capacitor/app` | 6.0.0 |
| `@capacitor/filesystem` | 6.0.1 |
| `@capacitor/share` | 6.0.4 |

## Build locally

```bash
npm install
npx cap sync android
npx cap open android   # opens Android Studio → Build → Generate APK
```

---
*Three Cats LSP · [@threecats_lsp](https://www.instagram.com/threecats_lsp)*
