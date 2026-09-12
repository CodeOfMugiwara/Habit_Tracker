# Habit Tracker — Lavender Sky

A beautiful, minimal habit and mood tracker with the Lavender Sky color palette. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies.

## Features

- **Home Dashboard** — Greeting, day streak, today's habits with circle progress, weekly stats
- **Habit Tracker** — Track daily habits with emoji icons and ✓/~/✗ status cycling
- **Mood Tracker** — Log moods with emoji grid, interactive SVG line graph, and mood insights
- **Stats** — Completion rates with progress bars for each habit
- **Calendar** — Monthly grid with mood emojis and notes
- **Settings** — Edit title, name, habits (emoji + name), moods (emoji + name + color), drag to reorder
- **Dark Mode** — Lavender Sky dark palette toggle in sidebar
- **Graph Hover** — Toggle tooltip on graph hover in sidebar
- **Notes** — Click any calendar day to add a note
- **Data Persistence** — All data saved to localStorage, survives refresh
- **Month Archiving** — Past months preserved and browsable

## Pages

| Page | Description |
|------|-------------|
| **Home** | Greeting, streak, today's habits, weekly progress |
| **Habits** | Full month habit grid with date navigation |
| **Mood** | Mood grid, interactive SVG graph, insights |
| **Stats** | Completion rates with progress bars |
| **Calendar** | Monthly overview with mood emojis and notes |
| **Settings** | Customize everything |

## Color Palette

### Light Mode (Lavender Sky)
| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#F9F7FD` | Page background |
| Surface | `#FFFFFF` | Cards |
| Surface Alt | `#EEEBF7` | Alternating surfaces |
| Primary | `#A78BFA` | Accent, buttons |
| Primary Light | `#DCC3F3` | Hover states |
| Secondary | `#C4B5FD` | Secondary accent |
| Accent | `#F0E7FF` | Backgrounds |
| Success | `#86D6BF` | Done/complete |
| Warning | `#FC5A5A` | Errors, missed |
| Info | `#FCD34D` | Partial, alerts |

### Dark Mode
| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#181726` | Page background |
| Surface | `#232038` | Cards |
| Surface Alt | `#2D2947` | Alternating surfaces |
| Primary | `#A78BFA` | Accent, buttons |
| Success | `#34D399` | Done/complete |
| Warning | `#FBBF24` | Partial |
| Text | `#E5E7EB` | Primary text |

## Tech Stack

- HTML5
- CSS3 (custom properties, grid, flexbox)
- Vanilla JavaScript (no build step)
- localStorage for persistence

## Usage

Open `index.html` in any modern browser. No server required.

## Data Structure

All data is stored in localStorage under the key `lavender_tracker_v2`:

```json
{
  "data": {
    "2026-09": {
      "habits": { "0_12": "d", "1_12": "m" },
      "mood": { "12": 5 },
      "notes": { "12": "Had a great day" }
    }
  },
  "cfg": {
    "t": "Being New Version of Me Challenge",
    "n": "Krishna",
    "h": [{ "name": "Drink Water", "emoji": "💧" }],
    "m": [{ "label": "Very Happy", "emoji": "😊", "color": "#34D399", "value": 5 }]
  },
  "dark": false,
  "gh": true
}
```
