# Arcade

Single-file browser games — no build, no dependencies. Open the `.html` file in a browser.

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
