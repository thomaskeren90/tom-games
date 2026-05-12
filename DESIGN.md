# TOM GAMES — Design Document

## Top 5 Simple Games Popular in Indonesia (High Downloads)

Based on market research, these are 5 simple game archetypes that dominate Indonesia's casual gaming scene with millions of downloads each.

---

## 1. 🟡 Tahu Bulat-Style — Idle Clicker

**Original:** Tahu Bulat (by Own Games, Bandung) — 10M+ downloads on Google Play
**Genre:** Idle / Incremental Clicker
**Concept:** You sell fried tofu (tahu bulat) from a street cart. Tap to sell, earn money, upgrade your cart, ingredients, and marketing. Very Indonesian cultural flavor.

### Pain Points
| # | Pain Point | Severity |
|---|-----------|----------|
| 1 | **Progression stalls hard** after initial burst — feels like a wall unless you watch ads or pay | HIGH |
| 2 | **Too many ads** — forced video ads every few taps interrupt flow | HIGH |
| 3 | **Shallow upgrades** — upgrades feel meaningless, no visual feedback on progress | MEDIUM |
| 4 | **No offline earnings** — must keep app open to progress | MEDIUM |
| 5 | **Repetitive tapping fatigue** — no automation early on | MEDIUM |

### Solution & Differentiation
- **Smooth exponential curve** — no hard walls, always feeling progress
- **Zero forced ads** — optional rewarded ads only, never interrupt gameplay
- **Rich visual upgrades** — cart transforms visually (wooden cart → food truck → restaurant chain)
- **Offline earnings** with clear "welcome back" screen showing what you earned
- **Auto-tap unlock** at reasonable level so tapping isn't mandatory forever
- **Indonesian street food theme** — gorengan, sambal, es teh visuals

---

## 2. 🐦 Flappy Tap — Endless Flyer

**Original:** Flappy Bird archetype — 100M+ downloads globally, massive in Indonesia
**Genre:** Hyper-casual / Endless Runner (flyer)
**Concept:** Tap to fly through obstacles. Dead simple, dead hard.

### Pain Points
| # | Pain Point | Severity |
|---|-----------|----------|
| 1 | **Rage quit frustration** — one mistake = restart, no checkpoint | HIGH |
| 2 | **No sense of progress** — score resets, no persistence | HIGH |
| 3 | **Ugly/derivative visuals** — most clones look like cheap copies | MEDIUM |
| 4 | **No variety** — same pipes forever, no theme changes | MEDIUM |
| 5 | **No social/competitive element** — playing alone with no comparison | LOW |

### Solution & Differentiation
- **"Ghost run" system** — your best run shows as a ghost, always chasing yourself
- **Section-based difficulty** — every 10 pipes = new visual theme (city → jungle → ocean → space)
- **Smooth difficulty ramp** — not random, feels fair
- **Indonesian landmarks** as obstacles — Monas, Borobudur silhouettes, wayang puppets
- **Daily challenge** with fixed seed — everyone plays same layout, compare scores
- **Near-miss scoring** — bonus points for threading tight gaps

---

## 3. 🍬 Gem Match — Match-3 Puzzle

**Original:** Candy Crush Saga archetype — 1B+ downloads, dominant in Indonesia
**Genre:** Match-3 Puzzle
**Concept:** Swap gems/candies to match 3+ and clear the board. Level-based progression.

### Pain Points
| # | Pain Point | Severity |
|---|-----------|----------|
| 1 | **Pay-to-win energy system** — run out of lives, must wait or pay | CRITICAL |
| 2 | **Artificial difficulty spikes** — levels designed to sell boosters | HIGH |
| 3 | **Predatory monetization** — pop-ups for purchases, confusing currency systems | HIGH |
| 4 | **Lives timer** — 30 min per life, hostile to binge play | HIGH |
| 5 | **Too many special mechanics** — bloated with confusing power-ups | MEDIUM |

### Solution & Differentiation
- **Unlimited lives** — play as much as you want, no energy system
- **Fair difficulty curve** — every level is solvable without boosters (playtested logic)
- **No real-money pressure** — earn boosters through play, not purchase
- **Clean gem/jewel aesthetic** instead of candy — more universal, less childish
- **"Zen mode"** — infinite play with no timer, just relaxing matching
- **Indonesian batik patterns** on the gems — culturally distinctive

---

## 4. 🔢 Nomer 2048 — Number Slide Puzzle

**Original:** 2048 — 100M+ downloads, universally popular
**Genre:** Puzzle / Brain Game
**Concept:** Slide numbered tiles, merge matching ones, reach 2048.

### Pain Points
| # | Pain Point | Severity |
|---|-----------|----------|
| 1 | **Game over feels abrupt** — board fills up, instant death | HIGH |
| 2 | **No undo** — one accidental swipe ruins a 20-minute run | HIGH |
| 3 | **Boring visuals** — plain colored tiles, no personality | MEDIUM |
| 4 | **No goals beyond 2048** — once you hit it, what's next? | MEDIUM |
| 5 | **No learning system** — doesn't teach you strategy | LOW |

### Solution & Differentiation
- **3 undo charges** per game — earned back by merging high tiles
- **Visual tile evolution** — numbers have personality (1024 glows, 2048 explodes with particles)
- **Multi-tier goals** — 2048 is just the beginning, then 4096, 8192, with milestone celebrations
- **"Hint" system** — highlights best move option (optional, limited uses)
- **Indonesian Rupiah theme** — tiles look like IDR denominations (Rp 1K, Rp 5K, Rp 10K... Rp 2048K)
- **Daily puzzle** — fixed starting layout, compete on fewest moves

---

## 5. 🎲 Ular Tangga — Board Game Classic

**Original:** Ludo King / Snakes & Ladders — 500M+ downloads, huge in Indonesia (Ular Tangga is the local name)
**Genre:** Board Game / Multiplayer
**Concept:** Roll dice, climb ladders, avoid snakes. Simplest board game ever made.

### Pain Points
| # | Pain Point | Severity |
|---|-----------|----------|
| 1 | **Pure luck, no skill** — zero player agency, boring for adults | HIGH |
| 2 | **Too many ads between turns** — ruins the flow | HIGH |
| 3 | **AI opponents are braindead** — no challenge in single player | MEDIUM |
| 4 | **Boring board design** — same old grid, no visual interest | MEDIUM |
| 5 | **No customization** — can't change rules or board layout | LOW |

### Solution & Differentiation
- **Power-up system** — choose to use items (extra roll, shield from snake, sabotage opponent) adding strategy
- **Board themes** — Indonesian-themed boards (Borobudur temple, Bali rice terraces, Jakarta cityscape)
- **Smart AI** with difficulty levels — Easy/Medium/Hard with different strategies
- **"Chaos mode"** — snakes and ladders move positions every 5 turns
- **2-4 local multiplayer** on same device (pass-and-play)
- **Custom board editor** — place your own snakes and ladders
- **Minimal ads** — one banner, no interstitials

---

## Technical Stack

- **Pure HTML5 + CSS3 + JavaScript** — no frameworks, no dependencies
- **Mobile-first responsive** — works on any phone browser
- **Offline-capable** — all games work without internet
- **LocalStorage** for save data
- **CSS animations** — no heavy libraries
- **Each game = single HTML file** — zero build step

## Repository Structure

```
tom-games/
├── index.html          # Game portal / launcher
├── tahu-bulat.html     # Idle clicker
├── flappy-tap.html     # Endless flyer
├── gem-match.html      # Match-3 puzzle
├── nomer-2048.html     # Number puzzle
├── ular-tangga.html    # Board game
└── DESIGN.md           # This file
```
