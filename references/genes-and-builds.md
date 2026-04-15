# MHS3 Genes & Builds Reference

## Gene Grid Basics
- Every monstie has a **3×3 gene grid** (9 slots, labeled A1-C3)
- Each gene has: **attack type** (Power/Speed/Technical) + **element** (Fire/Ice/Thunder/Water/Dragon/Non-Elem)
- Gene types: **Active** (battle skills, cost Kinship/Stamina) or **Passive** (always-on buffs)
- Gene tiers: S (strongest) > XL > L > M (higher tiers = stronger effects, may cost more)

## Affinity Effects (Skill Modifier Suffixes)

Active skills display a suffix in parentheses (e.g., "Flame Claw (STR)") indicating a trade-off modifier. Two independent affinity slots exist per skill.

### Affinity Effects 1 — Skill Power vs Wyvernfell vs Stamina
| Suffix | Effect |
|---|---|
| STR | Increases skill power, increases Stamina consumed |
| ATK | **Greatly** increases skill power, **greatly** increases Stamina consumed |
| SKL | Increases skill power, reduces Wyvernfell power |
| CRFT | **Greatly** increases skill power, **greatly** reduces Wyvernfell power |
| BRK | Increases Wyvernfell power, increases Stamina consumed |
| CRSH | **Greatly** increases Wyvernfell power, **greatly** increases Stamina consumed |
| BLNT | Increases Wyvernfell power, reduces skill power |
| HVY | **Greatly** increases Wyvernfell power, **greatly** reduces skill power |

### Affinity Effects 2 — Crit / Stamina Efficiency / Duration / Healing
| Suffix | Effect |
|---|---|
| STAB | Increases Crit Rate, increases Stamina consumed |
| FLSH | **Greatly** increases Crit Rate, **greatly** increases Stamina consumed |
| XPRT | Reduces Stamina consumed, reduces skill power |
| TLNT | **Greatly** reduces Stamina consumed, **greatly** reduces skill power |
| LONG | Increases effect duration, increases Stamina consumed |
| ARC | **Greatly** increases effect duration, **greatly** increases Stamina consumed |
| CURE | Increases HP recovery, increases Stamina consumed |
| HEAL | **Greatly** increases HP recovery, **greatly** increases Stamina consumed |

**Key pattern**: Every affinity is a trade-off. "Greatly" variants are stronger in both directions. When evaluating skills, check both affinity slots — a skill with (ATK, FLSH) hits extremely hard with high crit but costs massive stamina.

## Bingo System
A **Bingo** = three genes of the same attack type OR same element forming a line on the grid.

**Grid layout:**
```
A1  A2  A3     Horizontal lines: rows A, B, C
B1 [B2] B3     Vertical lines: columns 1, 2, 3
C1  C2  C3     Diagonal lines: A1-B2-C3, A3-B2-C1
```
**8 possible Bingo lines total** (3 horizontal + 3 vertical + 2 diagonal).

**Counting bingos — check ALL 8 lines for BOTH dimensions:**
1. For each of the 8 lines, check: do all 3 genes share the same **Type**? → Type Bingo
2. For each of the 8 lines, check: do all 3 genes share the same **Element**? → Element Bingo
3. A single line CAN score both a Type Bingo AND an Element Bingo simultaneously
4. Rainbow Gene counts as ANY type and ANY element for matching
5. Count Type bingos and Element bingos separately — both contribute to total

**Bingo bonuses:**
- Type Bingo (3 Power in a row): +5% damage for that attack type
- Element Bingo (3 Fire in a row): elemental damage bonus
- **Critical MHS3 change: Multiple Bingos stack MULTIPLICATIVELY** (not additively)
  - Two bingos don't just add — they multiply, making optimal placement crucial

**Species Bingo Amount Bonuses:**
- Completing 1, 3, or 5 total bingos grants species-specific stat increases
- These bonuses vary per species (e.g., Palamute at 3 bingos gets +3 Stamina Recovery)
- This is a key factor in species selection for advanced builds

## Rainbow Gene
- Wildcard — counts as ANY type and ANY element for Bingo
- **Best placement: center slot (B2)** — intersects all 4 lines through center (both diagonals + row B + column 2)
- Enables up to 8 simultaneous Bingo lines when grid is optimized around it
- Most top builds use Rainbow Gene at B2

## Rite of Channeling
- Transfer genes between monsties — **no sacrifice required** (changed from MHS2)
- Rearrange genes within same monstie freely at any time
- **Gene Search**: press L3 (controller) or V (keyboard) to browse all existing genes
  - Press □ or F to see which species carry that gene and in which environment
  - Only shows genes you've obtained at least once
- Complete gene list spreadsheet: `docs.google.com/spreadsheets/d/1UqLviLsplDUugTIWiC5drsJnf-XbkZU62QGQNadgSfA`

## Key Build Principle: Balance Actives and Passives
- **Common mistake**: filling all 9 slots with active attacks → burns Stamina/Kinship too fast
- Include at least 1 active per attack type (P/S/T) so you can answer any Head-to-Head
- Fill remaining slots with passives for sustained power
- Consider monstie's Stamina Tendency when choosing skill costs (see building-guide.md)

## Buff Stacking Rules (source: Les Carnets)
- Same buff at **equal or higher tier** → **renews duration** (does not stack)
- Same buff at **lower tier** → **ignored** entirely (higher tier persists)
- **Different buff types** combine **additively** (e.g., Attack Up + Element Atk Boost)
- **Exception**: Element Atk Boost (XL) is **multiplicative** with other damage buffs
- Some skills explicitly stack (e.g., Egg Skill Fireform: Attack Up S→M→L progressively)

### Active Buff Tiers (from Les Carnets)
| Buff | S | M | L | Notes |
|---|---|---|---|---|
| Power Charge | +66% damage | +95% | +145% | Egg Skill Adamant Rage = 245% |
| Attack Up | +10% | +20% | +30% | |
| Element Attack Up | +10% | +20% | +30% | |
| Critical Up | ~+5% crit | ~+10% | ~+15% | |
| Bloodrite | +30% damage, 30% lifesteal, -20% HP/turn | — | — | 5 turns, 20 stamina |

---

## Passive Skill Values by Tier (source: MonsterBuddy.app)

Most passives follow a **5/10/15/20% linear scaling** (S/M/L/XL). This pattern is confirmed for the skills below. Skills where only XL is verified are marked — lower tiers likely follow the same pattern but are unconfirmed.

**Use these numbers for build trade-offs:** A type bingo gives +5% multiplicative damage. So swapping a gene that breaks a bingo is worth it if the new passive gives ≥5% benefit to compensate.

### Offense
| Skill | Elem | Type | S | M | L | XL |
|---|---|---|---|---|---|---|
| [Elem] Atk Boost | varies | Power | +5% | +10% | +15% | **+20% (multiplicative)** |
| Non-Elem Atk Boost | Non-Elem | Power | +5% | +10% | +15% | +20% |
| Dancer | Water | Speed | +5%/−5% | +10%/−10% | +15%/−15% | +20% dmg/−20% taken (full HP) |
| All-Out | Dragon | Power | +12% dmg | +18% | +24% | +30% (stamina ×1.2 at all tiers) |
| Critical | Dragon | Speed | ~+5%? | ~+7-10%? | ~+10-12%? | **+15% crit rate** |
| Salt in Wound | Non-Elem | Power | +5% | +10% | +15% | +20% vs status targets |
| Critical Kinship | Thunder | — | ? | ? | ? | **+15 Kinship per crit** |

### Stamina
| Skill | Elem | Type | S | M | L | XL |
|---|---|---|---|---|---|---|
| Stamina Surge | Thunder | Speed | ? | ? | ? | **+6 recovery/turn** |
| Stamina Boost | Water | Power | ? | ? | ? | **+20 starting stamina** |

### Survivability
| Skill | Elem | Type | S | M | L | XL |
|---|---|---|---|---|---|---|
| Health Boost | Non-Elem | Power | +5% HP | +10% | +15% | +20% |
| [Elem] Def Boost | varies | Tech | ? | ? | ? | **−30% elem dmg** |
| All-Elem Def Boost | Non-Elem | Tech | ? | ? | ? | **−10% all dmg** |
| Self-Heal | Fire | Speed | slight | small | decent | **20% max HP/turn** |
| Crit-Heal | Dragon | — | ? | ? | ? | **30% max HP on crit** |
| Divine Blessing | Non-Elem | — | minuscule | slight | low | medium chance to halve dmg |
| Tenacity | Ice | Power | survive fatal +slight HP | +some HP | +decent HP | (no XL) |
| Panacea | Dragon | Power | — | — | — | Negate abnormal statuses |

### Kinship Gauge
| Skill | Elem | Type | S | M | L | XL |
|---|---|---|---|---|---|---|
| Soul Kinship | Non-Elem | Power | ? | ? | ? | **×1.4 (+40%)** |
| HtH Master | Ice | Tech | ? | ? | ? | **+12 Kinship per H2H** |

### Status
| Skill | Elem | Type | Effect |
|---|---|---|---|
| Inflict Rate Up | Non-Elem | — | Increases status infliction (no exact % published) |

### Under 50% HP (risk/reward)
| Skill | Elem | Type | S | M | L | XL |
|---|---|---|---|---|---|---|
| Heroics | Fire | Power | ? | ? | ? | **+25% damage** |
| Vigilance | Ice | Tech | ? | ? | ? | **+40% crit rate** |
| Partner | Thunder | — | ? | ? | ? | **×2.0 (+100%) Kinship gen** |

**Important**: Passive genes with the SAME NAME do not stack. Using both Critical (L) and Critical (XL) wastes a slot — only the highest applies.

---

## Build Templates (S-Tier Monsties)

### Dreadqueen Rathian — Status Pressure (PvE/PvP)
- **Role**: AoE poison + burn, highest HP in game, Speed/Fire
- **Core genes**: Noxious Poison skills, Burn AoE, Soul Kinship (XL)
- **Passives**: Venom Attack (XL), Burn Attack (XL)
- **Bingo target**: Speed-type lines + Fire element lines
- **Farm**: Rathian / Dreadqueen dens in Azuria

### Boltreaver Astalos — Crit Feedback Loop
- **Role**: Burst damage, Technical/Thunder
- **Core genes**: Crit-boosting actives, Thunder skills
- **Passives**: Critical Eye (XL), Thunder Attack (XL), Thunder Boost
- **Bingo target**: Technical-type + Thunder element
- **Synergy**: Bonus damage on HtH wins and vs paralyzed targets
- **Farm**: Astalos / Boltreaver dens in Azuria/Canalta

### Ruiner Nergigante — Crit-Kinship Engine (PvE)
- **Role**: Self-sustaining DPS, Power/Dragon
- **Core genes**: Ruinous Strike, Dragon skills
- **Passives**: Critical Eye (XL), Soul Kinship (XL), Dragon Attack (XL)
- **Bingo target**: Power-type + Dragon element
- **Synergy**: Crits fill Kinship → Kinship Skills deal massive damage → repeat
- **Farm**: High-rank dens, post-game

### Velkhana — Skill Seal Control (PvP)
- **Role**: Lock opponent skills, Technical/Ice
- **Core genes**: Skill Seal skills, Ice attacks
- **Passives**: Ice Attack (XL), defensive options for mirror matches
- **Bingo target**: Technical-type + Ice element
- **Note**: Less optimal for PvE (Skill Seal has limited value vs AI)
- **Farm**: High-rank Ice region dens, post-game

### Purple Gypceros — Status Stacking (PvP niche)
- **Role**: Multi-status disruptor (Poison/Paralysis/Sleep/Flash)
- **Passives**: Inflict Rate Up, Soul Kinship (XL)
- **Bingo target**: Technical-type
- **Farm**: Early-mid game regions (Azuria/Canalta)

---

## Gene Farming Quick Reference

| Gene | Found On | Region |
|---|---|---|
| Critical Eye | Nargacuga, Zinogre, Silverwind Nargacuga, Dreadking Rathalos | Ca, Ca, Ca, Ca |
| Soul Kinship (XL) | Deviant monsties (Dreadqueen, Boltreaver, Silverwind, etc.) | varies |
| Noxious Poison | Dreadqueen Rathian | Az |
| Bloodblight (XL) | Malzeno | Se |
| Skill Seal (XL) | Velkhana | PG |
| Solar Cry | Dreadqueen Rathian, Boltreaver Astalos | Az, Az |
| Thunder genes | Astalos, Zinogre, Lagiacrus, Thunderlord Zinogre | Az, Ca, Az, Ta |
| Ice genes | Legiana, Barioth, Velkhana, Aurora Somnacanth | Ca, Se, PG, Ca |
| Dragon genes | Deviljho, Magnamalo, Gore Magala, Malzeno, Nergigante | Ca, Se, Ca, Se, PG |
| Fire genes | Rathalos, Glavenus, Anjanath, Teostra, Dreadking Rathalos | Az, Ta, Az, PG, Ca |
| Water genes | Mizutsune, Namielle, Royal Ludroth | Az, PG, Az |

For the full gene → monstie → region mapping, see `gene-sources.md`.
