# Enemy Monsters — MHS3

Enemy monsters (non-hatchable) — bosses, endangered species, invasives, elder dragons, and their variants. Distinct from hatchable monsties (see [../monsties/monsties.md](../monsties/monsties.md)).

187 enemy rows total in the datamine, including unique fight variants (re-fights, story bosses, etc.).

## Categories

**Endangered Species** — Boss-level monsters that unlock via Habitat Restoration. Drop unique materials.
**Invasive Monsters** — Aggressive outsiders that invade zones. Night-only spawns. Drop Invasive-material weapons/armor.
**Elder Dragons** — Post-game only. Night spawns. See [elder-dragons.md](elder-dragons.md).
**Common** — Regular wild monsters (most enemies).

See [invasives-endangered.md](invasives-endangered.md) for the full invasive + endangered list.

## Key Enemy Mechanics

Every enemy monster in MHS3 has:
- **Base stats** (HP, ATK, DEF, SPE, CRIT) — grep `monsters/monsters.psv`
- **Element** (primary) — determines what it fires and is weak/resistant to
- **Attack Type** — Power / Speed / Technical, affects H2H
- **Slash/Blunt/Pierce Damage Rates** — how receptive the monster is to each weapon type globally
- **Status Hit Rates** — Poison, Burn, Paralysis, Sleep, Blastblight, Bleed, Blind, Sonic Bomb (for trap viability)
- **Parts** — separate HP pools per body part with their own S/B/P multipliers (see [parts.md](parts.md))

### Attack Pattern Shift

Many enemies shift attack type between states:
- **Normal** → one attack type (e.g., Velkhana: Technical)
- **Enraged** → different type (e.g., Velkhana enraged: Speed + Power)

Learn per-monster patterns — recognize tells for upcoming attack types.

### Status Resistance

Most bosses are resistant to the same element they use (Rathalos resists Fire, Lagiacrus resists Thunder). Most Invasives and Elder Dragons resist their primary element strongly. Status effects also have resistances — grep `monsters/monsters.psv` for hit rate columns.

## Reading monsters.psv

```
schema: name|species|element|level|non_elem|fire|water|thunder|ice|dragon|atk_rank|def_rank|hp_rank|heal_rank|crit_rate|speed|slash_dmg|blunt_dmg|pierce_dmg|monster_dmg|poison_hit|burn_hit|paralysis_hit|sleep_hit|blast_hit|bleed_hit|blind_hit|sonic_bomb_rate|status_type_1|status_type_2|status_type_3|monstie_id|exp_rate|materials|break_materials
```

- **crit_rate**: monster's chance to crit YOU
- **slash_dmg / blunt_dmg / pierce_dmg**: damage multiplier when attacked with that weapon type (higher = more vulnerable to that damage type)
- **poison_hit, burn_hit, etc.**: % chance your statuses apply to this monster (higher = easier to inflict)
- **sonic_bomb_rate**: sonic bomb trap effectiveness

### Example: "How to fight Rathalos"

```
grep "^Rathalos|" monsters/monsters.psv
```
Read the row: element Fire (so Water is strong vs it), likely high sonic_bomb_rate (vulnerable to Flash + Sonic Bomb), moderate slash_dmg and blunt_dmg. Cross-reference [parts.md](parts.md) to find weak spots (head / tail / legs).

### Example: "What zone has the most Fire monsters?"

```
awk -F'|' '$4=="1" { print $1, $2 }' monsters/monsters.psv   # (Fire-primary enemies)
```

Cross-reference [../habitats/habitats.md](../habitats/habitats.md) zone-element table.

## Monster Picture Book (Regions + Flavor)

The Monsterpedia entry data has Regions, Areas, Habitat blurb, Main Flavour (lore), Sub Flavour (behavior notes), Trace Items:

```
grep "^Deviljho" monsters/monster-book.psv
```

Schema: `name|enemy_id|otomon_id|regions|areas|dungeons|habitat|main_flavour|trace_items|mutation_monster`

Useful for "where does X spawn?" and lore questions.

## Enemy Skills (What Moves Enemies Use)

161 monster-exclusive skills catalogued:

```
grep -i "dragon feller" monsters/enemy-skills.psv
grep -i "explosive" monsters/enemy-skills.psv
```

Schema: `skill_id|name|description`. Cross-reference with fight encounters to predict what a monster will cast.

## Enemy Level Scaling

836 enemy × stage combinations. How enemies scale per zone:

```
grep "Rathalos" monsters/enemy-levels.psv | head -20
```

Schema: `enemy|stage|stage_area_levels|level_scale|level_fluctuation|scale_max|night_add|is_eco`

- **night_add**: level boost when fighting at night (usually +10)
- **is_eco**: whether this fight participates in ecosystem ranking

## Fight Types

| Type | Mechanics |
|---|---|
| Overworld encounter | Bump into a monster on the field; they flee to nest if defeated |
| Retreat den fight | Follow a fleeing monster to its nest; guaranteed egg |
| Invasive hunt | Night-only; specific spawn points; unique materials |
| Habitat Restoration unlock | Defeat the Feral variant in each region |
| Story boss | Scripted encounters; usually unique (not in the overworld pool) |
| Elder Dragon | Post-game only; night spawns; SR tickets for guaranteed |

## See Also

- [parts.md](parts.md) — part-break targeting (slash/blunt/pierce per part)
- [elder-dragons.md](elder-dragons.md) — elder dragon unlock, spawns, fight notes
- [invasives-endangered.md](invasives-endangered.md) — full invasives + endangered lists
- [../weapons/weapons.md](../weapons/weapons.md) — weapon-type → damage-category match
- [../habitats/habitats.md](../habitats/habitats.md) — where monsters spawn
