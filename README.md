# Bad Vibe Survivor

A minimalist, fast-paced survivor game built as a self-contained browser experience. Move through a procedurally generated arena, collect XP gems, survive increasingly difficult enemies, and choose automatic weapons and passive upgrades between levels.

![Bad Vibe Survivor](https://img.shields.io/badge/game-browser-blue) ![Technology](https://img.shields.io/badge/built%20with-HTML%2FCSS%2FJavaScript-orange)

## Play

Open `index.html` in a modern browser, or serve the repository with any static web server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Gameplay

- Survive against an ever-growing swarm of geometric enemies.
- Collect XP gems to gain levels.
- Choose from three randomized weapons or passive upgrades on level-up.
- Build a run with up to five weapons at once.
- Defend against stronger enemies, including a boss every 90 seconds.
- Explore randomized terrain made from arenas of rectangles and circles.
- Beat your best survival time, saved locally in the browser.

## Controls

| Action | Keyboard | Touch / Pointer |
|---|---|---|
| Move | `WASD` or arrow keys | Drag or point in the desired direction |
| Pause | `Escape` or `P` | Use the pause interface |
| Select upgrade | `1`, `2`, or `3` | Tap a card |

All attacks, projectiles, and weapon effects are automatic. Movement is the main control.

## Weapons

Each run begins with one randomly selected weapon. Other weapons can be discovered through level-up choices, and owned weapons can be upgraded to level 7.

The available arsenal includes:

- Windmill
- Punch
- Whip
- Aura
- Soul Scythe
- Slime Trail
- Mines
- Orbit
- Pulse
- Mace
- Spike Ring
- Whirlwind
- Shards
- Needle Storm
- Axe
- Daggers
- Ricochet
- Bombs
- Bolt
- Seekers
- Laser
- Chain Lightning
- Boomerang
- Vortex
- Comet
- Sentinel

## Passives

Passives can be upgraded to level 6:

- **Vitality** — increases maximum health
- **Swiftness** — increases movement speed
- **Magnet** — increases XP pickup range
- **Power** — increases damage
- **Haste** — reduces weapon cooldowns
- **Regen** — restores health over time

## Features

- 30-piece shape pool for players, enemies, projectiles, and previews
- Random enemy shapes and complementary run color palettes
- Nine randomized terrain layouts
- Multiple enemy movement patterns, including zig-zag, dash, orbit, hop, and ghost movement
- Spatial-grid enemy lookup for efficient collision and attack queries
- Particle effects, screen effects, explosions, knockback, slowing, and homing projectiles
- Responsive desktop and mobile layout
- Local best-time tracking
- Shape gallery accessible from the title screen

## Technical Notes

The entire game is contained in `index.html`:

- Plain HTML, CSS, and JavaScript
- Canvas-based 2D rendering
- No build step or external dependencies
- `localStorage` is used for the best survival time
- Uses a spatial hash grid for collision and nearby-enemy queries
- Supports high-density displays and mobile safe-area insets

## Project Structure

```text
.
├── index.html  # Game markup, styles, and complete JavaScript implementation
└── README.md   # Project documentation
```

## Development

Run a local server for the best browser-development experience:

```bash
python3 -m http.server 8000
```

Edit `index.html` and refresh the page. There is no compilation or asset pipeline.
