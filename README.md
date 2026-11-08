# Metrix.Bar Dashboards

Custom [Metrix.Bar](https://metrix.bar/) native menu bar and system tray dashboards.

## Dashboards

| Dashboard | Directory | Description |
| :--- | :--- | :--- |
| **[Komari](./komari)** | `komari/komari.bar` | Multi-server status, real-time bandwidth, traffic quota, and historical load & ping trends for [Komari](https://komari-document.pages.dev/). |

## Installation

### Option 1: Add Registry in Metrix.Bar

Add the following Registry URL in **Metrix.Bar → Settings → Registries**:

```text
https://raw.githubusercontent.com/baranwang/metrix-bar/main/index.json
```

Or open via URI scheme:

```text
metrixbar://registry/add?url=https%3A%2F%2Fraw.githubusercontent.com%2Fbaranwang%2Fmetrix-bar%2Fmain%2Findex.json
```

### Option 2: Direct Import

Import `komari.bar` directly:

```text
metrixbar://install?url=https%3A%2F%2Fraw.githubusercontent.com%2Fbaranwang%2Fmetrix-bar%2Fmain%2Fkomari%2Fkomari.bar&sha256=f41ea313d02c5d686f4a391f17d56c1dc08f281cc4302c4cddbf6a5fce3b2fd7
```
