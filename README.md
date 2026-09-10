# Arcade

Single-file browser games — no build, no dependencies. Open `index.html` for the
menu, or any game `.html` directly.

## `fighter.html` — Smash-style platform fighter (in progress)

The current focus. Mario, Luigi, Zelda, and Link fight on a platform stage using
D&D spells. See [DESIGN.md](DESIGN.md) for the full spec.

Built so far:

- Title → mode (VS CPU / VS Player) → character select → fight → win screen
- Platforming: gravity, double jump, sprint (double-tap), pass-through / drop-through platforms
- Attacks: neutral, up, dash, plus a 3-hit combo ending in a launcher
- **Spells** with a shared mana pool + per-spell cooldowns:
  - **Fireball** — arcing projectile, big knockback
  - **Magic Missile** — 3 homing darts
  - **Shield** — bubble that absorbs hits and drains mana
- Damage % + knockback scaling, 3 stocks, blast zones, respawn invuln
- Per-character stats (weight / speed / jump / reach / magic)
- Basic CPU: approach, vertical chase, poke, cast, recover

Next:

- Sharper CPU (spacing, shield reads, edge-guarding)
- More attacks per character / real differentiation
- Sound, hit-stop polish, better KO feedback
- Stage hazards, stock/time options

## `flappy.html` — Flappy Bird remake (in progress)

The current focus. A bird, gravity, and a tap to flap; dodge the pipes, ride the
scrolling ground platform, don't touch anything.

Controls: `Space` / `↑` / click / tap to flap. Best score is saved locally.

Built so far:

- Bird physics (gravity + flap impulse) with tilt
- Scrolling **ground platform** and parallax hills
- Procedurally spawned pipe pairs, collision, scoring
- Ready / play / game-over states, hit flash, best-score persistence

Next:

- Sprites and polish pass on the frontend
- Sound
- Difficulty ramp (gap shrink / speed up)
- Medals on the game-over panel

## `pong.html` — unbeatable Pong

You play an overpowered bot that **cannot be beaten**. It knows exactly where the
ball is going, always gets there, and returns every shot to the corner you are
farthest from — a little faster each touch.

Controls: `W` / `S` or `↑` / `↓` (or mouse / touch) to move; `Space` to pause or
restart. CPU wins at 11; you stay at 0. The only number you can move is
**LONGEST RALLY**.
