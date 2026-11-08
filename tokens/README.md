# Tokens Dashboard for Metrix.Bar

AI coding token usage and spend dashboard (`.bar` v0) for [Tokens (`tokens.ci`)](https://tokens.ci/).

## Features

- **Zero-Config CLI Detection**: Automatically reads `~/.config/tokens/credentials.json` (created by `tokens login`) to detect your GitHub username and personal API token (`tt_…`). Also supports viewing any public profile by username or unlocking private profiles with a Read Token (`tkr_…`).
- **Menu Bar / System Tray**: Monochrome template Tokens mark with configurable tray display (`Today Tokens · Today Cost` by default, `Today Tokens · Rank`, `Total Tokens · Rank`, `Total Tokens · Total Cost`, `Today Tokens Only`, or `Today Cost Only`).
- **Today Hero Overview**:
  - Live daily token total, today's leaderboard rank badge (`#N today`), daily spend, and message count.
  - 5-category `TOKEN BREAKDOWN` bar and list (`Input`, `Output`, `Cache Read`, `Cache Write`, `Reasoning`).
  - Collapsible `CLIENTS & MODELS` breakdown with client logos (`https://tokens.ci/clients/client-*`), model brand icons, per-model token/message stats, and `Fast` / `Standard` speed pills.
- **Usage Detail (`All Time` / `30 Days` / `7 Days`)**:
  - 2×2 summary grid (`Total Tokens`, `Est. Cost`, `Active Days`, `Submissions`).
  - `Token Breakdown` card with proportional bar and 5-row vertical breakdown.
  - `Daily Trend` area chart with `Tokens | Cost ($)` toggle.
  - Horizontally scrollable 53-week `Activity` contribution heatmap anchored to the latest week, with P92 token intensity grading and click-to-inspect daily breakdowns.
  - `Active Clients` pill strip, `Models` ranking card (`Tokens | Cost` toggle + `Show All N` expansion), and `Devices` card with automatic cloud session grouping (`Claude Code cloud` etc.), unmasked local device names, and single-device drill-down view.

## Inputs

| Input | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `username` | `string` | No | Optional when logged in with `tokens login`. Enter any GitHub username to view a public profile. |
| `token` | `secret` | No | Optional Read Token (`tkr_…`) for private profiles or API Token (`tt_…`) for unmasked device names. |
| `trayFormat` | `select` | No | Menu bar display format (default: `Today Tokens + Today Cost`). |
| `baseURL` | `string` | Yes | Base URL of the Tokens server (default: `https://tokens.ci`). |
| `credentials` | `file` | No | Path to CLI credentials file (default: `~/.config/tokens/credentials.json`). |

## SHA-256

```text
bcc9c9b05b7c3e762fd5684554b6a0db7e7edd9bbe706f78a725fd4ca22da4d9
```
