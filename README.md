# Jetpack Flamingo

Jetpack Flamingo is a browser-based, arcade-style survival game where you guide a flamingo through an icy watercolor sky using a tiny jetpack. The goal is simple: stay airborne, thread through obstacle gaps, and beat your best score.

## Gameplay at a glance

- **Tap / click / press Space or Arrow Up** to fire the jetpack and gain lift.
- The flamingo is constantly pulled down by gravity, so timing is everything.
- Fly through moving obstacle gaps to increase your score.
- The run ends when you collide, and your **best score is saved** in local storage.

## Game feel and style

- Hand-painted, watercolor-inspired visuals with soft bloom.
- Responsive world scaling for portrait and landscape play.
- Splash/start/game-over overlays plus a persistent score HUD.
- Optional fullscreen mode for immersive runs.

## Run locally

Because this is a static web game, you can run it with any simple local server:

```bash
python3 -m http.server 4173
```

Then open:

```text
http://127.0.0.1:4173
```

## Screenshots (gameplay phases)

These captures show the game flow from launch to failure, including multiple active gameplay phases.

### 1) Splash screen (before starting)

![Jetpack Flamingo splash screen](browser:/tmp/codex_browser_invocations/0a66c33594669ede/artifacts/shots2/phase-01-splash.png)

### 2) Takeoff phase (immediately after start)

![Jetpack Flamingo takeoff phase](browser:/tmp/codex_browser_invocations/0a66c33594669ede/artifacts/shots2/phase-02-takeoff.png)

### 3) Early gameplay (initial obstacle weaving)

![Jetpack Flamingo early gameplay](browser:/tmp/codex_browser_invocations/0a66c33594669ede/artifacts/shots2/phase-03-early-gameplay.png)

### 4) Extended gameplay (deeper run)

![Jetpack Flamingo extended gameplay](browser:/tmp/codex_browser_invocations/0a66c33594669ede/artifacts/shots2/phase-04-extended-gameplay.png)

### 5) Game over summary

![Jetpack Flamingo game over screen](browser:/tmp/codex_browser_invocations/0a66c33594669ede/artifacts/shots2/phase-05-game-over.png)
