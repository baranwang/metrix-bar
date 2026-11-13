# Tokens Dashboard for Metrix.Bar

AI coding token usage, spend, desktop widgets, and shareable daily statement receipt dashboard (`.bar` v0, `v1.2.1`) for [Tokens (`tokens.ci`)](https://tokens.ci/).

## Features

- **Zero-Config CLI Detection**: Automatically reads `~/.config/tokens/credentials.json` (created by `tokens login`) to detect your GitHub username and personal API token (`tt_…`). Also supports viewing any public profile by username or unlocking private profiles with a Read Token (`tkr_…`).
- **Private Account Connection**: Click **Connect Private Account** to create and securely save a Read Token using your existing CLI login or personal API token. Restores client and model details, preserves existing credentials, and reuses the Read Token after refresh or restart.
- **Menu Bar / System Tray**: Monochrome template Tokens mark with configurable tray display (`Today Tokens · Today Cost` by default, `Today Tokens · Rank`, `Total Tokens · Rank`, `Total Tokens · Total Cost`, `Today Tokens Only`, or `Today Cost Only`).
- **Desktop Widgets**:
  - Small: today's token total, estimated cost, and leaderboard rank.
  - Medium: today's overview and message count alongside a 7-day token trend.
  - Large: today's overview, a 30-day token trend, and the three clients with the most tokens today.
  - Native light/dark appearance, shared account and data cache, and calendar-aligned trends with missing dates filled with zero. Widget summaries always show today, independently of the panel's selected period or receipt date.
- **Daily AI Statement Receipt (`🧾 Statement`)**:
  - Shareable thermal-paper receipt view (`DAILY AI STATEMENT`) with torn-tooth bottom edge and monochrome ink client/model logos.
  - Shows daily API-equivalent spend, active streak (`STREAK`), message count, comparison against prior average active day (`VS AVERAGE DAY`), per-client/model cost breakdown, and `CACHE HIT RATE`.
  - 4 curated editorial OKLab backdrops (`Sage`, `Terracotta`, `Nordic`, `Charcoal`), date stepper (`‹ Date ›`), one-click headerless 2× PNG copy to clipboard, and PNG file export.
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

## Private Account Setup

If your private account only shows aggregate usage and device stats, sign in with `tokens login` (or enter your personal API token in **Read or API Token**), then click **Connect Private Account** in the dashboard. The dashboard verifies that the token belongs to the selected account, creates a Read Token, saves it in Metrix.Bar's secret storage, and reloads client and model details.

Connecting enables Private Mode on the Tokens account; it never makes the profile public. Tokens are only created after you click the button, never during polling or preflight. Your CLI credentials file and existing API token are preserved. Subsequent refreshes and restarts reuse the saved Read Token. Connection and persistence have been verified with Metrix.Bar 0.2.3.

You can also paste an existing `tkr_…` token into **Private Read Token**. Legacy Read Tokens entered in **Read or API Token** continue to work; **Private Read Token** takes priority when both are set.

## Desktop Widget Setup

Widget support requires Metrix.Bar 0.2.0 or newer and a supported system widget container. On macOS 14 or newer, open **Edit Widgets**, add a small, medium, or large **Metrix.Bar** widget, and select **Tokens**. Windows 11 22H2 or newer uses the Widgets board with the Metrix.Bar companion provider; KDE Plasma 6 uses the companion plasmoid.

Widgets share the dashboard's existing five-minute data polling. The system controls visible refresh timing; clicking a widget opens Tokens. If a refresh fails, the last available values remain visible. After Metrix.Bar exits, widgets show cached content.

## Changes in v1.2.1

- Fix missing client and model details for private accounts with a one-click connection using the existing CLI login or personal API token.
- Securely persist the Read Token separately from existing credentials and reuse it after restart. Retry failed storage without issuing another token.
- Verify account ownership before connecting, block duplicate requests, and reload full details even when a refresh is already running.

## Changes in v1.2.0

- Add small, medium, and large native widget summaries.
- Handle setup, loading, unavailable accounts, missing client details, and cached data in widget output.
- Use explicit avatar dimensions for compatibility with the current Metrix.Bar renderer.

## Inputs

| Input | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `username` | `string` | No | Optional when logged in with `tokens login`. Enter any GitHub username to view a public profile. |
| `token` | `secret` | No | Optional Read Token (`tkr_…`) for private profiles or API Token (`tt_…`) for unmasked device names. |
| `readToken` | `secret` | No | Read Token saved automatically by **Connect Private Account**, or entered manually. Takes priority over a Read Token in `token`. |
| `trayFormat` | `select` | No | Menu bar display format (default: `Today Tokens + Today Cost`). |
| `baseURL` | `string` | Yes | Base URL of the Tokens server (default: `https://tokens.ci`). |
| `credentials` | `file` | No | Path to CLI credentials file (default: `~/.config/tokens/credentials.json`). |

## SHA-256

```text
253bac972d1698ce096fb477f42be6b92dbd50cfe8da66969ccea2ee0e433942
```
