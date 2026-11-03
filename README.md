# EveBL — EVE Build List

A desktop app for EVE Online to calculate and plan production chains.

## Changelog

### v2.2.2
- **Automatic updates** — fixed: the update dialog offered new versions but could not install them

> **Install this version by hand:** v2.2.0 and v2.2.1 show the update dialog but cannot install the update. Download v2.2.2 below (or use **Release page** in the dialog) and install it once; from then on EveBL updates itself.

### v2.2.1
- **Material efficiency** — ME now applies to the whole job, as in EVE, instead of being rounded up for every run. Jobs with many runs need fewer materials than before (e.g. 15 per run at ME 10 over 100 runs: 1,350 instead of 1,400)
- **Header ME** — your Material Efficiency setting is no longer reset to 10 by Calculate, and blueprints without ESI data now start at that value
- **Pinned items** — open reliably even if an item is renamed in a game update, and blueprints saved at ME 0 show ME 0
- **Mining** — the reprocessed output no longer comes out one unit short in some cases (e.g. 905 instead of 906), and the page stays fast as your history grows
- Under the hood: updated libraries and a reworked codebase

### v2.2.0
- **Multiple characters** — log in as many characters as you like and switch between them in the top-right menu, or pick **All characters** to combine their blueprints and assets (a BPO owned by anyone counts, BPC runs and asset quantities add up, the best ME wins). Your existing login is kept
- **Mining ledger** — new Mining page with your personal mining history: totals, breakdown by ore, system, character or day, any date range, and an estimate of the reprocessed minerals at your yield. EveBL keeps the history beyond the 30 days ESI provides
- **Blueprint ME** — blueprints you haven't edited now follow the selected character's ME when you switch characters
- **ESI errors** — characters whose data could not be loaded are now named in a notice with a Retry button, instead of silently showing incomplete data
- **Automatic updates** — EveBL checks for new versions on start and can install them for you (Update, Later or Skip)
- **macOS & Linux** — settings, logins and pinned items are now saved in the standard app data folder (`~/Library/Application Support/EveBL`, `~/.local/share/EveBL`); before, they could be lost between starts
- **SDE data** — updated to the latest EVE Static Data Export

> **Log in again:** characters logged in before v2.2.0 need to log in once more to grant the new mining ledger and industry jobs permissions. The Mining page shows a button for this.

### v2.1.1
- **Chain view** — fixed hover highlighting: components shared by several items (e.g. reaction materials) now correctly light up under every item that uses them, not just one
- **SDE data** — updated to the latest EVE Static Data Export

### v2.1.0
- **Production chain** — the manufacturing chain is now available directly in the Production card as a tab alongside the production list; nodes can be checked off as done without switching views
- **Ore variants** — moon ore and ice material lists no longer show quality variants (e.g. "Shining Monazite") — only the base type is listed

### v2.0.1
- Fix Windows installer packaging

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
| macOS | `macOS (universal)` |
| Linux (x64) | `Linux AppImage (x64)` or `Linux .deb (x64)` |

The `.sig`, `.app.tar.gz` and `latest.json` files are used by EveBL's built-in updater — you don't need to download them. From v2.2.0 on, EveBL offers new versions itself when it starts.

## Installation

### Windows
1. Download the `Windows Installer (x64)` `.exe`
2. Run it and follow the installer wizard
3. Launch **EveBL** from the Start Menu or desktop shortcut

### macOS
1. Download the `macOS (universal)` `.dmg`
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
