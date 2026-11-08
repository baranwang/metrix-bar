# Metrix.Bar Dashboards

Custom [Metrix.Bar](https://metrix.bar/) native menu bar and system tray dashboards.

## Dashboards

| Dashboard | Directory | Description |
| :--- | :--- | :--- |
| **[Komari](./komari)** | `komari/komari.bar` | Multi-server status, real-time bandwidth, traffic quota, and historical load & ping trends for [Komari](https://komari-document.pages.dev/). |
| **[Tokens](./tokens)** | `tokens/tokens.bar` | AI coding token usage, daily spend, 53-week activity heatmap, model breakdown, and multi-device submissions for [Tokens](https://tokens.ci/). |

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
metrixbar://install?url=https%3A%2F%2Fraw.githubusercontent.com%2Fbaranwang%2Fmetrix-bar%2Fmain%2Fkomari%2Fkomari.bar&sha256=b2f3ef640a1c35b6a322178423c8f03c19d4f1bb98e07fb5dfb3c3457b9fcf18
```

Import `tokens.bar` directly:

```text
metrixbar://install?url=https%3A%2F%2Fraw.githubusercontent.com%2Fbaranwang%2Fmetrix-bar%2Fmain%2Ftokens%2Ftokens.bar&sha256=bcc9c9b05b7c3e762fd5684554b6a0db7e7edd9bbe706f78a725fd4ca22da4d9
```
