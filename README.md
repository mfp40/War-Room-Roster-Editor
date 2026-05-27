# War Room Roster Editor

A fast, dark-themed spreadsheet editor for War Room Football roster JSON files. Built for the War Room community — no installs, no dependencies, no server. Just open the HTML file in your browser.

![War Room Roster Editor](https://img.shields.io/badge/War%20Room-Roster%20Editor-4f8ef7?style=flat-square&labelColor=0d0f12)
![Zero Dependencies](https://img.shields.io/badge/dependencies-none-3ecf8e?style=flat-square&labelColor=0d0f12)
![Single File](https://img.shields.io/badge/single-file-f5a623?style=flat-square&labelColor=0d0f12)

---

## Quick Start

1. Download `roster_editor.html`
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari)
3. Click **⬆ Import JSON** and load your roster file
4. Edit, save, and export

That's it. No Node, no Python, no build step.

---

## Features

### Spreadsheet Grid
- **All players** visible in a scrollable, sortable table
- **Click any column header** to sort ascending or descending
- **Color-coded attribute chips** — elite (yellow-green), good (blue), average (amber), poor (red) — applied consistently across OVR and all attributes

### Inline Editing — edit directly in the grid without opening the side panel
| Column | How to edit |
|---|---|
| **OVR** | Double-click → type or use ↑/↓ keys |
| **Age** | Double-click → type or use ↑/↓ keys |
| **Ht** | Double-click → type or use ↑/↓ keys |
| **Wt** | Double-click → type or use ↑/↓ keys |
| **Exp** | Double-click → type or use ↑/↓ keys |
| **Dev Trait** | Single click → dropdown |
| **Personality** | Single click → dropdown |
| **Team** | Single click → dropdown (all 32 teams + FA) |
| **Attribute chips** | Double-click → type or use ↑/↓ keys |

Press **Enter** or click away to commit. Press **Escape** to cancel.

### Position-Aware Attribute Columns
- **No position filter** → 9 universal columns (Speed, Accel, Agility, Strength, Stamina, Aware, Clutch, Consist, Durable)
- **Filter by position** → full position-specific attribute set with labeled group headers (e.g. QB shows Passing / IQ / Mobility / Physical)

### Filtering & Search
- **Search bar** — filter by player name or team, with one-click **×** to clear
- **Team filter** — all 32 teams + FA
- **Position filter** — all positions, also controls which attribute columns are shown
- **Dev Trait filter** — XFactor, Superstar, Normal, Declining
- **Personality filter** — all 21 personality labels, plus "Not Set" to find unassigned players

### Side Panel
Full player detail editor — opens when you click any row. Fields include:
- **Identity**: First/Last name, college, team, position, demographic
- **Core**: Overall, age, experience, height, weight, dev trait, potential
- **Draft**: Draft round and pick
- **Contract**: Annual salary, years, signing bonus
- **Personality**: Label dropdown (21 options) + 7 hidden trait sliders (Work Ethic, Competitiveness, Composure, Leadership, Loyalty, Temperament, Ego) each on a 1–20 scale
- **Attributes**: All position-specific attributes with 40–99 range inputs

Inline grid edits sync to the panel in real time if that player is open.

### Personality System
Personality labels are color-coded by archetype:
- 🟢 **Positive** (green) — FranchiseCornerstone, TeamCaptain, ModelProfessional, QuietLeader, LockerRoomGuy, SteadyVeteran
- 🔵 **Competitive Edge** (teal) — Grinder, Competitor, ClutchPerformer, SilentAssassin, Perfectionist, Sparkplug
- ⚪ **Neutral** (gray) — FanFavorite, Professional, LaidBack
- 🔴 **Problem** (red) — Mercenary, Showboat, Hothead, Diva, Unmotivated, HeadCase

The hidden personality traits (1–20) drive development rate, contract negotiations, and locker-room dynamics in-game. The label drives trade-demand multipliers. They can be set independently.

### File Operations
| Button | What it does |
|---|---|
| **⬆ Import JSON** | Load any War Room roster `.json` file |
| **💾 Save** | Commits all changes to the in-memory session (clears the unsaved indicator). Use this as a checkpoint. |
| **⬇ Export JSON** | Downloads the edited roster as `Claude_Roster_Edited.json` |

> **Note:** Because this is a local browser app, "Save" commits to your session's working copy. "Export" is how you get the file back to disk. Always export before closing your browser tab.

---

## Roster Format

The editor works with the `war-room-roster` JSON format. A minimal valid player entry requires only:

```json
{
  "firstName": "Patrick",
  "lastName": "Mahomes",
  "position": "QB",
  "age": 29,
  "overall": 97,
  "team": "KC"
}
```

Valid teams: `BAL PIT CLE CIN TEN IND HOU JAX NE NYJ BUF MIA KC LV DEN LAC MIN CHI GB DET NO CAR ATL TB DAL PHI NYG WAS SF SEA LAR ARI FA`

Valid positions: `QB RB WR TE LT LG C RG RT DE DT ILB OLB CB S K P`

Free agents use `"team": "FA"` — they go into the league pool and don't count toward any team's 53-man roster.

---

## Attribute Value Reference

| Range | Tier | Color |
|---|---|---|
| 90–99 | All-Pro / Elite | 🟡 Yellow-green |
| 75–89 | Pro Bowl / Good | 🔵 Blue |
| 60–74 | Starter / Average | 🟠 Amber |
| 40–59 | Backup / Poor | 🔴 Red |

OVR tiers follow the same scale: a 90+ OVR is an All-Pro candidate; 80–84 is a reliable high-end starter; 75–79 is a solid starter.

---

## Browser Compatibility

| Browser | Status |
|---|---|
| Chrome 90+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |

---

## Contributing

Pull requests welcome. If you find a bug or want to request a feature, open an issue. Please keep the zero-dependency, single-file philosophy — the whole point is that anyone in the community can just download one file and go.

---

## License

MIT — see `LICENSE` for details.
