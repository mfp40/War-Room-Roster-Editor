# War Room Roster Editor

A fast, dark-themed spreadsheet editor for War Room Football roster JSON files. Built for the War Room community — no installs, no dependencies, no server. Just open the HTML file in your browser.

![War Room Roster Editor](https://img.shields.io/badge/War%20Room-Roster%20Editor-4f8ef7?style=flat-square&labelColor=0d0f12)
![Zero Dependencies](https://img.shields.io/badge/dependencies-none-3ecf8e?style=flat-square&labelColor=0d0f12)
![Single File](https://img.shields.io/badge/single-file-f5a623?style=flat-square&labelColor=0d0f12)

---

## Quick Start

1. Download `war_room_roster_editor.html`
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari)
3. Click **⬆ Import JSON** and load your roster file
4. Edit, save, and export

That's it. No Node, no Python, no build step.

---

## Two Modes — One File

The editor has a **⚡ Players / 🎯 Coaching** toggle in the header. Each mode has its own grid, toolbar filters, and side panel. Switching modes preserves all unsaved changes in both.

---

## Players Mode

### Spreadsheet Grid
- **All players** visible in a scrollable, sortable table
- **Click any column header** to sort ascending or descending
- **Color-coded OVR and POT chips** — and all attribute chips — use consistent tier colors across the entire grid

### Inline Editing — edit directly in the grid without opening the side panel
| Column | How to edit |
|---|---|
| **OVR** | Double-click → type or use ↑/↓ keys |
| **POT** | Double-click → type or use ↑/↓ keys |
| **Age** | Double-click → type or use ↑/↓ keys |
| **Ht** | Double-click → type or use ↑/↓ keys |
| **Wt** | Double-click → type or use ↑/↓ keys |
| **Exp** | Double-click → type or use ↑/↓ keys |
| **Dev Trait** | Single click → dropdown |
| **Personality** | Single click → dropdown |
| **Team** | Single click → dropdown (all 32 teams + FA) |
| **Attribute chips** | Double-click → type or use ↑/↓ keys |

Press **Enter** or click away to commit. Press **Escape** to cancel without saving.

### Position-Aware Attribute Columns
- **No position filter** → 9 universal columns (Speed, Accel, Agility, Strength, Stamina, Aware, Clutch, Consist, Durable)
- **Filter by position** → full position-specific attribute set with labeled group headers (e.g. QB shows Passing / IQ / Mobility / Physical)

### Filtering & Search
- **Search bar** — filter by player name or team, with one-click **×** to clear
- **Team filter** — all 32 teams + FA
- **Position filter** — all positions; also controls which attribute columns are shown
- **Dev Trait filter** — XFactor, Superstar, Normal, Declining
- **Personality filter** — all 21 personality labels, plus "Not Set" to find unassigned players

### Side Panel
Full player detail editor — opens when you click any row:

| Section | Fields |
|---|---|
| **Identity** | First/Last name, college, team, position, demographic |
| **Core** | Overall, Potential, Age, Experience, Height, Weight, Dev Trait |
| **Draft** | Draft round, draft pick |
| **Contract** | Annual salary, years, signing bonus |
| **Personality** | Label dropdown (21 options) + 7 hidden trait sliders (Work Ethic, Competitiveness, Composure, Leadership, Loyalty, Temperament, Ego) each on a 1–20 scale |
| **Attributes** | All position-specific attributes, 40–99 range |

Inline grid edits sync to the open panel in real time.

### Personality System
Personality labels are color-coded by archetype:
- 🟢 **Positive** (green) — FranchiseCornerstone, TeamCaptain, ModelProfessional, QuietLeader, LockerRoomGuy, SteadyVeteran
- 🔵 **Competitive Edge** (teal) — Grinder, Competitor, ClutchPerformer, SilentAssassin, Perfectionist, Sparkplug
- ⚪ **Neutral** (gray) — FanFavorite, Professional, LaidBack
- 🔴 **Problem** (red) — Mercenary, Showboat, Hothead, Diva, Unmotivated, HeadCase

The hidden personality traits (1–20) drive development rate, contract negotiations, and locker-room dynamics in-game. The label drives trade-demand multipliers. They can be set independently.

---

## Coaching Mode

### The Coaching Grid

All three coaching roles — **HC**, **OC**, and **DC** — are displayed in a unified grid. Base columns are always present; the trailing columns change based on the Role filter.

#### Base columns (always shown)
Team, Role, OVR, Dev, Age, Exp, Scheme

#### All Roles view (no role filter)
Trailing columns: Leadership, Agg, RB Wk, Demo — all sortable and inline-editable.

#### Head Coach filter
Trailing columns: 6 HC attributes + Leadership + Agg + RB Wk

| HC Attribute | What it governs |
|---|---|
| Game Mgmt | Clock management, timeouts, challenges |
| Play Calling | In-game situational play selection |
| Player Dev | XP gain multiplier for coached players |
| Leadership | Locker room chemistry and morale |
| Discipline | Penalty rate and practice performance |
| Adaptability | Mid-game scheme adjustment effectiveness |

#### Offensive Coordinator filter
Trailing columns: 6 OC attributes

| OC Attribute | What it governs |
|---|---|
| Pass Design | Pass play efficacy and route concept quality |
| Run Design | Run scheme effectiveness |
| RZ Offense | TD% inside the 20 |
| 3rd Down Off | 3rd down conversion rate modifier |
| Tempo | Pace of play and hurry-up capability |
| Situational | 2-pt attempts, screens, trick plays |

#### Defensive Coordinator filter
Trailing columns: 6 DC attributes

| DC Attribute | What it governs |
|---|---|
| Pass Cov | Coverage shell effectiveness |
| Run Defense | Gap discipline and run fits |
| Pass Rush | Stunt/twist packages and blitz design |
| RZ Defense | Points allowed inside the 20 |
| 3rd Down Def | Stop rate on 3rd down |
| Turnover Gen | Forced fumble and INT tendency |

### Coaching Inline Editing
| Column | How to edit |
|---|---|
| **OVR** | Double-click → type or use ↑/↓ keys |
| **Dev Trait** | Single click → dropdown |
| **Age / Exp** | Double-click → type or use ↑/↓ keys |
| **Scheme** | Single click → dropdown (OC/DC only; HC opens side panel) |
| **HC Attribute chips** | Double-click → type or use ↑/↓ keys |
| **OC/DC Attribute chips** | Double-click → type or use ↑/↓ keys |
| **Leadership** | Single click → dropdown (HC rows only) |
| **Agg / RB Wk** | Double-click → type or use ↑/↓ keys (1–10, HC rows only) |
| **Demo** | Single click → dropdown (all roles) |

### Coaching Filters
- **Search** — filter by coach name or team
- **Team** — all teams present in the loaded file
- **Role** — Head Coach, Off. Coordinator, Def. Coordinator
- **Off. Scheme** — WestCoastTiming, OutsideZoneRun, AirRaidSpread, PowerRunGap, RPOSpreadOption, VerticalDownfield
- **Def. Scheme** — Tampa2Cover2Zone, Cover3Quarters, PressManCover1, BlitzHeavyFireZone, ThreeFourTwoGap, BendDontBreak

### Coaching Side Panel
Opens when you click any coach row:

| Section | Fields |
|---|---|
| **Identity** | First/Last name, demographic |
| **Vitals** | Overall (40–99), Dev Trait, Age, Experience |
| **Appearance** | Clothing type, clothing color ID, wearing hat |
| **Scheme** | HC: Off. Scheme + Def. Scheme + Leadership Trait; OC: Off. Scheme; DC: Def. Scheme |
| **Team Philosophy** | Aggressiveness (1–10) and RB Workload (1–10) sliders — HC only |
| **HC / OC / DC Attributes** | All 6 role-specific attributes, 40–99 range |

---

## File Operations

| Button | What it does |
|---|---|
| **⬆ Import JSON** | Load any War Room roster `.json` file |
| **💾 Save** | Commits all changes to the in-memory session (clears the unsaved indicator). Use as a checkpoint. |
| **⬇ Export JSON** | Opens a native save dialog (Chrome/Edge) so you can choose the filename and save location. Falls back to an automatic download on Firefox/Safari. |

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

The `coaching` block is optional. Teams without a coaching entry get auto-generated coaches.

---

## Attribute & Rating Reference

| Range | Tier | Color |
|---|---|---|
| 90–99 | All-Pro / Elite | 🟡 Yellow-green |
| 75–89 | Pro Bowl / Good | 🔵 Blue |
| 60–74 | Starter / Average | 🟠 Amber |
| 40–59 | Backup / Poor | 🔴 Red |

OVR and POT follow the same scale. Coaching attributes (40–99) use the same color tiers.

---

## Browser Compatibility

| Browser | Status | Export Dialog |
|---|---|---|
| Chrome 90+ | ✅ Full support | ✅ Native save dialog |
| Edge 90+ | ✅ Full support | ✅ Native save dialog |
| Firefox 88+ | ✅ Full support | ⬇ Auto-download |
| Safari 14+ | ✅ Full support | ⬇ Auto-download |

---

## Contributing

Pull requests welcome. If you find a bug or want to request a feature, open an issue. Please keep the zero-dependency, single-file philosophy — the whole point is that anyone in the community can just download one file and go.

---

## License

MIT — see `LICENSE` for details.
