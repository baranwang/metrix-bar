# Komari Dashboard for Metrix.Bar

Multi-server monitoring dashboard (`.bar` v0) for [Komari](https://komari-document.pages.dev/).

## Features

- **Menu Bar / System Tray**: Monochrome adaptive Komari icon (`match-media` aware) with configurable tray metrics (`Online/Total · Total Bandwidth`, `Total Bandwidth`, `↑Up ↓Down`, or `Online/Total`).
- **Cluster Overview**: 3-card header showing Online Nodes (with 10-segment status bar), Live Bandwidth, and Total Traffic.
- **Server Cards**:
  - 2×2 hardware grid (`CPU`, `Memory`, `Disk`, `Load`) with 14-segment capsule bars.
  - Live upload (`↑` Blue) and download (`↓` Green) rates with a 60-slot bidirectional mirrored wave sparkline and cumulative outbound/inbound traffic.
  - Remaining traffic quota bar (24-segment capsule bar).
  - 3-column live Ping latency & packet loss strip (`ms` + `%`).
  - Uptime days, expiration countdown, TCP/UDP connections, and billing cycle price pill.
- **Single-Server Detail View**:
  - Single-layer collapsible node info card with `System / Resources / Network` tabs.
  - `Load | Ping` view switcher and `Live | 1H | 4H | 1D` time range selector.
  - 6 independent metric area charts (`CPU`, `Memory + Swap`, `Disk`, `Network`, `Connections`, `Processes`) and multi-target `Ping` latency chart with interactive line toggles.
- **Automatic Localization**: Automatically follows system `zh` / `en` locale (with Chinese fallback).

## Inputs

| Input | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `baseURL` | `string` | Yes | Base URL of your Komari server (e.g. `https://status.example.com`). |
| `apiKey` | `secret` | No | Optional Bearer API key for private sites (`private_site`) or viewing hidden nodes. |
| `refreshInterval` | `select` | No | Polling interval: `2s`, `5s` (default), `10s`, `30s`, `60s`. |
| `trayFormat` | `select` | No | Menu bar display format (default: `10/10 · 1.1M/s`). |
| `offlineNotify` | `bool` | No | Desktop notification when an online node goes offline (default: `true`). |

## SHA-256

```text
b2f3ef640a1c35b6a322178423c8f03c19d4f1bb98e07fb5dfb3c3457b9fcf18
```
