# EMBERKEEP — a pixel-art tower defense

Open **index.html** in any modern browser. No install, no assets, no internet needed — the whole game is one file.

Survive 20 waves of goblins, wargs, orcs, slimes, ogres and a dragon. Build along the winding road, upgrade your towers, and do not let them reach the keep.

## Controls

| Input | Action |
| --- | --- |
| Mouse | Select / build / hover for info |
| `1` `2` `3` `4` | Pick Archer / Cannon / Frost / Mage |
| Click a grass tile | Place the selected tower |
| Click a tower | Inspect it (range, damage, kills) |
| `U` / `X` | Upgrade / sell the selected tower |
| `Space` | Start the next wave |
| `S` | Toggle 1x / 2x speed |
| `P` / `Esc` | Pause (Esc also cancels a build) |
| `M` | Mute sound |
| Right-click | Cancel build / deselect |

## Towers

| Tower | Cost | Role |
| --- | --- | --- |
| Archer | 80 | Fast single-target arrows. Cheap backbone. |
| Cannon | 140 | Slow shells with splash damage. Great vs crowds. |
| Frost | 110 | Pulses chill every enemy in range (slow + light damage). |
| Mage | 180 | Chain lightning that ignores armor. |

Each tower has three levels. Upgrades cost gold; selling refunds 60% of everything invested.

## Tips

- Frost + Cannon is a strong combo: clump them up, then shell them.
- Orcs and bosses have armor — Archers and Cannons lose damage to it, Mages do not.
- Slimes split into two oozes when killed. Finish them before they split near the exit.
- Bosses (Ogre waves 5/10/15/19, Dragon wave 20) cost 5 lives if they leak.

## Difficulty

- **Easy** — 30 lives, extra gold, weaker enemies.
- **Normal** — 20 lives, the intended experience.
- **Hard** — 15 lives, tougher and greedier enemies.

Best results are saved in your browser (localStorage) and shown on the title screen.

## Tweaking the game

Everything lives in `index.html`:

- `WAY` — the road waypoints (tile coordinates).
- `WAVES` — wave composition: `[type, count, gapSeconds, delaySeconds]`.
- `TOWERS` — cost, damage, range, rate, upgrades per tower.
- `ENEMIES` — HP, speed, armor, gold, sprite size.
- `DIFFS` — lives/gold/HP multipliers per difficulty.
- `DECOR` — trees and rocks that block building.

Save and refresh the page after editing.
