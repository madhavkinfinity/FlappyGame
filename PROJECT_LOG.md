# PROJECT_LOG.md

## Project
Fun Flamingo (web game)

## Current status
- Core Flappy-style game loop implemented with watercolor/Monet-inspired visual style.
- Flamingo character with wing animation is implemented.
- Current Fields mechanic is implemented (soft directional drift zones).
- Procedural water ripples and animated lily pads are implemented.
- Synthesized audio implemented via Web Audio API:
  - flap, score, hit, game-over SFX
  - ambient and piano-like background loop
- Splash screen implemented (`Tap To Start`).
- Fullscreen button implemented for desktop/mobile with:
  - Fullscreen API path where available
  - In-app immersive fallback when browser fullscreen API is unavailable
- Responsive rendering implemented with orientation-based world sizing:
  - landscape world: `900x600`
  - portrait world: `600x900`

## Mobile portrait optimization
Tuned portrait profile (new):
- Slower pace in portrait:
  - `scrollSpeed`: 162 (portrait) vs 185 (landscape)
  - `spawnEvery`: 1.36 (portrait) vs 1.22 (landscape)
- Easier obstacle profile in portrait:
  - `pipeGap`: 238 (portrait) vs 180 (landscape)
  - Safer spawn bounds via `pipeTopPadding`/`pipeBottomPadding`
- Gentler current forces in portrait:
  - `currentForceX`: 120 (portrait) vs 210 (landscape)
  - `currentForceY`: 170 (portrait) vs 260 (landscape)
- Slightly stronger flap in portrait:
  - `flapImpulse`: -385 (portrait) vs -370 (landscape)

## Safari/iOS behavior notes
- Browser fullscreen API support can vary by Safari version and context.
- Added fullscreen API usage + in-app immersive fallback to maximize usable screen space.
- Added web-app capable meta tags and manifest/service worker for installability.
- Added scroll/gesture suppression to reduce accidental page movement.

## Key files
- `index.html`: app shell, overlays, splash, fullscreen button
- `styles.css`: full-viewport app layout, safe-area padding, mobile styling
- `game.js`: gameplay, rendering, audio, orientation logic, portrait tuning
- `manifest.webmanifest`: PWA manifest metadata
- `sw.js`: service worker for offline cache
- `icon.svg`: app icon used by manifest
- `screenshot-mockups.html` and `screenshot-mockups.css`: App Store screenshot concepts

## Run locally
```bash
cd "/Users/madhavkyatsandra/Documents/New project"
python3 -m http.server 8000
```
Open: `http://localhost:8000`

## Publish flow (GitHub Pages)
1. Commit and push `main`.
2. GitHub repo -> Settings -> Pages.
3. Source: Deploy from branch, branch: `main`, folder: `/ (root)`.

## Open issues / next improvements
- Validate Safari portrait behavior on physical devices after hard refresh.
- Add optional in-game iOS banner on splash with one-tap A2HS instructions.
- Consider dynamic difficulty ramp after 20+ score.
- Add pause/resume and mute toggle for mobile convenience.
