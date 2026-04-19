# Combat — MHS3

MHS3 combat is **turn-based** with prediction mechanics. You control your Rider + active monstie. AI companions act independently but can be influenced.

## Attack Type Triangle

```
Power (red)      → beats Speed     → loses to Technical
Speed (blue)     → beats Technical → loses to Power
Technical (green) → beats Power    → loses to Speed
```

Every monstie has a default attack type. Your weapon attacks also have types. Match your choice to counter the enemy's for optimal damage.

## Head-to-Head (H2H)

- Triggered when you and the enemy use the **same attack type** (both Power, both Speed, etc.)
- Winner determined by triangle: your Power vs their Technical → you win
- **Winning H2H**: reduced damage taken, charges Kinship Gauge
- **Losing H2H**: increased damage taken, no Kinship gain
- **Gold-colored attacks cannot be countered via H2H.** Bypass the system entirely — defend or use skills to mitigate, don't try to counter gold attacks.

## Double Attacks

Coordinated strike between Rider and monstie. Requires ALL three:
1. Use the **same attack type** as your monstie
2. Use a **regular attack** (not item or special skill)
3. **Win** the Head-to-Head

Double Attacks deal massive damage — often highest single-turn output. If your monstie favors Power, use Power attacks when you expect an H2H.

## Kinship Gauge

- Tear-shaped meter next to your health bar.
- Fills via: landing hits, winning H2Hs, Double Attacks (double fill rate), Synchro Rush (huge fill).
- Full gauge → **Ride your monstie** → heals monstie, boosts attack, ALL normal attacks damage the Wyvernsoul Gauge.
- Filling further while mounted → **Kinship Skills**: per-species devastating attacks.
- Kinship Attack element is **fixed per species** — gene channeling cannot change it.
- Genes like Soul Kinship (XL) boost gauge fill rate (+40%).
- Double Kinship: both party members can ride simultaneously.

## Wyvernfell

Wyvernfell is a **per-skill stat** shown alongside Power and Stamina on every Active Skill. It determines damage to the enemy's **Wyvernsoul Gauge** — it does NOT affect HP damage.

**Formula (source: Les Carnets):** Gauge damage = **Move Wyvernfell × Monstie Wyvernfell** (both percentages, multiplied).

- Move Wyvernfell range: **10–70** (only Active Skills; regular attacks = 0 except Hammer)
- Monstie base: **36–60**, plus **+5 to +15** from Bingo bonuses (species-dependent)
- Scaling is multiplicative: 84 Wyvernfell monstie deals 2× gauge damage vs 42. A 40-WF move deals 4× vs a 10.
- **Critical hits: 1.5× Wyvernsoul damage**

**What deals Wyvernfell damage:**
- Active Skills from Rider and Monstie
- Hammer basic attacks (unique — only weapon where basic attacks damage the gauge)
- ALL Monstie attacks including basic attacks
- Attacks while mounted (normal attacks deal heavy gauge damage)
- Double Attacks and Kinship Skills
- Breaking body parts contributes

**Affinity suffix effects on Wyvernfell:**

| Suffix | Wyvernfell | Tradeoff |
|---|---|---|
| BRK | +Wyvernfell | +Stamina cost |
| CRSH | ++Wyvernfell | +Stamina cost |
| BLNT | +Wyvernfell (Hammer: +15 vs base) | -Skill Power (HP damage) |
| HVY | ++Wyvernfell | -Skill Power (HP damage) |
| SKL | -Wyvernfell | +Skill Power |
| STR/ATK | No change | +Skill Power + Stamina |
| STAB/FLSH | No change | +Crit Rate |
| XPRT/TLNT | No change | -Stamina, -Skill Power |

**Wyvernfell Up buffs (increase gauge damage, 3 turns):**

| Tier | Sources |
|---|---|
| S | Composure (Egg Skill, stackable) |
| M | Storm Veil, Ice Armor / Ice Armor+, Blade Rush |
| L | Icebreaker (Egg Skill), Pump Up |

**Wyvernsoul Defense Down (reduces enemy gauge resistance, 3 turns, stackable):**
Surface Break, Dragon Blast, **Pickaxe Beak** (stackable!), Dracophage Shot, Berserk Slide+.

**Key passive:** Dragon Buster — flat **+25 Wyvernfell** stat boost. Synergizes with Pickaxe Beak.

**Best Wyvernfell monsties** (grep `monsties/monsties.psv` for live values):
- Chatacabra: 56 base + 5 bingo = **61**
- Paolumu: **60** total — Kinship Attack: 120 WF AoE
- Yian Garuga: 44 base + 15 bingo = **59** — 10% base crit (1.5× synergy)

**Best Wyvernfell move:** Pickaxe Beak — 40 WF, 15 stamina, stacks Wyvernsoul Def Down for multiplicative gains.

## Wyvernsoul Gauge & Synchro Rush

The Wyvernsoul Gauge is the bar below enemy HP — their "fighting spirit." Depleting it → vulnerability.

**Wyvernsoul Stock system** (stronger monsters):
- Red orbs (Stock) beside their gauge
- Each full depletion consumes one Stock
- Gauge turns **blue for 1 turn** → monster **Staggered** (attacks miss)
- Overflow damage carries to the next red gauge
- Deplete all Stocks → **Topple** (incapacitated, ALL attacks become guaranteed Crits)

**State flow:** Red → deplete → Stock consumed + Blue (1-turn Stagger) → resets to red (or Topple if no stocks).

**Synchro Rush:** Available ONLY after Topple. Button prompt → entire party attacks simultaneously for massive damage + **greatly fills Kinship Gauge**.
- Use when out of stamina
- Consider skipping if you have stamina — toppled monsters take guaranteed Crits from ALL skill attacks, which can outdamage Synchro Rush and let you apply status/break parts
- Skip if you need to heal/buff — monster stays toppled regardless

**Core loop:** Deplete Wyvernsoul → Topple → Synchro Rush → fill Kinship → Mount Monstie → mounted attacks deal heavy Wyvernsoul damage → repeat.

## Monster Behavior States

| State | Attack Tendency | Visual Cues |
|---|---|---|
| Normal | Balanced | Standard animations |
| Enraged | Favors Power | Roars, aggressive stance, red aura |
| Tired | Favors Technical or Speed | Slower movement, panting |

Learn per-monster patterns — recognize tells for upcoming attack types.

## Status Effects

| Status | Effect | Resolution / Cure |
|---|---|---|
| Poison / Noxious / Severe | DoT per turn (% max HP — higher tiers hit harder) | ~3 turns. Antidote / Antidote Powder (AoE+Negate) |
| Burn | DoT + **+20% damage taken** (additive) | Burn Ointment / Burnheal Powder |
| Paralysis | Each turn: **chance** to skip (probability roll) | Multi-turn. Paracare / Paraheal Powder |
| Sleep | Cannot act until hit. Wake-up hit is **guaranteed crit (1.5×)**. Free turn to heal/buff | Until damaged, or ~3 turns. Energy Drink / Awakening Powder |
| Blastblight | Delayed explosion (~3–5 turns). Can detonate early (Magma Counter, Hellfire Retribution) | Soap Scud / Cleansing Powder |
| Bleeding | **Doubles damage of next hit taken** (multiplicative, not DoT) | Sushifish (single; gives regen) |
| Darkness (Flash) | Reduces accuracy | Intuitizer / Darkheal Powder |
| Stun | Skips one turn entirely (guaranteed) | Short. Caused by Hammer skills, Sonic Bomb, traps |
| Skill Seal | Cannot use ANY skills — only P/S/T basics | Multi-turn. Zest Pill. Velkhana signature |

**Nulberry Elixir**: universal single-target status cure.

**Inflict Rate Up** (passive gene, S/M/L/XL): +chance to apply any status. Stacks with status-specific skills. **Salt in Wound (XL)**: +20% damage vs status-afflicted.

**Note:** "Exhaust" is NOT a status in MHS3 — Bow's Exhaust Coating deals Wyvernfell damage, not a status.

## Deep Lookup

For full move/skill data, grep PSVs:
- `grep -i "dragon eater" skills/active-skills.psv` — active skill stats
- `grep -i "critical" skills/passive-skills.psv` — passive skill tiers
- `grep "Storm Veil\|Pickaxe Beak\|Composure" skills/buffs-debuffs.psv` — buff/debuff details

## See Also

- [combat/weapon-mechanics.md](weapon-mechanics.md) — per-weapon-type mechanics
- [genes/genes.md](../genes/genes.md) — affinity effects and bingo
- [monsters/parts.md](../monsters/parts.md) — part-break targeting
