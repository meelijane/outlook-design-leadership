# Opening Remarks — MC Deck

The MC slide deck for **Outlook Design Leadership 2026** (Ritz-Carlton Melbourne, 23.04.2026), built in [Claude Design](https://claude.ai/design) and exported as a self-contained static site.

## Files

- `index.html` — the deck (25 slides, all type/ASCII/SVG, no image assets)
- `deck-stage.js` — the `<deck-stage>` web component that handles navigation, scaling, speaker notes, and print

Both are static — no build step, no dependencies beyond Google Fonts (Inter + IBM Plex Mono) loaded over CDN.

## Hosting

Drop the folder on any static host (GitHub Pages, Netlify, Vercel, S3, etc.). It serves at `/opening-remarks/`. Keep the two files together — `index.html` loads `deck-stage.js` as a sibling.

## Using the deck

- **Navigate:** ← / → arrows, PgUp / PgDn, Space, Home / End, or number keys
- **Reset to start:** press `R`
- **Speaker notes:** embedded in `index.html` as JSON (`#speaker-notes`); the component posts the current slide index to a parent window if embedded
- **Print / PDF:** the browser's Print → Save as PDF produces one page per slide
- **Tweaks panel** (palette, ASCII density, gestures, animation, accent hue) only appears inside the Claude Design editor and stays hidden when self-hosted

The canvas is authored at 1920×1080 and auto-scales (letterboxed) to fit any viewport.
