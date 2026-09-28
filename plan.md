# 📋 Plan — IRON CIRCUIT Website: Proximate Implementace

## Kontext
- **Status quo:** Single-page landing page (`index.html`) — Hero, Coming Soon, League, Pilots (5), Arenas (4), Modes, ICN News, Footer + Music dock.
- **Design system:** Dark industrial, accent `#d8902f`, fonts: Teko / IBM Plex Sans / IBM Plex Mono.
- **Media available:** 5 pilot porträty, 4 arena images, 1 soundtrack, layered Vesna portrait (`news_anchor/`).

---

## Prioritet 1 — Social Media Links ve Footer
**Estimace:** 15–20 min
- [x] Add ikonky (SVG inline) social siet: YouTube
- [x] Style: ghost links ve accent-color, hover glow effect
- [x] Position: nad copyright line, horizontal row
- Link: `https://www.youtube.com/@FilipoLipos`

## Prioritet 2 — Interactive Pilot Cards (detailed view)
**Estimace:** 45–60 min
- [ ] Click on pilot card → overlay/modal se pilot details
- [ ] Inside modal: full portrait, robot stats, move list preview, corporate lore
- [ ] Close: click outside / X button / ESC key
- [ ] CSS: backdrop-blur, accent border, entrance animation

## Prioritet 3 — Arenas Carousel (enhancement)
**Estimace:** 30–45 min
- [ ] Add `aria-label`, `alt` text improvements
- [ ] Add hover parallax effect on arena images
- [ ] Add "View arena details" CTA per card → modal s arena map + special rules

## Prioritet 4 — Modes: Expandable Detail Cards
**Estimace:** 20–30 min
- [ ] Accordion-style expand on click
- [ ] Reveal: move list, combos, controls, difficulty tips
- [ ] Collapses back when another mode is opened

## Prioritet 5 — ICN News Section Enhancement
**Estimace:** 30–45 min
- [ ] Enhance Vesna portrait: scanline overlay + flicker effect (from `news_anchor/` layers)
- [ ] Add ICN ticker / breaking news bar above the section
- [ ] Add 2–3 fake ICN headlines that rotate

## Prioritet 6 — Scroll Reveal Animations
**Estimace:** 20–30 min
- [ ] IntersectionObserver: fade-in / slide-up sections on scroll
- [ ] Pilot cards staggered entrance
- [ ] Arena cards slide from left/right alternately

## Prioritet 7 — Game Screenshots / GIFs Section
**Estimace:** 30–45 min (depends on assets)
- [ ] Add new section "In Action" between Modes and ICN
- [ ] Grid of screenshot cards (2x2 or 3x2)
- [ ] Hover: zoom + play icon for GIFs
- [ ] Placeholder frames if assets not ready

---

## Quick Wins (bonus — <10 min each)
| # | Item | Benefit | Status |
|---|------|---------|--------|
| B1 | Add `scroll-behavior: smooth` meta viewport | Polished nav | ✅ |
| B2 | Add favicon / manifest | Professional finish | ✅ |
| B3 | Fix `overflow-x: hidden` → `overflow-x: clip` + remove `overflow-y: hidden` bug | CSS spec + scrolling | ✅ DONE |
| B4 | Add `prefers-reduced-motion` media query | Accessibility | ✅ |
| B5 | Add tooltip on `cs-submit` for privacy info | UX polish | ✅ DONE |

---

## Suggested Order (prioritization)
1. **Quick wins B2, B3, B4** — cleanup + accessibility
2. **Prioritet 1** — social links (quick + high value)
3. **Prioritet 6** — scroll reveal (makes entire page feel alive)
4. **Prioritet 2** — pilot detail overlay (most requested feature)
5. **Prioritet 5** — ICN enhancement (lore/immersion)
6. **Prioritet 3+4** — arena/mode enhancements
7. **Prioritet 7** — screenshots (needs assets)
