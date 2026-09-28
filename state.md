# Project State — IRON CIRCUIT Website

## Session Info
- **Date**: 2026-09-28
- **Status**: YouTube social icon verified and in place

## What's Been Done
- ✅ Verified YouTube social icon in footer — `media/icon/youtube.png` correctly linked and image file exists (4.4 KB)
- ✅ Explored project structure — single-page HTML site with embedded CSS/JS
- ✅ Added "Coming Soon" section:
  - Live countdown timer to launch date (Dec 15, 2026)
  - Animated days/hours/minutes/seconds blocks
  - Email notification signup form with confirmation feedback
  - Corner bracket decorations matching industrial theme
  - CRT-style scanlines background pattern
  - Glowing "Launching 2026" badge with pulse animation
  - Shimmer gradient animation on the title text
  - Responsive design for all screen sizes
  - Placed between hero and league sections
- ✅ Removed sweep line (scanline) animation from Coming Soon countdown overlay
- ✅ Enhanced Vesna Holt (ICN News Anchor) portrait animation:
  - Added `base-drift` — subtle head movement on the base portrait layer
  - Speeded `blink-layer` cycle from 6s to 3.5s for more natural blinking
  - Added `lights-pulse` — independent scale/pulse on the lights layer
  - Enhanced `plate-shift` with more intermediate keyframes
  - Added `masks-color` — subtle sepia/saturation shifts on the masks layer
  - Added `glow-pulse` — pulsing border-box-shadow on the portrait container
  - Added scanline overlay — animated horizontal line sweeping across the portrait
  - Tightened `portrait-crt` flicker timing for more dynamic broadcast feel
- ✅ Analyzed existing design system:
  - Dark industrial aesthetic (dark backgrounds, warm orange accent #d8902f)
  - Fonts: Teko (display), IBM Plex Sans (body), IBM Plex Mono (labels)
  - Sections: Hero, League, Pilots (5), Arenas (4), Modes, ICN News, Footer
  - Features: Fixed top bar, music player dock, responsive layout

## What's Next / TODO
- [ ] (future) Add game screenshots or GIFs
- [ ] (future) Add trailer embed
- [ ] (future) Add social media links in footer
- [ ] (future) Add more interactive elements / animations

## Design Notes
- Color palette: dark ink (#070a0c), panel (#11181d), steel (#34434b), accent (#d8902f / #f2b34d)
- All styles are embedded in `<style>` in index.html
- The "Coming Soon" section is placed between hero and league section
- Should maintain the corporate sci-fi / mech aesthetic
- Use Teko for headings, IBM Plex Mono for labels

## Key Files
- `index.html` — main page with all CSS and JS inline
- `media/arenas/` — arena images
- `media/pilots/` — pilot character images
- `media/audio/` — soundtrack files
