# 🐉 CRYSTAL DRAGONS — Game Design Document
### Version 1.1 | Working Title | Genre: Idle Collection / Simulator

> ⚠️ "Crystal Dragons" is a working title — a catchier, more searchable name TBD before launch.

---

## 1. GAME OVERVIEW

### One-Sentence Pitch
> Equip a team of chibi dragons, send them to mine giant crystals, level up your
> keeper to power your whole team, chase Cosmic-tier legendaries, and rebirth
> endlessly — competing on global leaderboards for real prizes.

### The Fantasy
You're a Dragon Keeper. Your adorable chibi dragons follow you around; you deploy
them to attack giant crystals for treasure. Collect their loot, level up, hatch
rarer dragons, break tougher crystals, and build the ultimate collection.

### Target Audience
- Roblox players who love idle/simulator/pet games (Pet Sim, Grow a Garden fans)
- Mostly MOBILE players, skewing younger — mobile-first design is mandatory
- Motivated by: collection, progression, status/flex, competition

### Core Pillars
1. Satisfying idle-strategy loop (deploy → collect → redeploy)
2. Meaningful rarity chase (rarity drives power, pouch, earnings, level cap + variants)
3. Endless progression (main-level + rebirth treadmill + worlds)
4. Social & competitive (gifting, leaderboards, Season 1 competition)
5. Charm & flex (funny chibi dragons, show-off cosmetics)

---

## 2. CORE GAMEPLAY LOOP

```
EQUIP up to 5 chibi dragons (they follow you)
   |
SEND them to attack GIANT CRYSTALS in the world
   |
Dragons AUTO-EARN Coins -> fill POUCHES (capacity by rarity)
   |  [While waiting: tap-boost, smash bonus crystals, hatch eggs, level up]
POUCH FULL -> dragon stops -> COLLECT -> REDEPLOY
   |
Spend Coins -> buy EGGS -> hatch DRAGONS (PERMANENT)
   |
Earn Essence -> LEVEL UP MAIN CHARACTER -> all dragons level up (capped by rarity)
   |
Stronger dragons -> break POWER-GATED crystals + bigger pouches + more earnings
   |
Progress walls -> REBIRTH (keep dragons/essence/level, reset coins/eggs)
   |
+10-15% permanent boost + milestone unlocks -> re-grind faster -> next WORLD -> ENDLESS
```

Session rhythm: pouches fill quickly early (~30–90s) → frequent collect/redeploy.
Later: bigger pouches + auto-collect shift toward relaxed idle.

---

## 3. THE DRAGONS

### Chibi Design
- Cute chibi dragons that follow the player
- Funny, memeable names/personalities (e.g., "Sir Burnsalot," "Chonky Wyrm," "Lil Void")
- Highly shareable / screenshot-worthy

### Every Dragon Has 4 Attributes (scale with rarity)
| Attribute | What it does |
|---|---|
| Attack Power | Which crystals it can damage + earn speed |
| Pouch Capacity | How much it holds before you must collect |
| Earn Rate | Coins per second while attacking |
| Max Level Cap | How high it can be leveled (via main level) |

### Rarity Tiers & Hatch Odds
| Rarity | Drop % | Relative Stats | Max Level Cap |
|---|---|---|---|
| Common | 55% | Baseline | 10 |
| Rare | 28% | ~2.5x | 25 |
| Epic | 12% | ~6x | 50 |
| Legendary | 4% | ~15x | 75 |
| Mythic | 1% | ~40x | 100 |

(Exact caps tuned in Economy Spreadsheet.)

### Variants (flex + content multiplier — recolor same model)
| Variant | Chance | Stat Multiplier | Look |
|---|---|---|---|
| Normal | Default | 1x | Base |
| ✨ Golden | 1 in 40 | 3x | Gold shader |
| 🌈 Rainbow | 1 in 200 | 8x | Animated rainbow |
| 🌑 Dark/Void | 1 in 1,000 | 20x | Black + purple glow |
| 🌌 Cosmic | 1 in 5,000 | 50x | Galaxy/starfield |
| ⚡ Secret | 1 in 25,000+ | 100x+ | Unique FX |

### Roster Size (v1)
- ~24 base dragons × 6 variants = ~144 collectibles (only 24 models to make)
- Event/exclusive dragons added post-launch

---

## 4. CRYSTALS & WORLDS

### Giant Crystals
- Multiple per world; INFINITE (always attackable) in v1
- POWER-GATED: tougher crystals need higher total Attack Power → soft gate + rarity chase

### Breakable Bonus Crystals (v1)
- Periodically spawn with HP; players focus dragons + tap to break
- Drop bonus loot (rare essence, potions, coin bursts) → active "events"

### Worlds (Rooms) — start with 2
| World | Unlock | Theme | Crystals |
|---|---|---|---|
| 🏰 Dragon Valley | Free | Grassy starter | Low power |
| 🌋 Ember Peaks | 500K coins | Volcanic | High power |
| (v2: Frost, Sky, Void) | | | |

---

## 5. POUCH & OFFLINE JAR (signature mechanic)

### Pouches (active)
- Each equipped dragon has a pouch (capacity = rarity)
- Fills as they attack; when FULL, dragon STOPS earning
- Player COLLECTS to bank coins + redeploy
- Auto-Collect gamepass auto-empties (convenience monetization)

### Offline Jar (idle)
- Offline, dragons drop earnings into the Offline Jar (capacity-limited)
- Upgradeable / purchasable / enhanceable → bigger jar = log out longer
- Player-friendly convenience (NOT pay-to-win)

---

## 6. CURRENCIES & ECONOMY

| Currency | Earned From | Spent On |
|---|---|---|
| Coins | Dragons mining crystals (pouches/jar) | Eggs, world unlocks, equip slots |
| Essence | Passive from dragons + bonus crystals | MAIN CHARACTER LEVELS, offline jar upgrades |

### Cost Curves (exponential)
- Eggs ~triple per tier: 100 -> 500 -> 2,500 -> 12,000 -> 60,000 -> [W2] 300K -> ... -> 50M
- Main level essence cost rises per level (steep)

(Exact numbers in Economy Spreadsheet.)

---

## 7. MAIN CHARACTER LEVEL & DRAGON LEVELING (core progression)

- Spend ESSENCE to level up your MAIN CHARACTER (keeper)
- Each main level → ALL owned dragons level up in sync
- Each dragon has a MAX LEVEL CAP based on rarity/breed
- When a dragon hits its cap, it stops scaling → pressure to get higher-rarity dragons
- Power = Main Level × each dragon's capped stats

Three stacking progression layers:
| Layer | Driven by | Feels like |
|---|---|---|
| Collection | Hatching eggs | "Get them all + rarer" |
| Power | Main level (essence) | "Getting stronger" |
| Prestige | Rebirth | "Ascending, endless" |

(Fusion/evolution of capped dragons = v2 idea.)

---

## 8. REBIRTH (endless engine)

### On Rebirth
| Element | Reset? |
|---|---|
| Coins | ✅ Reset |
| Unhatched eggs / progress | ✅ Reset (may convert to coins) |
| DRAGONS (collection) | ❌ NEVER lost |
| Essence | ❌ Kept |
| Main character level | ❌ Kept |

### Gains
- +10–15% ADDITIVE permanent multiplier per rebirth (tunable; NOT compounding)
- Milestone unlocks every 5 rebirths (new world/dragon/feature)
- Rebirth count = leaderboard status flex

### Requirement scales up
```
Rebirth 1: 100K coins (~30–45 min)
Rebirth 2: 500K   Rebirth 3: 2M   Rebirth 5: 50M
Each ~5x the last -> endless
```

Rebirth = ascending (keep collection), re-grind faster, reach further.

---

## 9. EQUIP / TEAM SYSTEM
- 5 equip slots default (only equipped dragons earn)
- Expand via daily login + purchasable add-ons
- "Which 5 do I equip?" strategic decision
- Unequipped dragons stored in collection

---

## 10. SOCIAL & CO-OP (v1: Gifting Only)
- Gifting: send potions/items to friends (one-way, safer anti-cheat)
- Potions: Luck, 2x Coin, 2x Essence, XP boost
- Online-time rewards: stay online → earn potions
- (Full trading = v2 after anti-cheat proven)

---

## 11. GOALS & RETENTION SYSTEMS
- Collection Dex (all dragons/variants — "collect them all")
- Tutorial/onboarding (4-step guided start)
- Daily rewards / login streak (return hook + slots)
- Codes system (YouTuber virality)
- Light quests ("break 5 bonus crystals," "reach Rebirth 3")

---

## 12. LEADERBOARDS & SEASON 1 COMPETITION

### Three Leaderboards
1. Most Rebirths (grinders)
2. Rarest Collection / Most Dragons (collectors)
3. Total Power (combined — main comp metric, hardest to cheese)

### Season 1 (LEGAL — gift cards, achievement-based, ranked by Total Power)
| Rank | Prize |
|---|---|
| 🥇 #1 | ₹2,000 gift card + Champion dragon + permanent title |
| 🥈 #2 | ₹1,500 gift card + exclusive dragon |
| 🥉 #3 | ₹1,000 gift card + exclusive dragon |
| #4–5 | ₹500 gift card + limited skin |
| #6–10 | ₹300 gift card + limited skin |
| #11–50 | Exclusive in-game dragon/badge |
| First to Mythic | ₹500 gift card + dragon named after them |

Rules: ✅ Skill-based (not luck) ✅ Gift cards NOT Robux (Robux giveaways BANNED)
✅ Referrals give in-game rewards only, decoupled from prizes ✅ Written rules ⚠️ Check local laws.

---

## 13. MONETIZATION (Light + Flex, No Pay-to-Win)
| Item | Type | Price (R$) |
|---|---|---|
| Auto-Hatch | Gamepass | 299 |
| Auto-Collect | Gamepass | 399 |
| VIP (chat tag, area, small boost) | Gamepass | 499 |
| 2x Coins (permanent) | Gamepass | 499 |
| Extra Equip Slots | Gamepass | 399 |
| Bigger Offline Jar | Gamepass | 349 |
| Flex Cosmetics (trails, name glow, skins) | Gamepass | 799–1,499 |
| Temp Boosts | Dev Product | 49–149 |
| Coin Packs | Dev Product | 99–2,000 |

Flex cosmetics = high-priced, zero gameplay advantage.

---

## 14. ANTI-CHEAT (Mandatory — Every System Server-Side)
- ALL logic server-side: currency, pouches, jar, levels, leaderboards, rebirth
- Server calcs earn rate × time, caps at pouch/jar capacity
- Validate every collect/hatch/level/rebirth event
- Rate-limiting + sanity checks (impossible jumps flagged)
- Account age 30+ days for competition eligibility
- One prize per account/IP; manual audit of top winners
- Blacklist + ban exploiters; promote next legit player

⚠️ Anti-cheat is AI's weakest area — spend best AI-tool time here + stress-test.

---

## 15. ART, SOUND & UX
- Funny/cute chibi dragons, colorful worlds
- Juicy feedback: flying coins, popping numbers, sparkles, crit bursts, SFX
- Upbeat music + punchy SFX (cheap, huge game-feel impact)
- Mobile-first UI (every screen works on small touchscreens)
- Accessibility: mute, low-graphics toggle

---

## 16. SCOPE: V1 vs FUTURE
| System | V1 | V2+ |
|---|---|---|
| Core deploy-collect loop | ✅ | |
| 2 worlds | ✅ | +3 worlds |
| 24 dragons + 6 variants | ✅ | +event dragons |
| Pouch + Offline Jar | ✅ | |
| Main level + dragon caps | ✅ | Fusion/evolution |
| Rebirth (endless) | ✅ | |
| Gifting + potions | ✅ | Full trading |
| Dex, tutorial, dailies, codes, quests | ✅ | |
| 3 leaderboards + Season 1 | ✅ | Seasons 2+ |
| Light monetization + flex cosmetics | ✅ | more cosmetics |
| Anti-cheat + mobile-first | ✅ | |

---

## 17. SUCCESS METRICS (Honest)
- Ship a working game: ~90%
- Day-1 retention 20%+: the gate before spending marketing
- Real traction (100–500+ CCU, some revenue): ~30–40%
- Viral hit: ~5% (normal — not failure if it doesn't happen)
- True success = shipping a real game + learning the pipeline. A hit is the bonus.

---

## 18. BUILD & TOOLS SUMMARY
- AI: GitHub Copilot (free) + Roblox Assistant (free) + Claude (~₹1,700/mo for hard systems)
- Art: Roblox AI/Meshy for dragons; Midjourney/Leonardo for icon+thumbnail
- You = Director: define systems, prompt AI, test, iterate
- Timeline: ~8–10 weeks (learn Studio → core → progression → social → polish → soft launch → marketing)
- Budget: ~₹5k build / ₹15–20k marketing+competition (separate)

---

## CHANGELOG
- v1.1: Rebirth reworked (+10-15% additive, milestone unlocks; dragons NEVER lost).
        Added Main Character Level system (essence -> level -> all dragons level, rarity-capped).
- v1.0: Initial full design.

## END OF DOCUMENT
