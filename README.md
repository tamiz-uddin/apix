# APIX — Local-First Multi-Protocol API Workstation

> High-performance, local-first API client, programmable mock server, and load runner built with a Rust core engine and Tauri v2.

- **Web App & Docs:** https://postman.tamiz.pro
- **Latest Installers:** https://github.com/tamiz-uddin/apix/releases/latest
- **Bug Reports & Feature Requests:** [GitHub Issues](https://github.com/tamiz-uddin/apix/issues)

---

## Downloads (Latest Release)

| Platform | Package | Architecture | Download |
| :--- | :--- | :--- | :--- |
| **Windows** | `*-setup.exe` (NSIS) | x64 (64-bit) | [Latest Release](https://github.com/tamiz-uddin/apix/releases/latest) |
| **Linux (Portable)** | `.AppImage` | x86_64 | [Latest Release](https://github.com/tamiz-uddin/apix/releases/latest) |
| **Linux (Debian / Ubuntu)** | `.deb` | amd64 | [Latest Release](https://github.com/tamiz-uddin/apix/releases/latest) |
| **Linux (Fedora / RHEL / openSUSE)** | `.rpm` | x86_64 | [Latest Release](https://github.com/tamiz-uddin/apix/releases/latest) |
| **macOS** | `.dmg` | Apple Silicon / Intel | [Latest Release](https://github.com/tamiz-uddin/apix/releases/latest) |

---

## Platform Installation Guide

<details open>
<summary><strong>Linux (AppImage, Debian/Ubuntu .deb, Fedora/RHEL .rpm)</strong></summary>

**System Requirements:** 64-bit x86_64 Linux with WebKit2GTK 4.1 (Ubuntu 22.04+, Fedora, Arch/Garuda, Debian 12+).

### 1. Portable AppImage (All Distros — Arch, Garuda, Manjaro, Ubuntu, Fedora)
1. Download `apix_*_amd64.AppImage` from [Releases](https://github.com/tamiz-uddin/apix/releases/latest).
2. Make it executable and run:
```bash
chmod +x apix_*_amd64.AppImage
./apix_*_amd64.AppImage
```
> **Note:** If FUSE is not installed on Ubuntu 22.04+, install `libfuse2` or run `./apix_*_amd64.AppImage --appimage-extract-and-run`.

### 2. Ubuntu / Debian / Linux Mint / Pop!_OS (`.deb`)
```bash
sudo apt update
sudo apt install ./apix_*_amd64.deb
```

### 3. Fedora / RHEL / openSUSE (`.rpm`)
```bash
# Fedora / RHEL
sudo dnf install ./apix-*.x86_64.rpm

# openSUSE
sudo zypper install ./apix-*.x86_64.rpm
```

**Uninstall:**
- Debian/Ubuntu: `sudo apt remove apix`
- Fedora: `sudo dnf remove apix`
- AppImage: delete the `.AppImage` file

</details>

<details>
<summary><strong>Windows (64-bit NSIS Installer)</strong></summary>

**System Requirements:** Windows 10 or Windows 11 (64-bit) with Microsoft Edge WebView2 (auto-installed if missing).

### 1. Standard Setup Wizard (Recommended)
1. Download `apix_*_x64-setup.exe` from [Releases](https://github.com/tamiz-uddin/apix/releases/latest).
2. Double-click the executable to install for the current user (no administrator rights required).
3. If Windows SmartScreen displays a prompt, click **More info** -> **Run anyway**.
4. Launch **APIX** from the Start Menu or Desktop shortcut.

### 2. Silent / Unattended Install (PowerShell)
```powershell
.\apix_0.1.0_x64-setup.exe /S
```

**Uninstall:**
Open **Windows Settings -> Apps -> Installed Apps -> APIX -> Uninstall**.

</details>

<details>
<summary><strong>macOS (Apple Silicon & Intel .dmg)</strong></summary>

**System Requirements:** macOS 12 Monterey or newer (Apple Silicon M1–M4 or Intel x64).

### 1. Install from Disk Image
1. Download the `.dmg` matching your Mac architecture from [Releases](https://github.com/tamiz-uddin/apix/releases/latest).
2. Double-click the `.dmg` file to mount it.
3. Drag **APIX.app** into your **Applications** folder and eject the disk image.

### 2. First Launch (Gatekeeper Notice)
If macOS reports the app is from an unidentified developer, right-click **APIX.app** -> **Open** -> **Open**, or run:
```bash
xattr -cr /Applications/APIX.app
open /Applications/APIX.app
```

**Uninstall:**
Drag **APIX.app** from `/Applications` to Trash.

</details>

---

## Core Capabilities

- **6 Native Protocols:** HTTP/1.1 & HTTP/2, GraphQL (with schema introspection), WebSocket, Server-Sent Events (SSE), MQTT (QoS 0/1/2), and gRPC Unary (runtime `.proto` compilation).
- **Zero UI Thread Blocking:** All networking, 4-tier environment resolution (`PersonalLocalOverride > SharedTeam > Collection > Global`), cookie management, and payload streaming run inside the Rust core engine.
- **Tri-Mode Collaboration:** Solo Local (SQLite WAL + `.request.yaml`), Git-Native Team (deterministic YAML/JSON), and Real-Time Cloud Workspaces with RBAC (`Owner`, `Admin`, `Editor`, `Viewer`).
- **Testing, Mocking & Load Benchmarking:** Sandboxed `rquickjs` (`pm.*`) pre/post scripting, data-driven Collection Runner, Tokio Load/Stress Runner (`p50`/`p90`/`p95`/`p99`), and Mock Server with latency & fault injection.

---

## Licence

Copyright (c) 2026 [Tamiz Uddin](http://tamiz.pro/). All rights reserved.

APIX is **proprietary freeware**. Anyone may download, install, and use it free of charge for personal, educational, or commercial work. It is **not** open source: copying, modifying, redistributing, or reselling the software or its source code requires written permission. See [LICENSE](LICENSE) for full terms.
