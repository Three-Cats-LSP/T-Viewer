# T-Viewer

Lightweight text file viewer for Android — companion app to [LSP D-Planner](https://github.com/Three-Cats-LSP/LSP_D-planner).

🌐 **Web Version**: https://three-cats-lsp.github.io/T-Viewer/

---

## Android App

📲 **[Download T-Viewer.apk](https://github.com/Three-Cats-LSP/T-Viewer/raw/main/Android%20Apk/T-Viewer.apk)**

**Installation:**
1. Open the download link above in Chrome on your Android device
2. Tap **Download** when prompted
3. Go to *Settings → Apps → Special app access → Install unknown apps → Chrome* → enable
4. Open the downloaded APK and tap **Install**

---

## Overview

T-Viewer opens text files exported from LSP D-Planner — deco logs, dive plans, slates — directly on your phone. Files can be opened from the Files app, shared from LSP D-Planner via the Android share sheet, or dragged and dropped in the browser version.

---

## Features

- Open `.txt` / `.log` / `.plan` files via native Android file picker
- Receive files shared from LSP D-Planner (or any app) via Android **Open with / Share**
- Drag & drop in browser version (desktop)
- Dive-plan syntax highlighting — headers, depths, warnings, labels
- Font size zoom: slider, `+`/`−` buttons, pinch-to-zoom
- Zoom saved between sessions
- Share text via Android native share sheet
- Copy full text to clipboard
- Keyboard shortcuts: `Ctrl+O` open, `Ctrl+±` zoom
- PWA installable — works offline
- Zero external dependencies — single `index.html`

---

## Stack

| Package | Version |
|---|---|
| Capacitor | 6.2 |
| `@capacitor/android` | 6.2.0 |
| `@capacitor/app` | 6.0.0 |
| `@capacitor/filesystem` | 6.0.1 |
| `@capacitor/share` | 6.0.4 |

---

## Build locally

```bash
npm install
npx cap sync android
npx cap open android   # opens Android Studio → Build → Generate APK
```

APK is built automatically by GitHub Actions on every push to `main` and committed to `Android Apk/T-Viewer.apk`.

---

## Repository Structure

| Path | Purpose |
|------|---------|
| `index.html` | Entire app — single self-contained file |
| `manifest.json` | PWA manifest for browser install |
| `android/` | Capacitor Android project |
| `Android Apk/` | Latest built APK (auto-updated by CI) |
| `App Icon/` | Icon source PNG |

---

*Three Cats LSP · [@threecats_lsp](https://www.instagram.com/threecats_lsp)*
