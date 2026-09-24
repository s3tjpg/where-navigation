# 🚗 Where Navigation & Radar — BeamMP Edition

[![BeamNG.drive](https://img.shields.io/badge/BeamNG.drive-v0.33+-orange.svg)](https://beamng.com)
[![BeamMP](https://img.shields.io/badge/BeamMP-Multiplayer-blue.svg)](https://beammp.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A navigation companion, speed camera radar, and multiplayer synchronization mod built natively for **BeamNG.drive** and **BeamMP**.

---

## 📦 All-In-One Package Structure

The release is packaged as a single archive that extracts directly into your BeamMP server:

```text
Resources/
  ├── Client/
  │   └── where_navigation.zip   (Auto-downloaded by joining players)
  ├── Server/
  │   └── whereSync/
  │       ├── main.lua           (Syncs live radar, speed cameras & hazards)
  │       └── info.json
  └── README_SERVER_SETUP.txt
```

---

## ✨ Features

### 🗺️ Real-Time Vector Navigation & Radar HUD (`whereNavigation`)
* **Live Multiplayer Radar**: Displays surrounding BeamMP players as active vehicle blips with live speed readouts and compass headings.
* **Vector Cartography**: High-contrast, clean vector roads rendered dynamically with smooth turn-by-turn routing and ETA.
* **Speed Cameras & Radar Detection**: Real-time road corridor scanning for speed enforcement cameras with stroboscopic optical flash alerts when speeding.
* **Live Crowd-Sourced Hazards**: Real-time moving distance countdowns for road hazards, construction zones, police patrols, and vehicle accidents.
* **Admin Panel (Default PIN: `1111`)**:
  * Deploy speed cameras at vehicle position with custom speed limits.
  * Drop global custom Points of Interest (POIs) that sync to all players.
  * Define localized area speed limits for road zones.
  * Broadcast emergency warnings and server alerts.
  * Delete pins or export config directly to BeamMP server JSON.

### ⚡ 7-Segment Digital GPS Speedometer HUD (`whereSpeedometer`)
* **Authentic Digital LCD Display**: Crisp 7-segment digital geometry (0 italics slant, matching physical GPS hardware).
* **Color-Coded Status**: Neon green (`#00e500`) active display automatically turns bright alert red (`#ff2244`) when exceeding the active speed limit.
* **Speed Limit Presets**: Selectable caps (`OFF`, `50`, `90`, `120`, `140`) with audio-visual overspeed alert tickers.
* **Full Telemetry Box**: Live GPS signal indicator, trip odometer, trip average speed, max recorded speed, altitude (m), compass heading, and clock.

---

## 📥 Installation

### 🚀 For BeamMP Server Hosts
1. Download **[`Where_Navigation_BeamMP_Edition.zip`](https://github.com/s3tjpg/where-navigation/releases/latest/download/Where_Navigation_BeamMP_Edition.zip)** from the [Releases](https://github.com/s3tjpg/where-navigation/releases) page.
2. Extract the `Resources` folder directly into your BeamMP Server root directory (where `BeamMPServer.exe` is located).
3. Ensure server plugins are enabled in your `ServerConfig.toml`:
   ```toml
   ServerPlugins = true
   ```
4. Start your BeamMP Server! You will see:
   ```text
   === [whereSync] Where Multiplayer Sync Plugin Loaded ===
   ```

### 🎮 For Single Players / Direct Installation
1. Download **[`Where_Navigation_BeamMP_Edition.zip`](https://github.com/s3tjpg/where-navigation/releases/latest/download/Where_Navigation_BeamMP_Edition.zip)**.
2. Open the zip and take `where_navigation.zip` from inside `Resources/Client/`.
3. Drop `where_navigation.zip` into your BeamNG mods folder:
   ```text
   %LocalAppData%\BeamNG.drive\<version>\mods\
   ```

---

## 🔐 Admin Panel Access
* Tap the menu button on the navigation app, then click **Admin Panel** at the bottom (or type `/adminpanel1111` in game chat).
* **Default PIN**: `1111` *(can be customized in `settings/where_config.json`)*.

---

## 📄 License
This project is open-source under the MIT License. See [LICENSE](LICENSE) for details.
