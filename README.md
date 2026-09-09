# Pong

A minimal single-file Pong game. Open `pong.html` in a browser — no build, no dependencies.

The catch: you are playing an overpowered bot that **cannot be beaten**. It knows
exactly where the ball is going, always gets there, and returns every shot to the
corner you are farthest from — a little faster each touch. The score only moves in
one direction.

## Controls

- `W` / `S` or `↑` / `↓` — move your paddle (left side)
- Mouse / touch drag also moves your paddle
- `Space` — pause / resume, or restart after the loss
- CPU wins at 11. You stay at 0.

The only number you can actually change is **LONGEST RALLY** — how many times you
kept the ball alive in a single point.

## Roadmap

This is an early draft. Planned additions:

- Escalating taunts as the score climbs
- Sound effects
- Persist the best rally between sessions
- Increasingly absurd bot behavior
