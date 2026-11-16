# NomadForge 3D

**Interactive 3D off-grid camper van & rig configurator.**

NomadForge 3D is a browser-based 3D configurator and build planner for off-grid camper vans and overland rigs. Pick a base vehicle, snap modular interior and exterior components into place, try finishes in real time, and x-ray or explode the build to inspect hidden wiring, plumbing and clearances — while live trackers keep your cost, payload, power and water budgets honest.

It's a single self-contained `index.html` (Three.js loaded from a CDN) — no build step, no install.

## Features

- **Base vehicles (2025 specs)** — Sprinter High-Roof (144/170/170 EXT), Transit (130/148/148 EL, low/medium/high roof), ProMaster (136/159/159 EXT), 1-ton crew-cab pickup + slide-in camper, Type A cutaway skoolie, and 4x4 cab-over box truck, each with wheelbase, roof-height and paint options.
- **View modes** — one-tap Exterior, Cutaway (auto-opens the wall facing you), X-Ray and Interior views, plus fine-tune Solid / X-ray / Off controls per layer.
- **Inspection tools** — part isolation (hide, swap variant, change material, remove), an exploded-view slider, a floor grid, vehicle dimension lines, and live length / width / height callouts on any selected part (inches and centimeters).
- **Part search & custom parts** — search by brand, model or spec to find the closest catalog module; in the Android app, Search Online pulls live web results and pre-fills size, weight and price; add any custom part with its own specs and placement.
- **Camera presets** — Exterior 3/4, Rear Doors Open, Side Door Open, Top-Down Floorplan, and Driver Cab View on hotkeys `1`–`5`, with animated doors.
- **Modular catalog (45+ parts)** — sleeping & seating, kitchen & galley, bathroom & hygiene, off-grid power, water & climate, and exterior/overland gear. Modules snap to zones and swap when a zone is occupied.
- **Materials & finishes** — procedural cabinetry, countertop, wall/ceiling and flooring finishes, applied build-wide or per part.
- **Live build tracker** — itemized bill of materials and cost by phase, payload vs. GVWR, front/rear and left/right weight distribution, solar + alternator harvest vs. appliance draw with days of battery autonomy, fresh/grey water capacity, and engineering checks.
- **Phased build mode** — step through Phase 1 Insulation & Framing → 2 Electrical & Plumbing → 3 Cabinetry & Finish → 4 Exterior Gear.
- **Save / load** — multiple builds in browser storage, JSON import/export, and CSV bill-of-materials export.

## Install on Android

1. Open the [latest release](../../releases/latest) on your phone and download **`NomadForge-3D-vX.Y.Z.apk`** under *Assets*.
2. Open the downloaded file. If Android asks, allow your browser to **install unknown apps**.
3. Tap **Install**. The app works offline once installed (the 3D engine is bundled).

To update, use **Settings → Check for Update** in the app, download the newer APK and install it over the old one — your saved builds are kept.

## Run it in a browser

Open `index.html` in any modern browser (it needs an internet connection to load Three.js and fonts from the CDN).

## How releases are built

Adding a new `## vX.Y.Z` entry to the top of `CHANGELOG.md` on `main` triggers `.github/workflows/release.yml`, which publishes a GitHub release with those notes and builds a signed Android APK (Capacitor WebView wrapper with Three.js bundled for offline use) and attaches it to the release.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `1`–`5` | Camera presets |
| `x` | Toggle body X-ray |
| `g` | Toggle floor grid |
| `d` | Toggle dimensions |
| `h` | Hide selected part |
| `Delete` | Remove selected part |
| `Esc` | Deselect / close dialog |

## Updates

The app's **Settings → About** panel shows the current version and the latest changes, and its **Check for Update** button opens this repository's [latest release](../../releases/latest). See [CHANGELOG.md](CHANGELOG.md) for history.

## Notes

Vehicle dimensions, weights, and appliance power draws are typical published figures for planning purposes — always confirm against your own vehicle's door-jamb sticker and component spec sheets.
