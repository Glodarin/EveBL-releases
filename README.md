# EveBL — EVE Build List

A desktop app for EVE Online to calculate and plan production chains.

## Changelog

### v1.2.2
- **Ore source** — moon materials, basic minerals, and ice products now show the ores or ice types they are sourced from, displayed below the item name in the production list.


## Download

Pick the archive for your platform from the **Assets** section of this release:

| Platform | File |
|----------|------|
| Windows (x64) | `EveBL-win32-x64.zip` |
| macOS (x64) | `EveBL-darwin-x64.tar.gz` |
| Linux (x64) | `EveBL-linux-x64.zip` |

## Installation

### Windows
1. Download `EveBL-win32-x64.zip`
2. Extract the archive anywhere you like
3. Run `EveBL.exe`

No installer needed — the folder is self-contained and can be moved freely.

### macOS
1. Download `EveBL-darwin-x64.tar.gz`
2. Extract: `tar -xzf EveBL-darwin-x64.tar.gz`
3. Open `EveBL-darwin-x64/EveBL.app`

> **First launch:** macOS may block an unnotarised app. Right-click `EveBL.app` → **Open** → **Open** to bypass Gatekeeper.

### Linux
1. Download `EveBL-linux-x64.zip`
2. Extract the archive
3. Make the binary executable: `chmod +x EveBL-linux-x64/EveBL`
4. Run `EveBL-linux-x64/EveBL`

## Data

EveBL ships with pre-processed EVE SDE data. No account or API key is required for basic use.

Optional: log in with your EVE SSO account to load your characters' owned blueprint data.

## Settings persistence

Your pinned items, material efficiency values, and other settings are stored locally in your OS user-data folder and are never touched by an update.
