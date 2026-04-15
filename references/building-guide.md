# MHS3 Advanced Building Guide — Crafting the Perfect Monstie

Source methodology: Masuku (Les Carnets de la Wycadémie). This covers mechanics
the wiki glosses over — tendencies, ecosystem rank, dual element, and the full
optimization pipeline for endgame monsties.

## Building Pipeline (order of decisions)

1. **Choose species** → determines base stats, Bingo Amount Bonuses, Kinship Attack
2. **Hatch for Tendencies** → Stamina + Skill tendencies are set at hatch, permanent
3. **Ecosystem Rank (Excursions)** → stat increases, S-rank skills, dual element
4. **Environment Skills** → 3 slots from S-ranked environments
5. **Gene Channeling** → active skills, passive skills, Bingo optimization

---

## Step 1: Species Selection

Species determines four things that CANNOT be changed:
- **Base stats** (HP, Attack, Defense, etc.) — like Pokémon IVs, fixed per species
- **Bingo Amount Bonuses** — stat increases at 1, 3, and 5 total bingos (species-specific)
- **Kinship Attack** (and its element) — fixed, cannot be altered by channeling
- **Default attack genes** (less important — can be overwritten)

**Base stats matter**: Gravios is always tanky; Odogaron is always glass cannon. No amount of genes changes fundamental stat distribution.

**Bingo Amount Bonuses are species-specific and important for advanced builds:**
- 1 bingo, 3 bingos, and 5 bingos each trigger a species-specific stat increase
- Example: Palamute at 3 bingos → +3 Stamina Recovery (critical for "Child Labor" support build)
- Choose species partly based on which bingo bonuses align with your build goal

**Kinship Attack element is permanent** — if you're building around a specific element, check whether the species' Kinship Attack matches. A mismatch means your biggest move doesn't benefit from your element stacking.

---

## Step 2: Tendencies (Set at Hatch — Cannot Be Changed)

Found in the Skills page of a monstie's profile. Two independent tendencies:

### Stamina Tendency
| Tendency | Behavior | Build Implication |
|---|---|---|
| Proactive | Burns stamina aggressively, uses Second Wind when empty | Higher autonomous DPS, but you have less stamina for issuing orders |
| Average | Mixes active skills with regular attacks | Balanced stamina flow |
| Cautious | Uses Second Wind early even with stamina remaining | More stamina available for your commands, but 5 less Kinship per Second Wind. Better for high-cost skills |

### Skill Tendency
| Tendency | Behavior |
|---|---|
| Attack | Prioritizes offensive skills |
| Support | Prioritizes party buff skills |
| Hindrance | Prioritizes debuff / status skills |

**Practical advice**: For damage builds, Proactive + Attack is ideal. For support/status builds, Cautious + Support or Hindrance. You can hatch multiple eggs to roll for desired tendencies — potency doesn't matter for this since you'll replace genes anyway.

---

## Step 3: Ecosystem Rank & Excursions

### Two Separate Systems (same camp menu)
- **Habitat Restoration**: Release monsties permanently → raises zone Ecosystem Rank (B→A→S), unlocks mutations, enables dual-element eggs. See `spawn-conditions.md` for full mutation list, zone elements, and rank mechanics.
- **Excursions**: Send monstie temporarily (costs Training Talisman from Melynx Emporium) → grants individual stat bonuses and Environment Skills.

### Stat Increases via Excursions
Send a monstie to a specific ecosystem. At 3★ rank, they gain **2 stat increase slots** with these options:
| Bonus | Value |
|---|---|
| Attack | +80 |
| Defense | +80 |
| HP | +120 |
| Stamina Recovery | +5 per turn |

Use these to cover weaknesses. Example: Odogaron has terrible defense → give it +80 Defense and +120 HP to survive AoE fights.

### S-Rank Benefits (3 things)
When a monstie reaches S rank in an environment:

**1. Species S-Rank Attack Skill**
- Each species has a base attack gene and an S-rank variant with improved stats
- S-rank skills can only come from eggs hatched in an environment where the species is S-ranked
- Examples: Draconic Flurry → Draconic Flurry+ (50 → 60 Power), Night Parasites → Night Parasites+ (35 → 30 stamina cost), Poison Spike gets +10 Wyvernfell, Hell Horn gets +10 Power

**2. Environment Skills**
- Skills tied to a specific environment, outside the normal Bingo system
- Monstie auto-learns skills from its native environment at S rank
- Can learn skills from OTHER environments — but must be S-ranked there too
- **Max 3 Environment Skills** — must choose from the 6 available

| Environment | Skill Focus |
|---|---|
| Azuria | Stamina management |
| Canalta | Self-buff duration, Head-to-Head bonuses |
| Tarkuan | Kinship Gauge, Riding Gauge |
| Serathis | Buffs when losing a Heart (HP threshold) |

**Environment Skills have improved versions** triggered by specific genes in your Bingo:
- Example: Battle Thirst+ requires at least one Fire gene in your Bingo → easier on Fire monsties

**3. Dual Element (see below)**

---

## Step 4: Dual Element System

If your monstie is S-ranked in an area, it gains **that area's element** as a second element. This changes its appearance and alters combat properties.

### Elemental Damage Penalty
- Using a move of an element your monstie **doesn't have** → **10% damage reduction** (source: Les Carnets updated guide)
- Gaining the corresponding element via dual element **negates this penalty entirely**
- A Fire-element Ebony Odogaron deals the same Fire damage as a native Fire monstie (e.g., Dreadking Rathalos) with equivalent Attack stat

### No Offensive Benefit to Single Element
- A Fire Ebony Odogaron deals equal damage with Dragon moves as a pure Dragon Ebony Odogaron (both having double Dragon element)
- **Going dual element has no direct offensive downside** for the added element

### Elemental Resistance Changes
Dual element CAN alter a monstie's elemental weaknesses. This is species-specific and doesn't follow a universal rule. Multipliers:
| Resistance Level | Damage Taken |
|---|---|
| Extra weak | 150% |
| Weak | 125% |
| Neutral | 100% |
| Resistant | 90% |
| Highly resistant | 70% |

Example: Ebony Odogaron going dual element lowers its resistance to Fire, Water, Thunder, and Ice (originally neutral on all).

### Dual Element Trade-Off for Bingo
- Since Kinship Attack element is fixed, you may need TWO different elements in your Bingo grid
- This splits your elemental Bingo lines, reducing total elemental bonuses
- Evaluate whether the dual element damage access outweighs the Bingo dilution

---

## Step 5: Gene Optimization

### Priority Order for Gene Slots
1. **One active attack per type (P/S/T)** — ensures you can answer any H2H
2. **Rainbow Gene in center (B2)** — maximum Bingo coverage
3. **Core passives aligned with build** — see genes-and-builds.md for full table
4. **Bingo optimization** — arrange remaining genes to maximize type/element lines

### Stamina-Aware Skill Selection
- Match skill costs to your monstie's Stamina Tendency
- Proactive monsties burn stamina fast → lower-cost skills or Stamina Surge gene
- Cautious monsties conserve → can afford higher-cost skills
- Consider Stamina Recovery stat increase from Excursions

### Obtaining High-Tier Passive Genes
- **Egg potency matters here**: Highly Potent eggs have better odds for XL passives
- Higher potency → more genes + higher gene tiers at hatch
- **Paintball farming**: Use paintball on target monster, defeat it, collect 2 eggs from retreat nest
- Defeat the monster again in the nest to skip Rudy's dialogue

### Passive Stacking Rule
- **Same-name passives do NOT stack** — only the highest tier applies
- Critical (L) + Critical (XL) → only Critical (XL) works; the (L) is a dead slot
- Use the dead slot for a Bingo-contributing gene instead

---

## Build Archetypes

### Glass Cannon
- Species: Odogaron, Boltreaver Astalos, Rajang
- Passives: All-Out (XL), Critical (XL), [Element] Atk Boost (XL)
- Excursion bonuses: Attack +80, Stamina Recovery +5
- Risk: low survivability — consider Tenacity (M) as insurance

### Tank / Sustain
- Species: Dreadqueen Rathian, Gammoth, Gravios
- Passives: Health Boost (XL), All-Elem Def Boost (XL), Self-Heal (XL), Divine Blessing (XL)
- Excursion bonuses: HP +120, Defense +80

### Crit-Kinship Engine
- Species: Ruiner Nergigante, Zinogre, Magnamalo
- Passives: Critical (XL), Soul Kinship (XL), Critical Kinship (XL)
- Loop: crits fill Kinship → Kinship Skills → repeat

### Wyvernsoul Topple (maximize gauge depletion → Topple → Synchro Rush loop)
- Species: Chatacabra (61 WF), Paolumu (60 WF, 120 WF Kinship AoE), Yian Garuga (59 WF, 10% base crit)
- Passives: Dragon Buster (+25 Wyvernfell), Critical (XL) (+15% crit = 1.5x WF damage), All-Out (XL)
- Key moves: Pickaxe Beak (40 WF, 15 stamina, stacks Wyvernsoul Def Down), Dracophage Shot (Wyvernsoul Def Down)
- Weapons: Yeti Hammer (HVY Perfect Strike), Spongia Bow (highest WF + Exhaust Coating), Veldian Sibilus HH (party Wyvernfell Up)
- Armor: Goss Harag (Dragon Buster L), Diablos Nero (Dragon Buster M + Slugger)
- Loop: Stack Wyvernsoul Def Down → deplete gauge → Topple → Synchro Rush (fills Kinship) → mount → repeat
- See `combat-weapons.md` for full Wyvernfell formula and buff/debuff sources

### Status Disruptor
- Species: Purple Gypceros, Dreadqueen Rathian, Bishaten
- Passives: Inflict Rate Up (XL), Salt in the Wound (XL)
- Active skills: variety of status moves (Poison, Para, Sleep)
- Bishaten's Kinship Attack (Fruit Barrage) inflicts multiple statuses → gear toward status build

### Support / "Child Labor" Palamute

**Species:** Canyne (Palamute) — Speed / Non-Elem / Rank 5 / Fanged Beast / Canalta (Blessing Hill)
**Obtained:** Chapter 13 ("Ward") — defeat Invasive Arzuros at Blessing Hill, collect egg from Endangered Den.

**Stats:** Very high Speed (9 trend), solid Defense, mediocre Attack (5) and Crit (1). NOT a damage dealer — pure support.
**Riding actions:** Jump, Wall Climb, Roar, Melee Attack, **Ground Dive** (unique — access underground passages). Also has Wall Climb, making it the best exploration monstie.
**Kinship Attack:** Rising Axel — Non-Elem single-target damage.

**Unique genes (Canyne-exclusive):**
- **Art of Raw Power**: Non-Elem Attack Up buff to self (20 stamina)
- **Art of Friendship** (Lv30): Grants Regenerate to ALL allies (20 stamina) — key support skill
- **Art of Striking**: Non-Elem damage, increases on repeated use

**Core build strategy:** Cycle between healing allies, recovering stamina, and dodging damage.
- **Nourishing Pinecones** (from Blood Orange Bishaten, Tarkuan): 0 stamina cost, recovers own stamina
- **White Shadow** (from Silverwind Nargacuga, habitat mutation): 80 stamina, 2-turn full evasion
- **Art of Friendship**: Party Regenerate
- Passives: Stamina Surge (XL) +6 recovery/turn, Stamina Boost (XL) +20 starting stamina
- Excursion bonus: Stamina Recovery +5 (Canalta)
- 3-bingo bonus: +3 Stamina Recovery
- **Tendency: Cautious** (more stamina control for ordered skills)

**Total stamina engine:** Base recovery + Stamina Surge XL (+6) + bingo bonus (+3) + excursion (+5) = massive per-turn recovery. Nourishing Pinecones costs 0 and recovers more on top.

**vs other Speed/Non-Elem options:** Canyne doesn't compete on damage. Nargacuga/Odogaron/Seregios are better DPS. Canyne is the only dedicated support monstie in Speed/Non-Elem, with unmatched stamina cycling and party sustain via Art of Friendship.
