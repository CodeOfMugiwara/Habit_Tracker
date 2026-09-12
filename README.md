# Habit & Mood Tracker

A clean, minimal habit and mood tracker for September 2026 (auto-detects current month). Built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies.

## Features

- **Habit Tracker** — Track 14 daily habits with ✓/~/✗ status cycling (click to toggle)
- **Mood Tracker** — Log your mood each day from 6 levels
- **Notes** — Add a note for any day via the 📝 icon
- **Dashboard** — View today's stats, habits, mood, and notes at a glance
- **History** — Browse any past month with month + year selectors
- **Dark Mode** — Toggle in the sidebar, preference saved
- **Customizable** — Edit habit names, add/remove/reorder habits, edit mood levels, change tracker title
- **Drag & Drop** — Reorder habits and moods via drag handles in Setup
- **Auto Month** — Automatically detects current month, highlights today
- **Data Persistence** — All data saved to localStorage, survives refresh
- **Month Archiving** — Past months are preserved and accessible in History

## Pages

| Page | Description |
|------|-------------|
| **Tracker** | Main habit grid + mood grid + notes |
| **Dashboard** | Today's overview with stats |
| **History** | Browse any saved month |
| **Setup** | Customize title, habits, moods |

## Tech Stack

- HTML5
- CSS3 (custom properties, grid, flexbox)
- Vanilla JavaScript (no build step)
- localStorage for persistence

## Usage

Open `index.html` in any modern browser. No server required.

## Data Structure

All data is stored in localStorage under the key `progress_tracker_v1`:

```json
{
  "allData": {
    "2026-09": {
      "habits": { "0_12": "done", "1_12": "missed" },
      "mood": { "12": 5 },
      "notes": { "12": "Had a great day" }
    }
  },
  "config": {
    "title": "Being New Version of Me Challenge",
    "habits": ["Wake up before 6:00 AM", ...],
    "moods": [{ "label": "Happy", "emoji": "😊", "color": "#66bb6a", "value": 5 }]
  },
  "darkMode": false
}
```
