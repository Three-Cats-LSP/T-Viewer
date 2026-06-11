# T-Viewer

A companion app for [LSP D-Planner](https://github.com/Three-Cats-LSP/LSP_D-planner) — open, read, and edit dive plan text files exported by LSP D-Planner directly on your Android device.

Also runs as a web app in any browser — no install required.

🌐 **Web App**: https://three-cats-lsp.github.io/T-Viewer/

---

## Android App

T-Viewer is available as a native Android app built with Capacitor by Ionic.

📲 **[Download APK](https://three-cats-lsp.github.io/T-Viewer/download.html)**

> Direct download page: https://three-cats-lsp.github.io/T-Viewer/download.html

**Installation:**
1. Open the download page on your Android device
2. Tap **Download APK**
3. Open the downloaded file from your Downloads folder
4. If prompted, allow *Install from unknown sources* in Settings
5. Install and launch T-Viewer

---

## LSP D-Planner

T-Viewer is designed to work alongside [LSP D-Planner](https://github.com/Three-Cats-LSP/LSP_D-planner) — a technical dive decompression planner supporting Bühlmann ZH-L16C + GF, VPM-B, and VPM-B/GFS algorithms.

Export a dive plan as TXT from LSP D-Planner and share it directly into T-Viewer on your Android device.

- **LSP D-Planner Web App**: https://three-cats-lsp.github.io/LSP_D-planner/
- **LSP D-Planner APK**: https://three-cats-lsp.github.io/LSP_D-planner/download.html

---

## Features

- Open `.txt` / `.log` / `.plan` / `.div` files
- Receive shared files directly from LSP D-Planner on Android
- **Edit mode** — tap the edit button to modify file contents; save back to device or discard changes with confirmation dialog
- Syntax highlighting for deco logs:
  - Section headers (cyan / blue)
  - Parameter lines — `Algorithm :`, `Depth :`, `Deco Gas 1 :` etc. (teal)
  - Data rows — `Stp`, `Asc`, `Des` etc. (amber in dark / black in light)
  - Separator lines (dim)
  - Warning keywords (orange / red)
- Dark and light theme — tap 🌙 / ☀️ to toggle
- Customizable colors — adjust any syntax or UI color per theme via the **COLORS** tab
- Font selector — choose from System Default, Monospace, Roboto Mono, Source Code Pro, JetBrains Mono, Open Sans, Noto Sans
- Pinch-to-zoom — font size shown in top bar
- No word wrap — long deco table rows scroll horizontally for clean alignment
- Copy and share text
- Drag and drop on desktop browser (web version)
- All settings persisted in `localStorage`

---

## UI

### Top Bar

| Button | Action |
|--------|--------|
| Folder icon | Open a file |
| Copy icon | Copy all text to clipboard |
| Edit icon | Enter edit mode (appears after file is opened) |
| Save icon | Save / download edited file (appears in edit mode) |
| Share icon | Share current file text |
| `?` | Open COLORS / ABOUT modal |
| Font size label | Current font size (e.g. `15px`) — pinch to zoom |
| 🌙 / ☀️ | Toggle dark / light theme |

### Edit Mode

Tap the edit button (pencil icon) to make the content area editable. The save button (floppy disk) appears in the top bar.

- **Save**: commits edits and downloads the file (or writes to device on Android)
- **Exit without saving**: if you have unsaved changes, a confirmation dialog asks whether to discard or keep editing

### `?` Modal — COLORS Tab *(opens first)*

- **Font selector** — pick the display font for the content area
- **Dark / Light sub-tabs** — edit colors independently per theme
- **Color rows**: swatch + label + hex text input + color picker
- **Reset button** — revert any theme's colors back to defaults
- Changes apply live without reloading

### `?` Modal — ABOUT Tab

- App description and feature list
- Links: T-Viewer APK download, LSP D-Planner APK download, LSP web app, both GitHub repos, Instagram, PayPal

---

## Syntax Highlighting

T-Viewer applies lightweight syntax highlighting to plain-text dive plan files:

| Class | Pattern | Dark color | Light color |
|-------|---------|------------|-------------|
| `.h` Header | All-caps lines (`DECO PLAN`, `GAS CONSUMPTION`) | cyan `#00d9ff` | blue `#004488` |
| `.s` Separator | Lines of dashes / equals / dots | dim border | grey `#cccccc` |
| `.d` Data | Lines containing depth/time units (`60m`, `3:00`) | amber `#ffb703` | black `#000000` |
| `.w` Warning | Lines with `warn`, `caution`, `deco`, `stop` etc. | orange `#ff6d00` | red `#cc3300` |
| `.l` Label | `Key : Value` parameter lines | teal `#00b8a0` | dark teal `#005544` |

All colors are fully customizable via the COLORS tab.

---

## Repository Structure

| Path | Purpose |
|------|---------|
| `index.html` | Self-contained web app — the entire viewer in one file |
| `manifest.json` | PWA manifest |
| `download.html` | Android APK download page |
| `android/` | Capacitor Android project |
| `Android Apk/` | Latest built APK (auto-updated by CI) |

---

## Deployment

Static single-file app. GitHub Pages serves `index.html` directly from `main`.

Android APK is built automatically by GitHub Actions on every push to `main` and committed back to `Android Apk/T-Viewer.apk`.

---

## Disclaimer

T-Viewer is a file viewer and editor. It does not perform any decompression calculations. Always use a calibrated dive computer and formal dive training. Use at your own risk.

---

*Developed by Three Cats LSP · [@threecats_lsp](https://www.instagram.com/threecats_lsp)*
