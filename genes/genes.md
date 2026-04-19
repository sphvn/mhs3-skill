# Genes — MHS3

## Gene Grid Basics

- Every monstie has a **3×3 grid** (9 slots, A1–C3).
- Each gene has: **attack type** (Power/Speed/Technical) + **element** (Fire/Ice/Thunder/Water/Dragon/Non-Elem).
- Gene types: **Active** (battle skills, cost Kinship/Stamina) or **Passive** (always-on buffs).
- Gene tiers: **S (strongest) > XL > L > M** (higher tiers = stronger effects, may cost more).

## Rainbow Gene

- Wildcard — counts as ANY type and ANY element for Bingo.
- **Best placement: center slot (B2)** — intersects all 4 lines through center (both diagonals + row B + column 2).
- Enables up to 8 simultaneous Bingo lines when grid is optimized around it.

## Affinity Effects (Skill Modifier Suffixes)

Active skills display a suffix in parentheses (e.g., "Flame Claw (STR)") indicating a trade-off. Two independent affinity slots per skill.

**Affinity Effects 1 — Skill Power vs Wyvernfell vs Stamina:**

| Suffix | Effect |
|---|---|
| STR | +skill power, +stamina |
| ATK | ++skill power, ++stamina |
| SKL | +skill power, -Wyvernfell |
| CRFT | ++skill power, --Wyvernfell |
| BRK | +Wyvernfell, +stamina |
| CRSH | ++Wyvernfell, ++stamina |
| BLNT | +Wyvernfell, -skill power |
| HVY | ++Wyvernfell, --skill power |

**Affinity Effects 2 — Crit / Stamina Efficiency / Duration / Healing:**

| Suffix | Effect |
|---|---|
| STAB | +Crit Rate, +stamina |
| FLSH | ++Crit Rate, ++stamina |
| XPRT | -stamina, -skill power |
| TLNT | --stamina, --skill power |
| LONG | +duration, +stamina |
| ARC | ++duration, ++stamina |
| CURE | +HP recovery, +stamina |
| HEAL | ++HP recovery, ++stamina |

## Bingo System

A **Bingo** = three genes of the same attack type OR same element in a line.

```
A1  A2  A3
B1 [B2] B3     8 lines: 3 rows + 3 cols + 2 diagonals
C1  C2  C3
```

**Counting bingos:**
1. For each of the 8 lines, check Type match (all same P/S/T) → Type Bingo.
2. For each of the 8 lines, check Element match (all same element) → Element Bingo.
3. A single line CAN score both Type AND Element simultaneously.
4. Rainbow Gene counts as ANY for both dimensions.

**Bingo bonuses:**
- Type Bingo (3 same type): +5% damage for that attack type.
- Element Bingo (3 same element): elemental damage bonus.
- **Multiple bingos stack MULTIPLICATIVELY** (not additively). Two bingos ≠ 2×, they multiply.

For full bingo bonus data: `grep "^ELEMENT_FIRE\|^THREE_POWER" genes/bingo-bonuses.psv`.

## Rite of Channeling

- Transfer genes between monsties — **no sacrifice** (changed from MHS2).
- Rearrange genes within same monstie freely at any time.
- **Gene Search**: press L3 (controller) or V (keyboard) to browse all existing genes.
  - Press □ or F to see which species carry that gene and region.
  - Only shows genes you've obtained at least once.

## Buff Stacking Rules (Les Carnets)

- Same buff at **equal or higher tier** → **renews duration** (doesn't stack).
- Same buff at **lower tier** → **ignored** entirely.
- **Different buff types** combine **additively**.
- **Exception:** Element Atk Boost (XL) is **multiplicative** with other damage buffs.
- Some skills explicitly stack (e.g., Egg Skill Fireform: Attack Up S→M→L progressively).

### Active Buff Tiers

| Buff | S | M | L | Notes |
|---|---|---|---|---|
| Power Charge | +66% damage | +95% | +145% | Adamant Rage (Egg) = +245% |
| Attack Up | +10% | +20% | +30% | |
| Element Attack Up | +10% | +20% | +30% | |
| Critical Up | ~+5% crit | ~+10% | ~+15% | |
| Bloodrite | +30% dmg, 30% lifesteal, -20% HP/turn, 5t, 20 stam | — | — | |

## Build Principle: Balance Actives and Passives

Common mistake: filling all 9 slots with actives → burns Stamina/Kinship too fast.

- Include at least 1 active per attack type (P/S/T) so you can answer any H2H.
- Fill remaining slots with passives for sustained power.
- Consider monstie's Stamina Tendency (see [genes/builds.md](builds.md)).
- Same-name passives DO NOT stack — Critical (L) + Critical (XL) = only XL works.

## Passive Skill Values by Tier

Most passives follow a **5/10/15/20% linear scaling** (S/M/L/XL). Exact values per skill are in `skills/passive-skills.psv`. Highlights (source: MonsterBuddy):

### Offense

| Skill | Elem | Type | S | M | L | XL |
|---|---|---|---|---|---|---|
| [Elem] Atk Boost | varies | Power | +5% | +10% | +15% | **+20% (multiplicative)** |
| Non-Elem Atk Boost | Non-Elem | Power | +5% | +10% | +15% | +20% |
| Dancer | Water | Speed | +5%/-5% | +10%/-10% | +15%/-15% | +20% dmg/-20% taken (full HP) |
| All-Out | Dragon | Power | +12% | +18% | +24% | +30% (×1.2 stamina) |
| Critical | Dragon | Speed | ~+5%? | ~+8%? | ~+12%? | **+15% crit rate** |
| Salt in Wound | Non-Elem | Power | +5% | +10% | +15% | +20% vs status targets |
| Critical Kinship | Thunder | — | ? | ? | ? | **+15 Kinship per crit** |

### Stamina

| Skill | Elem | Type | XL |
|---|---|---|---|
| Stamina Surge | Thunder | Speed | **+6 recovery/turn** |
| Stamina Boost | Water | Power | **+20 starting stamina** |

### Survivability

| Skill | Elem | Type | XL |
|---|---|---|---|
| Health Boost | Non-Elem | Power | +20% HP |
| [Elem] Def Boost | varies | Tech | **−30% elem dmg** |
| All-Elem Def Boost | Non-Elem | Tech | **−10% all dmg** |
| Self-Heal | Fire | Speed | **20% max HP/turn** |
| Crit-Heal | Dragon | — | **30% max HP on crit** |
| Divine Blessing | Non-Elem | — | medium chance to halve dmg |
| Tenacity | Ice | Power | survive fatal + HP |
| Panacea | Dragon | Power | Negate abnormal statuses |

### Kinship

| Skill | XL |
|---|---|
| Soul Kinship | **×1.4 (+40% fill rate)** |
| HtH Master | **+12 Kinship per H2H win** |

### Under 50% HP (risk/reward)

| Skill | XL |
|---|---|
| Heroics | **+25% damage** |
| Vigilance | **+40% crit rate** |
| Partner | **×2.0 (+100%) Kinship gen** |

## Deep Lookup

- `grep -i "critical\|health boost" skills/passive-skills.psv` — all passives with these names
- `grep "^GENE_" genes/genes.psv` — all 268 genes with IDs
- `grep -E "^(ELEMENT|THREE)" genes/bingo-bonuses.psv` — species bingo bonus values

## See Also

- [genes/sources.md](sources.md) — gene → monstie → region farming
- [genes/builds.md](builds.md) — archetypes and stamina rotations
- [combat/combat.md](../combat/combat.md) — how bingos feed Wyvernfell + PST
