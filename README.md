# Shakedown

A Grateful Dead "Today in History" creation for the Rabbit R1. Shows the top-rated concert from the current calendar date across all years, with a full tracklist and inline audio playback.

## What It Does

On load, the app queries the [Relisten API](https://api.relisten.net) for the highest-rated Grateful Dead show recorded on today's month and day, then pulls the best-rated recording of that show. You get:

- Show date, venue, and location
- Recording source and lineage info
- Full tracklist with set labels
- Play/pause, next/previous track controls
- Auto-scrolling now-playing highlight
- R1 hardware button support (side click, scroll up/down)

## Installing on R1

Scan the QR code at `/qr.html` using your R1's Creations scanner. The code encodes all the metadata the R1 needs to install it directly.

## Running Locally

No build step — just serve the repo root:

```bash
python3 -m http.server 8000
# or
npx http-server
```

Then open http://localhost:8000.

## Deployment

Pushes to `main` automatically deploy to GitHub Pages via the workflow in `.github/workflows/pages.yml`.

## Tech

- Vanilla HTML/CSS/JS, no dependencies
- [Relisten API](https://api.relisten.net) for concert data
- [api.qrserver.com](https://api.qrserver.com) for QR code generation
- GitHub Pages for hosting

## License

[MIT](LICENSE)
