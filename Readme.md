# HLstatsX:CE 2.0.0

**A modern, resilient evolution of HLstatsX:CE 1.6.19 — built for Source 2, CS2, and the future of competitive multiplayer.**

HLstatsX:CE 2.0.0 is a full-scale rework of the classic real-time stats and ranking system for `srcds`-based games. Designed to thrive in both legacy Source 1 environments and modern CS2 servers, this fork introduces asynchronous RCON, hybrid log ingestion (UDP + HTTP), competitive mode awareness, and a scalable, restart-safe architecture.

Whether you're running a community server or a high-performance competitive hub, HLstatsX:CE 2.0.0 delivers unmatched reliability, flexibility, and insight.

---

## 🚀 Key Features

### 🌐 Hybrid Log Ingestion (UDP + HTTP)
- Unified listener for both legacy `srcds` UDP logs and CS2’s HTTP-based log stream — **on the same port**
- Powered by `Mojo::IOLoop` for non-blocking, event-driven performance
- Automatic log format detection and normalization
- Mojo::IOLoop powers the listener, so UDP and HTTP log handling is non-blocking.
- Multiple servers can stream logs concurrently without blocking each other.
- Packet parsing is modular and event-driven — no global locks or serialized queues.

### 🧠 Intelligent Packet Parsing
- Modular parser system handles mixed log formats with precision
- Per-server context tracking: map, hostname, difficulty, player state
- Engine-aware dispatching for Source 1 and Source 2 events

### 🔌 Plugin Compatibility
- **Source 1**: Fully supports legacy `hlstatsx.smx` Sourcemod plugin
- **CS2 / Source 2**: Compatible with HLstatsZ plugin for CounterStrikeSharp
  - Emulates Sourcemod-style events (`hlx_sm_*`)
  - Server mod set as `SOURCEMOD` for seamless integration

### 🛠️ Server-Specific Overrides
- Per-server config for:
  - Custom commands
  - Stat weighting and modifiers
  - Competitive mode toggles

### 📈 Web Frontend Options
- Compatible with:
  - Legacy HLstatsX PHP frontend
  - 🌠 HLstatsZ Next-Gen frontend:
    - AJAX-first, profile-centric UI
    - DataTables for sorting/filtering
    - OpenStreetMap for geo IP views
    - ApexCharts for sleek live graphs
    - Built-in caching and query optimization
    - ⚠️ Admin panel not yet implemented — use legacy frontend for setup

---

## 💡 Why HLstatsX:CE 2.0.0?

- **Battle-tested**: Proven across thousands of servers and millions of player sessions
- **Zero client-side footprint**: No in-game installs required
- **External server support**: Offload processing for zero impact on game performance
- **Fully async**: RCON, log ingestion, and DB operations are non-blocking and restart-safe
- **Built for CS2**: Competitive mode, Source 2 quirks, and HTTP logging all handled natively

---

## 📦 Installation & Setup

...

---

## 🤝 Credits

Based on HLstatsX:CE 1.6.19  
Maintained and modernized by the community for CS2 and beyond.

