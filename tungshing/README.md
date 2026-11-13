# 黄历 (Tungshing) for Metrix.Bar

Chinese almanac dashboard (`.bar` protocol v0, `v1.0.0`) for [Metrix.Bar](https://metrix.bar/), calculated locally with [tyme4ts](https://github.com/6tail/tyme4ts) `1.5.6`.

## Features

- **Menu Bar**: A stylized moon-phase icon based on the lunar day, with either the full lunar date (`十月初五`) or just the day (`初五`).
- **Daily Almanac**: Lunar and Gregorian dates, weekday, stem-branch dates, festivals, solar terms, and recommended and avoided activities.
- **Expandable Details**: 纳音, 冲煞, 值神, 建除, 星宿, 胎神, 吉神宜趋, 凶神宜忌, and 彭祖百忌.
- **Hourly Almanac**: Thirteen time slots with hourly activities, auspiciousness, and deity directions. The split midnight periods are labeled `子正` (`00:00–01:00`) and `子初` (`23:00–24:00`).
- **Date Navigation**: Previous/next day, calendar picker, return to today, and automatic highlighting of the current time slot.
- **Appearance**: A scrollable 480 × 720 panel with light/dark themes and Chinese serif typography.

## Installation

Add the registry from the [repository installation instructions](../README.md#installation), then install **黄历**.

Alternatively, open:

```text
metrixbar://install?url=https%3A%2F%2Fraw.githubusercontent.com%2Fbaranwang%2Fmetrix-bar%2Fmain%2Ftungshing%2Ftungshing.bar&sha256=d143b12970c3df03b1e71f123cf64f7cc0c06879464aa0cd22d14c71840d5fd9
```

## Configuration

| Input | Type | Default | Options |
| :--- | :--- | :--- | :--- |
| `trayFormat` | `select` | `month-day` | `month-day`: lunar month and day (`十月初五`); `day`: lunar day only (`初五`). |

No account or API key is required. The first load requires access to `https://esm.sh` to download the calendar library. Dates and the current time slot follow the computer's system time zone; the dashboard refreshes once a minute.

The menu bar always shows today, even when browsing another date in the panel. Its moon phases are symbolic illustrations based on the lunar day.

System widgets are not included. Verified with Metrix.Bar 0.2.4 on macOS.

## SHA-256

```text
d143b12970c3df03b1e71f123cf64f7cc0c06879464aa0cd22d14c71840d5fd9
```
