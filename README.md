# EveBL — EVE Build List

A desktop app for EVE Online to calculate and plan production chains.

## Changelog

### v2.0.0
- Full rewrite as a native desktop app (Tauri v2 + Rust + Vue 3) — ~38 MB vs ~390 MB previously

### v1.2.4
- Fix missing Material Icons in packaged builds — icons were rendering as text instead of glyphs

### v1.2.3
- Releases are now built via GitHub Actions on native runners — fixes macOS app bundle symlinks that were broken in previous Windows-built archives

### v1.2.2
- **Ore source** — moon materials, basic minerals, and ice products now show the ores or ice types they are sourced from, displayed below the item name in the production list

## Download

Pick the file for your platform from the **Assets** section of this release:

| Platform | File |
|----------|------|
| Windows (x64) | `Windows Installer (x64)` |
| macOS (x64) | `macOS (x64)` |
| Linux (x64) | `Linux AppImage (x64)` or `Linux .deb (x64)` |

## Installation

### Windows
1. Download the `Windows Installer (x64)` `.exe`
2. Run it and follow the installer wizard
3. Launch **EveBL** from the Start Menu or desktop shortcut

### macOS
1. Download the `macOS (x64)` `.dmg`
2. Open the DMG and drag **EveBL** into Applications
3. Launch from Launchpad or Spotlight

> **First launch:** macOS may block an unsigned app. Right-click **EveBL** → **Open** → **Open** to bypass Gatekeeper.

### Linux
**AppImage** (no install required):
1. Download the `Linux AppImage (x64)` `.AppImage`
2. Make it executable: `chmod +x EveBL_*.AppImage`
3. Run it: `./EveBL_*.AppImage`

**Debian/Ubuntu package:**
1. Download the `Linux .deb (x64)` `.deb`
2. Install: `sudo dpkg -i eve-bl_*.deb`

## Data

EveBL ships with pre-processed EVE SDE data. No account or API key is required for basic use.

Optional: log in with your EVE SSO account to load your character's owned blueprint data and asset quantities.

## Settings persistence

Your pinned items, material efficiency values, and other settings are stored locally in your OS user-data folder and are never touched by an update.
