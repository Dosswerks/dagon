# Dagon — A Dosswerks Arcade Game

A Defender-style underwater arcade shooter inspired by H.P. Lovecraft's short story *Dagon*. Defend the Monolith and protect the Deep Ones from abduction in the depths of a Lovecraftian ocean.

**Lovecraft Arcade Volume 3**

## Play

Open `index.html` in a modern browser. No build step or server required.

## Controls

| Key | Action |
|-----|--------|
| Arrow Keys / WASD | Move |
| Space / Z | Fire |
| X / B | Smart Bomb |
| Shift / C | Dash |
| Esc / P | Pause |
| M | Mute / Unmute |
| Q | Quit to Title (Game Over screen) |

Gamepad supported (D-pad/left stick for movement, A=fire, B=dash, X=bomb, Start=pause).

## Objective

- Destroy all enemies in each level to advance
- Protect the Monolith from Crab attacks
- Rescue Deep Ones from Abductors before they're mutated
- Avoid tentacles, mines, and enemy projectiles
- Survive as long as possible for a high score

## Enemies

| Enemy | Behavior |
|-------|----------|
| **Abductor** | Seeks and kidnaps Deep Ones, carries them to the surface to mutate them |
| **Crab** | Marches along the sea floor toward the Monolith and damages it on contact |
| **Pursuer** | Chases the player and fires projectiles |
| **Drifter** | Floats in semi-random patterns, drops pulsing mines |
| **Mutant** | Created when an Abductor successfully mutates a Deep One; fast and relentless |

## Game Mechanics

- **Deep Ones** wander near the sea floor and repair the Monolith when damaged. Once all enemies are cleared, they actively seek the Monolith to heal it.
- **Monolith** has a health bar. If destroyed, the game ends with "The Monolith Has Fallen."
- **Smart Bombs** destroy all enemies and mines in the viewport.
- **Dash** grants brief invulnerability and a speed burst (cooldown-based).
- **Combo System** rewards rapid kills with score multipliers.
- **Tentacles** rise from the ocean floor as static obstacles the player must navigate around.
- **Difficulty scales** with each level: more enemies, faster speeds, higher aggression.

## Technical Details

- Single HTML file, no dependencies (except QR code library for tip jar)
- 480×270 native resolution with integer scaling and HiDPI support
- Delta-time game loop at 60fps baseline
- 1920px wrapping world (4× viewport width)
- Procedural terrain, bioluminescent particles, parallax background
- Namco-style 8×8 pixel font for all in-game text
- Web Audio API sound system with SFX, music, and ambient channels
- Object pooling for projectiles and particles
- Seeded PRNG for deterministic level generation

## Assets

All sprite and audio assets go in the `assets/` folder:

### Sprites
- `player_1.png`, `player_2.png` — Player (80×29, 2 frames)
- `abductor_1.png`, `abductor_2.png` — Abductor (110×95 source, displayed at 40×52)
- `crab_1.png`, `crab_2.png` — Crab (50×27)
- `pursuer_1.png`, `pursuer_2.png` — Pursuer (70×36)
- `drifter_1.png`, `drifter_2.png` — Drifter (50×40)
- `mutant_1.png`, `mutant_2.png` — Mutant (130×54)
- `monolith.png` — Monolith (40×64)
- `deep-one.png` — Deep One (11×20)
- `tentacle.png` — Tentacle (45×160)
- `player-projectile.png` — Player projectile (8×4)
- `enemy-projectile.png` — Enemy projectile (6×6)
- `ground-house.png`, `ground-ruin.png` — Sea floor structures
- `background.png` — Parallax background (405×270, tiles with blended seams)
- `title-logo.png` — Title screen logo (534×360)
- `title-bg.png` — Title screen background (480×270)
- `gameover-bg.png` — Game over screen background (480×270)

### Audio
- `player-fire.mp3` — Player shoots
- `player-death.mp3` — Player dies
- `enemy-death.mp3` — Enemy destroyed
- `mine-detonate.mp3` — Mine explodes
- `mine-placement.mp3` — Drifter drops mine
- `level-complete.mp3` — Level cleared
- `level-begin.mp3` — New level starts
- `game-over.mp3` — Game over
- `deep-one-rescued.mp3` — Deep One freed
- `deep-one-abducted.mp3` — Deep One grabbed
- `monolith-attack.mp3` — Crab attacks Monolith
- `ambient-underwater.mp3` — Ambient loop
- `music.mp3` — Music loop

## Credits

Based on [*Dagon*](https://hplovecraft.com/writings/fiction/d.aspx) by H.P. Lovecraft.

A game by [Andrew Doss](https://www.andrewdoss.com).

© 2026 Andrew Doss. All Rights Reserved.
