# APIX — Local-First Multi-Protocol API Workstation

> High-performance, local-first API client, programmable mock server, and load runner built with a Rust core engine and Tauri v2.

- **Web App & Docs:** https://postman.tamiz.pro
- **Desktop Installers:** https://github.com/tamiz-uddin/apix/releases (macOS `.dmg`, Windows `.msi` / `.exe`, Linux `.AppImage` / `.deb` / `.rpm`)
- **Bug Reports & Feature Requests:** [GitHub Issues](https://github.com/tamiz-uddin/apix/issues)

---

## What Is This Repository?

This is the official **public releases & community issue tracker** for **APIX**.

APIX's source code is kept private. This repository hosts:
- Official signed/packaged desktop installers and release notes
- Community bug reports and feature requests
- Licensing terms ([LICENSE](LICENSE))

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
