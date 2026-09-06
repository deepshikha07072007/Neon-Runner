# DRIFT — Neon Runner

A single-file, browser-based endless runner built with HTML5 Canvas and vanilla JavaScript. No dependencies, no build step — just open `index.html` and play.

![Genre](https://img.shields.io/badge/genre-endless%20runner-4ff2e0) ![Tech](https://img.shields.io/badge/tech-Canvas%20%2F%20JS-ff3ea5)

## About

DRIFT drops you on a neon grid floor that scrolls endlessly toward you. Jump obstacles, slide under bars, grab coins, and survive as the speed ramps up. It's a synthwave-styled take on the classic "runner" genre (think Chrome Dino / Subway Surfers), themed around glowing grids, distant mountains, and a shifting color palette.

## How to Play

1. Open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge).
2. Click **Start Run** (or press **Space** / tap the screen).
3. Survive as long as you can — hitting an obstacle ends the run.

### Controls

| Action | Desktop | Mobile |
|---|---|---|
| Jump | `Space` or click/tap | Tap screen |
| Slide | `↓` Arrow | Swipe down |
| Pause | `P` or pause icon | Pause icon |
| Restart | `Space` on game-over screen | Run Again button |

## Gameplay Mechanics

- **Distance score** — increases automatically based on how far/fast you've traveled.
- **Coins** — floating pickups worth +25 points each, spawned in small clusters.
- **Obstacles** — three types, randomly spawned:
  - *Spike* — jump over
  - *Block* — jump over
  - *Bar* (overhead) — slide under
- **Speed ramp** — the runner speeds up the longer you survive, up to a max speed cap, and obstacles spawn more frequently over time (difficulty scales over the first ~45 seconds).
- **Theme shift** — the color palette (grid, glow colors, sky) cycles through 4 neon themes every 400 points.
- **Best score** — tracked for the current browser session and shown in the HUD and game-over screen.

## Features

- Fully responsive canvas that scales to fit any screen size while preserving aspect ratio.
- Touch controls for mobile (tap to jump, swipe down to slide).
- Parallax scrolling background: stars, mountains, glowing horizon line, and a perspective grid floor.
- Particle effects for jumps, landings, coin pickups, and crashes (with screen shake).
- Pause/resume support.
- Zero external assets or libraries — everything (art, animation, effects) is drawn procedurally with Canvas 2D.

## File Structure

This is a single self-contained file:

```
index.html   → HTML structure, CSS styling, and all game logic (JS) in one file
```

There's nothing to install and no server required — it runs entirely client-side.

## Customization Ideas

Since the whole game lives in one file, it's easy to tweak constants near the top of the `<script>` block:

- `GRAVITY`, `JUMP_VELOCITY` — adjust jump feel
- `BASE_SPEED`, `MAX_SPEED`, `SPEED_RAMP` — adjust difficulty pacing
- `THEMES` array — add or edit color palettes
- `spawnObstacle()` — tweak obstacle type odds or add new obstacle shapes

## Notes

- Best score currently resets on page reload (it's stored in a JS variable, not `localStorage`). Adding persistence would be a natural next step.
- Built with AI-assisted prompting as a personal project.

## License

Personal / hobby project — free to modify and reuse.
