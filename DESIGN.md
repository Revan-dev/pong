# Fighter — design

A Smash-style platform fighter with D&D spells. Canvas shapes, no assets.

## Roster (4)

| Character | Identity | Tuning |
|-----------|----------|--------|
| Mario  | all-rounder            | baseline everything |
| Luigi  | floaty, slippery       | higher jump, low friction, weak grounded game |
| Zelda  | glass-cannon caster    | slow, weak melee, strong spells + fast mana regen |
| Link   | disjointed melee       | sword = longer attack reach, heavier |

## Controls (Smash-style)

Two players share the keyboard; P2 can be swapped for CPU.

| Action | P1 | P2 |
|--------|----|----|
| Move / aim | `A` `D` | `←` `→` |
| Jump (double) | `W` | `↑` |
| Drop through platform | `S` | `↓` |
| Attack | `F` | `.` |
| Cast selected spell | `G` | `/` |
| Cycle spell | `T` | `,` |
| Sprint | double-tap `A`/`D` | double-tap `←`/`→` |

## Moves

- **Jump** — grounded jump + one air jump (weaker).
- **Sprint** — double-tap a direction; ~1.8x move speed while held.
- **Attack** — context sensitive:
  - neutral: fast, weak, low knockback
  - up (hold jump direction): launches upward, anti-air / juggle
  - dash (while sprinting): strong, high knockback, more endlag
- **Combination** — neutral → neutral within the combo window → third hit auto-becomes a launcher.

## Spells — mana + cooldowns

Shared mana pool (100), regenerates over time (faster for Zelda). Each spell has a cast cost and a cooldown.

| Spell | Cost | Cooldown | Effect |
|-------|------|----------|--------|
| **Fireball** | 25 | 0.75s | Arcing projectile, big damage + knockback |
| **Magic Missile** | 30 | 1.5s | 3 homing darts, low damage each, minimal knockback |
| **Shield (bubble)** | 15 + drain | 0.5s after drop | Bubble that absorbs hits and projectiles; drains mana while up, slows you, blocks attacking |

## Rules

- **Stocks:** 3 each. **Damage %** builds up; knockback scales with the victim's %.
- Leave the blast zone (past any screen edge) → lose a stock, respawn with invuln.
- Last player with stocks wins.

## Stage

One main platform + two floating platforms, all pass-through from below. Blast zones on all four edges.

## Modes

- **VS Player** — local 1v1
- **VS CPU** — P2 is a simple AI (approach, poke, recover, occasional cast)
