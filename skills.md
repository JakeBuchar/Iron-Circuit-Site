# Skills — IRON CIRCUIT Website

## Project Overview
Single-page promotional website for **IRON CIRCUIT**, a corporate mech combat fighting game. Built as a local versus and single-player fighting game in **Godot 4**. The site serves as a landing page and lore hub — not a web game, the actual game is built in Godot.

### Core Identity
- **Title**: Iron Circuit — Corporate Mech Combat League 2097
- **Theme**: Corporate mech fighting league settling disputes through mechanized combat
- **Tone**: Industrial, gritty, near-future sci-fi (year 2097)
- **Style**: Dark, high-contrast, mechanical aesthetic with warm orange accents

---

## Design System

### Colors
```
--ink:        #070a0c   (main background)
--panel:      #11181d   (card/content panels)
--steel:      #34434b   (borders, subtle elements)
--text:       #d8e1df   (primary text)
--muted:      #7f9795   (secondary text)
--accent:     #d8902f   (primary accent — warm orange/gold)
--accent-hot: #f2b34d   (hover/highlight accent)
--danger:     #d64242   (alerts, live indicator)
```

### Fonts
| Role | Font | Usage |
|------|------|-------|
| Display/Headings | Teko | Titles, section kickers, stat numbers |
| Body | IBM Plex Sans | Paragraph text, descriptions |
| Mono/Labels | IBM Plex Mono | Caps labels, metadata, UI text |

### Layout Rules
- Max content width: `min(1120px, calc(100% - 2.5rem))`
- Section padding: `5.5rem` vertical
- Pillar/stack elements use `gap` spacing, not margins where possible
- All padding uses `rem` units
- Responsive breakpoints: `980px`, `640px`

### Typography Conventions
- **Section kickers** (labels above titles): mono, 0.72rem, uppercase, `letter-spacing: 0.2em`, accent color
- **Section titles**: Teko, bold, `clamp(2.4rem, 5vw, 3.4rem)`, uppercase, `letter-spacing: 0.06em`
- **Body lead**: `color: var(--muted)`, max-width `36rem`, `font-size: 1.08rem`
- **Caps labels**: mono, small, uppercase, generous letter-spacing
- **Numbers/stats**: Teko, large, bold

---

## Component Library

### Buttons
- `.btn` — base button (padding, font-family, uppercase)
- `.btn-fill` — solid accent background, dark text
- `.btn-ghost` — transparent background, steel border, hover accent border

### Cards
- `.stat` — left accent border, bold number, mono label
- `.pilot` — image on top, bordered meta below, hover lift effect
- `.arena` — split grid (image + text), alternating layout
- `.mode` — top accent border, mono content panel style

### Special Sections
- **Hero**: Full viewport, animated background image, gradient overlay, CTA row
- **Coming Soon**: Countdown timer, email capture form, corner brackets, scanline effect
- **ICN News**: Inverted color scheme (light blue on cream), news-banner style
- **Footer**: Simple two-column, muted text

### Music Dock (Fixed Player)
- Fixed position, bottom-right
- Animated equalizer bars when playing
- Minimize/restore toggle
- Play, Stop, Mute controls
- Auto-plays on load

---

## Site Structure

```
Header (fixed top bar)
  └─ Brand "IRON CIRCUIT" + nav links

Hero (full viewport)
  └─ Tagline → Title → Lead text → CTA buttons

Coming Soon (NEW)
  └─ Badge → Title → Countdown → Email form

League / About
  └─ Section kicker → Title → Lead → Stats row (4 items)

Pilots (Roster)
  └─ 5 pilot cards (image + call name, name, robot, corp)

Arenas (Venues)
  └─ 4 arena cards (alternating image/text layout)

Modes (How to Play)
  └─ 3 mode cards (Versus, Campaign, Hangar & Jukebox)

ICN News
  └─ Inverted banner with news image + story text

Footer
  └─ Brand → Copyright
```

---

## Assets

| Directory | Contents |
|-----------|----------|
| `media/arenas/` | Arena background images (iron_city.jpg, overgrown_ruins.jpg, lantern_harbor.jpg, neo_prague.jpg) |
| `media/pilots/` | Pilot character images (mephala.jpg, kwame.jpg, liuliu.jpg, arjun_chandra.jpg, filip_vokurka.jpg, vesna_holt.jpg) |
| `media/audio/` | Soundtrack (metal-arena.wav) |

---

## Key Content

### The 5 Pilots
1. **Mephala** — "Iron Web" — PHALANX fortress/doctrine — Titan Defense Systems
2. **Kwame** — "Redline" — RAVEN rushdown duelist — Redline Motor Works
3. **Liuliu** — "Ghost Orchid" — GHOST air interceptor — Jade Sky Systems
4. **Arjun Chandra** — "Vanguard" — VALIANT balanced line — Bastion Dynamics
5. **Filip Vokurka** — "Blacksmith" — BIVOJ industrial brawler — Moravian Heavy Works

### The 4 Arenas
1. **Iron City** — City Arena (broadcast stage)
2. **Overgrown Ruins** — Reclaimed City (Sector 6)
3. **Lantern Harbor** — Harbor District (Lantern Quay)
4. **Neo Prague** — Vltava Skyline (Bohemia)

### Game Modes
- **Versus**: Local 2P or vs AI (Easy/Normal/Hard), best-of-3
- **Campaign**: 5 pilot stories, unlock sequentially, ICN news between matches
- **Hangar & Jukebox**: Chassis inspection, pilot dossiers, music player

---

## Editing Guidelines

### When modifying styles:
- Keep all CSS in the `<style>` block in `<head>` — this is a single-file site
- Follow existing class naming: kebab-case with clear descriptive names
- Use CSS custom properties (`var(--name)`) for all colors
- Maintain responsive breakpoints at 980px and 640px

### When adding new components:
- Use existing fonts (Teko for display, IBM Plex Sans for body, IBM Plex Mono for labels)
- Follow the accent color convention (`--accent` for primary, `--accent-hot` for hover)
- Keep card borders at `1px solid rgba(52, 67, 75, 0.7)` style
- Maintain the industrial/mech aesthetic — no soft curves or playful elements

### When editing content:
- Keep lore consistent: year 2097, corporate warfare, mech combat
- Pilot names and robot chassis names are fixed lore
- Arena descriptions are part of the game's worldbuilding

### Countdown timer:
- Target date defined as `TARGET` Date object in the `<script>` block
- Format: `new Date("YYYY-MM-DDTH00:00:00Z")`
- Timer updates every 1000ms via `setInterval`

---

## File: index.html (single file — everything inline)
- `<style>` in `<head>` contains all CSS (~400+ lines)
- `<script>` at end of `<body>` handles music player + countdown
- All images referenced via `media/` relative paths
- Google Fonts loaded via preconnect + link tags
