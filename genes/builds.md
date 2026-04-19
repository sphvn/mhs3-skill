# Build Archetypes & Stamina Rotations — MHS3

## Building Pipeline (order of decisions)

1. **Choose species** — determines base stats, Bingo Amount Bonuses, Kinship Attack.
2. **Hatch for Tendencies** — Stamina + Skill tendencies set at hatch, permanent.
3. **Ecosystem Rank (Excursions)** — stat increases, S-rank skills, dual element. See [excursions/excursions.md](../excursions/excursions.md).
4. **Environment Skills** — 3 slots from S-ranked environments.
5. **Gene Channeling** — active skills, passive skills, Bingo optimization.

## Tendencies (Set at Hatch — Cannot Be Changed)

### Stamina Tendency

| Tendency | Behavior | Build Implication |
|---|---|---|
| **Proactive** | Burns stamina aggressively, uses Second Wind when empty | Higher autonomous DPS, less stamina for your orders |
| **Average** | Mixes active skills with regular attacks | Balanced flow |
| **Cautious** | Uses Second Wind early even with stamina remaining | More stamina for your commands, but 5 less Kinship per Second Wind. Good for high-cost skills |

### Skill Tendency

| Tendency | Behavior |
|---|---|
| **Attack** | Prioritizes offensive skills |
| **Support** | Prioritizes party buff skills |
| **Hindrance** | Prioritizes debuff / status skills |

Hatch multiple eggs to roll for desired tendencies — potency doesn't matter since you'll replace genes anyway.

---

## Stamina Archetypes & Rotations

Source: [Reddit stamina guide by TheMobDylan](https://www.reddit.com/r/MonsterHunterStories/comments/1sobnlk/guideresource_a_basic_stamina_guide_for_mhs3/).

Every monstie fits one of three base stamina archetypes:

| Archetype | Stam Regen | Starting Stam | Playstyle |
|---|---|---|---|
| **Burst** | 4 | 70 | High starting pool, burst damage/utility |
| **Balanced** | 8 | 50 | Mixed, most flexible |
| **Sustain** | 12 | 30 | Low pool, high regen, consistent rotations |

**Key fact**: Monsties not on the field regen their Stamina up to their Starting Stamina while waiting; they still use their Stamina Regen per turn.

### Universal Stamina Regen Sources

1. **Stamina Habitat Boost** — +5 regen on Environments ranked at 3 Stars.
2. **Stamina Surge (XL)** — +6 regen from Zinogre's gene (**does not show on stat sheet**).
3. **Species Bingo Bonus** — +2, +3, or +4 regen on some species (grep `genes/bingo-bonuses.psv`).
4. **Stamina Regen Up Buff** — +3 regen from items or Hunting Horn's Militant March.

**Every monstie can hit ≥15 Stamina Regen** using just (1) + (2).

### Universal Starting Stamina Sources

1. **Stamina Boost (XL)** — +20 starting stamina from Plesioth line, Namielle, Royal Ludroth.
2. **Species Bingo Bonus** — +10 or +15 starting stamina on some species.

### Stamina Regen Breakpoints → Rotations

Major breakpoints every 5 stamina enable spamming a higher-cost move indefinitely.

| Regen | Tier | Example Rotations |
|---|---|---|
| ≤9 | Major | Burst build, hoard stamina for big plays |
| 10–11 | Major | (10 repeat), (0, 20 repeat) |
| 12 | Minor | (10, 10, 15 repeat) |
| 13 | Minor | (10, 15 repeat) — e.g., Venom → Omni Chaser early game |
| 14 | Minor | (10, 10, 20 repeat) |
| 15–16 | Major | (15 repeat), (10, 20), (0, 30), (10, 10, 25) |
| 17 | Minor | (10, 10, 30 repeat) |
| 18 | Minor | (15, 20 repeat) |
| 19 | Minor | (10, 10, 35), (15, 15, 25), (15, 20, 20) |
| 20–21 | **Major** | (20 repeat), (15, 25), (10, 30), (10, 10, 40) — **strongest tier**, Fruit Frenzy+ spam |
| 22 | Minor | (20, 20, 25) |
| 23 | Minor | (20, 25), (15, 15, 35) |
| 24 | Minor | (15, 15, 40), (20, 20, 30), (20, 25, 25) |
| 25–26 | **Major** | (25 repeat), (20, 30), (10, 40), (20, 20, 40) — **cheesiest**: Immortal Dog, Devour+ spam |
| 27 | Minor | Plesioth & Royal Ludroth only — Crash Wave spam |

### Archetype Examples

- **Paolumu support** (burst, low regen): 100 start stam (70 base + 15 bingo + 15 Stam Boost). Cast Egg Skill: Ardor Shard (100 stam, revives 1 heart) T1. Swap out, regen off-field, return for next revive.
- **Malzeno** (10 regen): Alternate Dracophage Shot (20 stam, Wyvernsoul Def Down) and basic attack; save Egg Skill: Dragon Feller for topple.
- **Ebony Odogaron tank** (15 regen with environment + Stam Surge): Solar Cry → alternate basic attack and Night Parasites+ (30 stam, heals on damage). Pair with Self-Heal (XL), Dancer (XL), All-Elem Def Boost (XL). Beats all 4 elder dragons cheaply.
- **Green Nargacuga** (16 regen with bingo + environment): Fruit Frenzy+ (20, Darkness AoE) + Sickle Tail (10, crit). Pair with Evasion + Critical genes, Accuracy Down coatings (Nargacuga bow), Nargacuga Armor.
- **Mizutsune** (17 regen): Foxflame Bubbles+ (15, burn + accuracy down) + Mud Torrent (15, DoT). Maintain Bubbly Dance (25, Water ATK + Dodge + Regen). Dancer + Evasion + darkness coatings (Deviljho bow).
- **Ratha** (19 regen): Venom Flame (15, para + poison) → Fireball Frolic (20, AoE Fire) OR Bishaten Embers (20, burn, extends debuff duration) OR double Venom Flame then Savage Fireball+ (25).
- **Fruit Frenzy+ spam** (20–21 regen): Strongest meta. Status AoE king — abuse statuses with Non-Elem monsties.
- **Shrouded Nerscylla** (22 regen): Fruit Frenzy+ → Sleep Needle+ (15, Wyvernfell + sleep) + Devour+ (25, lifesteal). Switch back to Fruit Frenzy+ to refresh debuffs.
- **Immortal Dog / Black Diablos** (25–26 regen): White Shadow (80, 2-turn full evasion) + Nourishing Pinecones (0 cost, +30 stam) → net +2 stam per cycle. Or Devour+ (25, lifesteal) for active damage. Effectively immortal.

### Situational Rule

- **Longer fights** (4+ turns): high Stamina Regen matters more.
- **Shorter fights** (1–3 turns): Starting Stamina matters more.
- **Mastery** = tailor monstie to the specific fight.

#### Example: Invasive Shogun Ceanataur farm

- **Boltreaver Astalos** (70 start + 18 regen): Adamant Rage (25) T1, Thunderclap (35) T2, Thunderclap (35) T3 → done.
- **Tobi-Kadachi** (45 start + 23 regen): Can't fit this rotation without sacrificing Stam Boost gene + losing 20% electric bingo. Worse.
- **Zinogre** (50 start + 23 regen): Can fit the rotation, but lower damage + almost no crit.

**High starting stamina wins short fights. High regen wins long ones. Plan the rotation first, then pick the monstie.**

---

## Build Archetypes

### Glass Cannon
- **Species**: Odogaron, Boltreaver Astalos, Rajang
- **Passives**: All-Out (XL), Critical (XL), [Element] Atk Boost (XL)
- **Excursion**: Attack +80, Stamina Recovery +5
- **Risk**: Low survivability — consider Tenacity (M) as insurance

### Tank / Sustain
- **Species**: Dreadqueen Rathian, Gammoth, Gravios, Ebony Odogaron
- **Passives**: Health Boost (XL), All-Elem Def Boost (XL), Self-Heal (XL), Divine Blessing (XL)
- **Excursion**: HP +120, Defense +80

### Crit-Kinship Engine
- **Species**: Ruiner Nergigante, Zinogre, Magnamalo
- **Passives**: Critical (XL), Soul Kinship (XL), Critical Kinship (XL)
- **Loop**: crits fill Kinship → Kinship Skills → repeat

### Wyvernsoul Topple
- **Species**: Chatacabra (61 WF), Paolumu (60 WF, 120 WF Kinship AoE), Yian Garuga (59 WF, 10% base crit)
- **Passives**: Dragon Buster (+25 WF), Critical (XL) (1.5× WF crit), All-Out (XL)
- **Key moves**: Pickaxe Beak (40 WF, 15 stam, stacks Wyvernsoul Def Down), Dracophage Shot
- **Weapons**: Yeti Hammer (HVY Perfect Strike), Spongia Bow (highest WF + Exhaust Coating), Veldian Sibilus HH (party Wyvernfell Up)
- **Armor**: Goss Harag (Dragon Buster L), Diablos Nero (Dragon Buster M + Slugger)
- **Loop**: Stack Wyvernsoul Def Down → deplete → Topple → Synchro Rush → Mount → repeat

### Status Disruptor
- **Species**: Purple Gypceros, Dreadqueen Rathian, Bishaten, Shrouded Nerscylla
- **Passives**: Inflict Rate Up (XL), Salt in the Wound (XL)
- **Actives**: Venom/Para/Sleep/Flash skills; Fruit Frenzy+ for AoE status
- **Bishaten's Kinship Attack** (Fruit Barrage) inflicts multiple statuses

### Support / "Child Labor" Palamute (Canyne)

- **Species**: Canyne (Speed / Non-Elem / Rank 5 / Fanged Beast / Canalta — Blessing Hill)
- **Obtained**: Chapter 13 ("Ward") — defeat Invasive Arzuros, collect egg from Endangered Den
- **Stats**: Very high Speed (9), solid Defense, mediocre Attack (5) and Crit (1). **Not a damage dealer — pure support.**
- **Riding actions**: Jump, Wall Climb, Roar, Melee Attack, **Ground Dive** (unique — underground passages). Best exploration monstie.
- **Kinship Attack**: Rising Axel (Non-Elem single-target).

**Unique genes (Canyne-exclusive):**
- **Art of Raw Power**: Non-Elem Atk Up buff to self (20 stam)
- **Art of Friendship** (Lv30): Grants Regenerate to ALL allies (20 stam) — key support
- **Art of Striking**: Non-Elem damage, scales with repeat use

**Core strategy**: Cycle healing, stamina recovery, and evasion.
- **Nourishing Pinecones** (from Blood Orange Bishaten, Tarkuan): 0 stam, recovers own stamina
- **White Shadow** (from Silverwind Nargacuga): 80 stam, 2-turn full evasion
- **Art of Friendship**: Party Regenerate
- Passives: Stamina Surge (XL) +6/turn, Stamina Boost (XL) +20 start
- Excursion: Stamina Recovery +5 (Canalta)
- 3-bingo bonus: +3 Stamina Recovery
- **Tendency: Cautious**

**Stamina engine**: Base + Stam Surge XL (+6) + bingo (+3) + excursion (+5) = massive regen. Nourishing Pinecones = free refill.

### Velkhana — Skill Seal Control (PvP)

- **Role**: Lock opponent skills (Technical/Ice)
- **Passives**: Ice Attack (XL), defensive options for mirror matches
- **Bingo**: Technical + Ice
- **Note**: Less optimal for PvE (AI barely uses skills)
- **Farm**: High-rank Ice region dens, post-game

## Environment Skills

At S-rank in an environment, a monstie unlocks one skill slot. Max 3 total across all regions.

| Region | Stat Bonus | B-Rank | A-Rank | S-Rank |
|---|---|---|---|---|
| Azuria | Max HP | Power Resilience | High Morale (+buff duration) | — |
| Canalta | Stamina Recovery | Speed Resilience | High Morale | Unscathed (negate H2H damage + bonus damage) |
| Tarkuan | Defense | — | Best Buds (Riding Kinship faster) | Resonance (Kinship boost at battle start) |
| Serathis | — | — | Perseverance (revive once after Heart loss) | Muster Forces (Kinship boost on Heart loss) |

Can mix skills from different regions. Sending to a region where not released grants stat bonuses only. **Ratha** is treated as S-rank in all regions by default.

## See Also

- [genes/genes.md](genes.md) — gene mechanics, bingo, affinity
- [genes/sources.md](sources.md) — where to farm each gene
- [excursions/excursions.md](../excursions/excursions.md) — habitat restoration, mutations, SR expeditions
- [combat/combat.md](../combat/combat.md) — Wyvernfell / Kinship mechanics
