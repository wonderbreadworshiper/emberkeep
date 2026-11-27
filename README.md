# EMBERKEEP — a pixel-art tower defense

Open **index.html** in any modern browser. No install, no assets, no internet needed — the whole game is one file.

Survive 20 waves of goblins, wargs, orcs, slimes, ogres and a dragon. Build along the winding road, upgrade your towers, and do not let them reach the keep. When the campaign is over, switch to **Endless Siege** on the title screen and see how long your defense holds.

## Controls

| Input | Action |
| --- | --- |
| Mouse | Select / build / hover for info |
| `1` `2` `3` `4` | Pick Archer / Cannon / Frost / Mage |
| Click a grass tile | Place the selected tower |
| Click a tower | Inspect it and open its upgrade sidebar |
| Click an upgrade path | Buy the next tier of that path |
| `U` / `X` | Upgrade the cheapest path / sell the selected tower |
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

Each tower has **three upgrade paths** (range, damage, speed — Frost's third path is slow strength), and each path upgrades **three times**. Buying a path tier only changes that stat, so you can build a long-range sniper, a rapid-fire archer, or anything between. Selling refunds 60% of everything invested.

## Difficulty and modes

- **Campaign** — 20 hand-built waves, then victory.
- **Endless Siege** — the same 20 waves, then procedurally generated hordes forever: mixed enemy types, rising HP and rewards, an ogre warband every 5 waves and a dragon every 20.
- **Easy** — 30 lives, extra gold, weaker enemies.
- **Normal** — 20 lives, the intended experience.
- **Hard** — 15 lives, tougher and greedier enemies.

Each mode and difficulty keeps its own best-wave record in your browser (localStorage), shown on the title screen. Endless records count waves survived.

## Tips

- Frost + Cannon is a strong combo: clump them up, then shell them.
- Orcs and bosses have armor — Archers and Cannons lose damage to it, Mages do not.
- Slimes split into two oozes when killed. Finish them before they split near the exit.
- Bosses (campaign: ogres on 5/10/15/19, dragon on 20 — endless: an ogre every 5 waves, a dragon every 20) cost 5 lives if they leak.

## Tweaking the game

Everything lives in `index.html`:

- `WAY` — the road waypoints (tile coordinates).
- `WAVES` — campaign wave composition: `[type, count, gapSeconds, delaySeconds]`.
- `endlessWaveRow` — procedural waves for Endless Siege past wave 20.
- `TOWERS` — cost, base stats and the three upgrade paths (each with three tiers and prices).
- `ENEMIES` — HP, speed, armor, gold, sprite size.
- `DIFFS` — lives/gold/HP multipliers per difficulty.
- `DECOR` — trees and rocks that block building.

Save and refresh the page after editing.
