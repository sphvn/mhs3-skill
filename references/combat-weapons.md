# MHS3 Combat & Weapons Reference

## Combat System Overview
MHS3 combat is **turn-based** with prediction mechanics. You control your Rider + active monstie. AI companions act independently but can be influenced.

## Attack Type Triangle (core mechanic)
```
Power (red)  → beats Speed    → loses to Technical
Speed (blue) → beats Technical → loses to Power
Technical (green) → beats Power → loses to Speed
```
Every monstie has a default attack type. Your weapon attacks also have types. Match your choice to counter the enemy's for optimal damage.

## Head-to-Head (H2H) Clashes
- Triggered when you and the enemy use the SAME attack type (both Power, both Speed, etc.)
- Winner determined by triangle: your Power vs their Technical → you win
- **Winning H2H**: reduced damage taken, charges Kinship Gauge
- **Losing H2H**: increased damage taken, no Kinship gain
- **Gold-colored attacks**: CANNOT be countered via H2H. Bypass the system entirely. Defend or use skills to mitigate. Do not attempt to counter gold attacks.

## Double Attacks
Coordinated strike between Rider and monstie. Requires ALL three conditions:
1. Use the **same attack type** as your monstie (e.g., both Power)
2. Use a **regular attack** (not item or special skill)
3. **Win** the Head-to-Head

Double Attacks deal massive damage — often highest single-turn output. Coordinate with your monstie's natural tendencies. If your monstie favors Power, use Power attacks when you expect an H2H.

## Kinship Gauge & Kinship Skills
- Tear-shaped meter next to YOUR health bar. Fills through landing hits, winning H2Hs, Double Attacks (doubles fill rate), and Synchro Rush (massive fill)
- Full gauge → **Ride your monstie** → fully heals monstie, boosts attack power, ALL normal attacks now damage the Wyvernsoul Gauge
- Filling further while mounted → **Kinship Skills**: unique per monstie, devastating multi-hit or special-effect attacks
- Kinship Attack element is **fixed per species** — cannot be changed by gene channeling
- Genes like Soul Kinship (XL) boost gauge fill rate (+40%)
- Double Kinship: possible when both party members ride simultaneously

## Wyvernfell (stat)
Wyvernfell is a **per-skill stat** shown alongside Power and Stamina cost on every Active Skill. It determines how much damage that skill deals to the enemy's **Wyvernsoul Gauge** — it does NOT affect HP damage.

**Formula (source: Les Carnets):** Gauge damage = **Move Wyvernfell × Monstie Wyvernfell stat** (both act as percentages, multiplied together).
- Move Wyvernfell range: **10–70** (only Active Skills; regular attacks = 0 except Hammer)
- Monstie base Wyvernfell range: **36–60**, plus **+5 to +15** from Bingo bonuses (species-dependent)
- Scaling is multiplicative: 84 Wyvernfell monstie deals **2x** gauge damage vs 42. A 40 Wyvernfell move deals **4x** vs a 10.
- **Critical hits: 1.5x Wyvernsoul damage**

**What deals Wyvernfell damage:**
- Active Skills from Rider and Monstie (each skill's Wyvernfell value)
- Hammer basic attacks (unique — only weapon type where basic attacks damage the gauge)
- ALL Monstie attacks including basic attacks
- Attacks while mounted (even normal attacks deal heavy gauge damage)
- Double Attacks and Kinship Skills (heavy gauge damage)
- Breaking body parts can also contribute

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

**Only two buff types affect gauge damage:**

Wyvernfell Up (increases Wyvernsoul damage, 3 turns):
| Tier | Sources |
|---|---|
| S | Composure (Egg Skill, stackable) |
| M | Storm Veil, Ice Armor / Ice Armor(+), Blade Rush |
| L | Icebreaker (Egg Skill), Pump Up |

Wyvernsoul Defense Down (reduces enemy gauge resistance, S tier, 3 turns, **stackable**):
- Surface Break (Egg Skill), Dragon Blast, **Pickaxe Beak** (stackable!), Dracophage Shot, Berserk Slide+

**Key passive:** Dragon Buster — flat **+25 Wyvernfell** stat boost. Synergizes with Dracophage Shot's Wyvernsoul Def Down.

**Best Wyvernfell monsties:**
| Species | Wyvernfell | Notes |
|---|---|---|
| Chatacabra | 56 base + 5 bingo = 61 | Best for Kinship Attacks |
| Paolumu | 60 total | Kinship Attack: 120 Wyvernfell AoE |
| Yian Garuga | 44 base + 15 bingo = 59 | 10% base Crit (1.5x synergy) |

**Best Wyvernfell move:** Pickaxe Beak — 40 Wyvernfell, 15 stamina, stacks Wyvernsoul Def Down for multiplicative gains each turn.

## Wyvernsoul Gauge & Synchro Rush
The Wyvernsoul Gauge is a bar displayed below enemy monsters' HP bars — their "fighting spirit." Depleting it causes the monster to become vulnerable.

**Wyvernsoul Stock system (stronger monsters):**
- Some monsters have red orbs (Wyvernsoul Stock) beside their gauge
- Each full gauge depletion consumes one Stock orb
- Gauge turns **blue for 1 turn** → monster is **Staggered** (its attacks miss)
- Damage dealt to the blue gauge carries over to the next red gauge
- Deplete all Stocks → **Topple** (monster incapacitated, ALL attacks become guaranteed Crits)

**State flow:** Red Gauge → deplete → Stock consumed + Blue Gauge (1 turn Stagger) → if stocks remain, resets to red → if no stocks, **Topple**

**Synchro Rush:** Available ONLY after Topple. Button prompt appears — entire party attacks simultaneously for massive damage and **greatly fills Kinship Gauge**.
- Use when out of stamina for skills
- Consider skipping if you have stamina — toppled monsters take guaranteed Crits from ALL your skill attacks, which can outdamage Synchro Rush and let you apply status/break parts
- Skip if you need to heal or buff — monster stays toppled regardless

**The core loop:** Deplete Wyvernsoul → Topple → Synchro Rush → fills Kinship → Mount Monstie → mounted attacks deal heavy Wyvernsoul damage → repeat

## Monster Behavior States
| State | Attack Tendency | Visual Cues |
|---|---|---|
| Normal | Balanced | Standard animations |
| Enraged | Favors Power | Roars, aggressive stance, red aura |
| Tired | Favors Technical or Speed | Slower movement, panting |

Learn per-monster patterns. After a few encounters, you'll recognize tells for upcoming attack types.

## Status Effects

| Status | Effect | Resolution / Cure |
|---|---|---|
| Poison / Noxious / Severe | DoT per turn (% of target's max HP — stronger tiers = more damage) | ~3 turns. Antidote (single) / Antidote Powder (AoE + Negate) |
| Burn | DoT per turn (Fire-based) | Burn Ointment (single) / Burnheal Powder (AoE + Negate) |
| Paralysis | Each turn: **chance** to skip action (probability roll, not guaranteed) | Multi-turn. Paracare (single) / Paraheal Powder (AoE + Negate) |
| Sleep | Cannot act until **hit by damage** (wake-up hit). Free turn to heal/buff | Until damaged (or ~3 turns if undisturbed). Energy Drink / Awakening Powder |
| Blastblight | Delayed explosion — detonates after ~3-5 turns. Can be detonated early (Magma Counter, Hellfire Retribution) | Soap Scud (single) / Cleansing Powder (AoE) |
| Bleeding | Incoming damage **amplified** while bleeding (damage-taken multiplier, not DoT) | Sushifish (single, also gives regen) |
| Darkness (Flash) | Reduces accuracy — attacks have higher miss chance | Intuitizer (single) / Darkheal Powder (AoE) |
| Stun | Skips one turn entirely (guaranteed, unlike Paralysis) | Short duration. Caused by Hammer skills, Sonic Bomb, traps |
| Skill Seal | Cannot use ANY skills — only basic P/S/T attacks available | Multi-turn. Zest Pill (single). Velkhana signature ailment |

**Nulberry Elixir** = universal single-target cure for any status.

**Inflict Rate Up** (passive gene, S/M/L/XL tiers): Increases chance to apply ANY status ailment. Stacks with status-specific skills like Debilitating Lilt. **Salt in Wound**: +10% damage vs status-afflicted targets.

**Note:** "Exhaust" is NOT a status ailment in MHS3 — Bow's Exhaust Coating deals Wyvernfell (gauge) damage, not a status effect.

---

## Weapon Types (6)

### Damage Categories
| Category | Weapons | Best vs Body Parts |
|---|---|---|
| Slash | Great Sword, Long Sword | Tails, wings |
| Blunt | Hammer, Hunting Horn | Heads, shells |
| Pierce | Bow, Gunlance | Bodies, soft spots |

### Great Sword (Slash)
- **Strengths**: High damage per hit, good part breaking, beginner-friendly
- **Pairs with**: Power monsties for consistent H2H coverage
- **Phase**: Strong all game, especially early

**Charge Gauge** (3 levels): Fills via skills (Quick Charge) and winning H2Hs. Higher charge = more powerful consumer skills.
- **Charged Slash**: Consumes charge, heavy single-target damage
- **Charge Burst**: High-damage charge finisher (regain stamina variant on some weapons)
- **Wide Slash / True Wide Slash**: Consumes charge, AoE damage to all enemies
- **Rage Slash**: 3-charge heavy single-target hit (unlocks ~Tarkuan)
- **GS Mastery** (passive): Slight chance to gain +1 extra charge level when filling gauge
- **Audacious Rage** (passive): Increases Rage Slash damage, but increases damage taken

### Long Sword (Slash)
- **Strengths**: Flow-based combat, sheathe counters, good sustained DPS
- **Pairs with**: Technical or Speed monsties for variety
- **Phase**: Rewarding mid-to-late game once mechanics are mastered

**Spirit Gauge** (multi-segment): Fills via Spirit Blade skills and winning H2Hs. Stances require at least 1 gauge segment and consume 1 segment per turn active.
- **Spirit Blade**: Builds Spirit Gauge + deals damage
- **Lunge Stance**: Costs 1 gauge/turn. Deals damage, then launches follow-up attacks after allies attack. Ends with Special Sheathe.
- **Retaliation Stance**: Costs 1 gauge/turn. Deals damage, then launches counterattacks after enemies attack. Ends with Special Sheathe.
- **Special Sheathe**: After stance ends — regular attacks deal more damage + unique Unsheathing attack. Length determined by Spirit Gauge level at activation.
- **Spirit Release Slash**: Consumes ALL Spirit Gauge, grants Critical Eye, counters one enemy attack. Removes Special Sheathe on counter or turn end.
- **LS Mastery** (passive): Slight chance to gain +1 extra Spirit Gauge level when filling
- **Iai Mastery** (passive): Slight chance to negate Spirit Gauge reduction during Special Sheathe
- **Counter Boost** (passive): Reduces damage taken during Special Sheathe + slightly increases damage

### Hammer (Blunt)
- **Strengths**: Highest raw damage, excellent Wyvernsoul damage, simple to use
- **Pairs with**: Power monsties for maximum impact
- **Phase**: Strong all game

**No unique gauge** — simplest weapon mechanically. **Unique trait: only weapon where basic attacks damage the Wyvernsoul Gauge** (all other weapons need Active Skills for gauge damage).
- **Perfect Strike**: AoE + heavy Wyvernsoul damage + Stun chance
- **Sweet Spot**: AoE + Wyvernsoul damage + Stun chance
- **Perfect Crush**: AoE + heavy Wyvernsoul damage + Stun chance
- **Spinning Meteor**: High-damage blunt finisher
- **Meteor Hammer**: Single target + heavy part damage
- **Hammer Mastery** (passive): Reduces Stamina cost when winning Head-to-Head
- **Striking Secret** (passive): Normal attacks deal more damage to Wyvernsoul Gauge
- **Soulbreak** (passive): Greatly increases damage dealt to broken monster parts

### Hunting Horn (Blunt)
- **Strengths**: Party support (ATK/DEF up, healing, status cleanse), blunt damage
- **Pairs with**: Support/survivability builds, long fights
- **Phase**: Shines in endgame team scenarios

**Note system**: Attacks generate colored notes — Red (Power), Blue (Speed), Green (Technical). Winning H2Hs or Double Attacks generate **Rainbow Notes** (wildcards for any color). Notes display on a melody staff; new notes push older ones off.

**Melody system**: Each HH has unique melodies activated by specific note sequences on the staff.
- **Two-note melodies**: Faster to build (e.g., Frigid Melody: Ice ATK & DEF Up)
- **Four-note melodies**: More powerful, require 4 specific notes in order
- Example melody effects: ATK Up, DEF Up, Evade All (1 turn), Speed Up, HP Drain, Wyvernfell Up, Elemental Resistance Up, Part Damage Up
- **Magnificent Trio**: Consumes ALL stored melodies — deals damage scaling with melodies consumed, grants all melody buffs to allies simultaneously
- **Polychrome Performer** (passive): Chance to turn notes into Rainbow Notes when adding
- **HH Mastery** (passive): Slightly increases Speed after performing a melody
- **Mending Musician** (passive): Recovers HP when performing a melody

### Bow (Pierce)
- **Strengths**: Ranged safety, status control, flexible
- **Pairs with**: Status-focused monsties (Purple Gypceros, Dreadqueen Rathian)
- **Phase**: Great mid-to-late for control strategies

**Charge Gauge** (up to Level 5): Fills via Rapid Shot (+2 levels), Quick Shot (+1 level), and winning H2Hs. Higher charge = stronger coating effects.

**Coating system — ONLY ONE COATING ACTIVE AT A TIME.** Using a new coating replaces the current one. **Switching coatings resets the Charge Gauge** — this is the key trade-off. Applying a coating costs **0 stamina** and also deals weapon-element damage to one enemy.

Available coatings: Power (increases bow damage), Poison, Paralysis, Sleep, Flash, Exhaust (boosts Wyvernsoul damage), Attack Down, Accuracy, Defense Down.

Key skills:
- **Rapid Shot**: +2 Charge levels + damage. STAB variant at Level 5: consumes charge for high crit damage
- **Dragon Piercer**: Consumes charge, unleashes coating power, single-target
- **Aerial Aim**: Consumes charge, unleashes coating power, single-target
- **Battle Ready** (passive): Auto-activates a random coating at battle start. Higher tiers also start with charge levels.
- **Deft Hands** (passive): +1 guaranteed charge level when switching coatings, chance for another +1 at higher tiers
- **Bow Mastery** (passive): Slight chance to gain +1 extra charge level when filling gauge

### Gunlance (Pierce)
- **Strengths**: Tankiest weapon, aggro drawing, shell damage ignores hitzones
- **Pairs with**: Any monstie that needs protection
- **Phase**: Great for defensive playstyles, endgame survivability

**Shell system** (8 shell capacity): Load shells via Guard Reload (2 shells + Guard) or winning H2Hs. Consume shells for shelling attacks. Shell damage is fixed (ignores monster defense).
- **Shelling**: Consumes 2 shells, elemental damage + Guard
- **Charged Shelling**: Higher damage shelling, more shells consumed
- **Burst Fire**: Consumes ALL 8 shells for massive damage + Guard (L). Triple stamina cost.
- **Wyvern's Fire**: Heavy explosion, massive damage, high stamina cost
- **Hail Cutter**: Overhead shell attack (manages Wyvern's Fire cooldown)
- **Derring Guard**: Brace 1 turn — boosts ATK/DEF relative to damage taken
- **Taunt**: Forces enemies to target you (aggro draw)
- **GL Mastery** (passive): Slight chance to load +2 extra shells when loading
- **Audacious Wyvern** (passive): Increases Wyvern's Fire / Wyvern's Blaze damage

## Part Breaking
- Specific damage types deal bonus damage to certain monster parts
- Breaking parts: extra materials + can disable monster abilities (e.g., broken tail = weaker tail swipes)
- Focus fire on weak points for faster kills and better drops

## Weapon Progression Recommendations
| Phase | Recommendation |
|---|---|
| Early game | Great Sword or Hammer — simple, powerful, easy to upgrade |
| Mid game | Add Long Sword or Bow for variety |
| Late game | All 6 have viable endgame builds; Hunting Horn + Gunlance shine in teams |

Weapons are crafted/upgraded using monster materials. Each weapon has branching upgrade trees. Farm specific monsters for parts. Upgrade regularly — weapon scaling matters.

## Field Tips
- **Hold A to gather** items in the field instead of tapping repeatedly — much faster for bulk collection
- **Combining Menu** is how you craft potions, traps, and consumables — recipes are purchased from vendors (not discovered automatically)
- Swap weapons between fights freely — the game encourages matching damage type to the encounter

## Recommended Settings
- **Options > Camera > Auto-Centering → OFF**: Defaults to on, which forces the camera to follow movement direction. Turning it off gives manual analog stick control — lets you run while looking behind you, scout surroundings, etc. Much better for exploration.
- **Options > Game Settings > Caution Icon Display**: Controls the dragon icon above overworld monsters that are much higher level than you. Toggle off if you find it distracting.
