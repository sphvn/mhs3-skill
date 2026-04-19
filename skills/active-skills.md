# Active Skills — MHS3

Active Skills are battle abilities that cost Stamina (and sometimes Kinship). They come from **genes** (for monsties), **weapon decos** (for the Rider), and **egg powers** (egg-unique skills).

292 total active skills in the game. For full catalog: `cat skills/active-skills.psv`.

Schema: `name|target|type|element|stamina|power|wyvernfell|effects|source`.

## Top Skills by Role

### DPS — Single Target

| Skill | Type | Elem | Stam | Pwr | WF | Source |
|---|---|---|---|---|---|---|
| Dragon Eater+ | Power | Dragon | 35 | 100 | 10 | Deviljho (Drains HP) |
| Calamity Slash | Power | Dragon | — | — | — | Nergigante (XL gene, massive hit) |
| Venom Flame | Power | Fire | — | — | — | Espinas (Paralysis + Noxious Poison) |
| Spirit Reckoning | weapon | varies | — | — | — | LS weapon skill (STR/SHARP variants) |

### DPS — AoE

| Skill | Type | Elem | Notes |
|---|---|---|---|
| Dragon Blast | Power | Dragon | All-enemy Dragon + Wyvernsoul Def Down (Deviljho) |
| Supernova | Power | Fire | Massive Fire AoE (Teostra) |
| Thundercall / Thunderclap | Power | Thunder | AoE Thunder bursts (Zinogre line) |
| Hellfire Retribution | Speed | Dragon | Detonates Blastblight early (Magnamalo) |
| Fruit Frenzy+ | Speed | Non-Elem | 20 stam, AoE multi-status (Bishaten line, Shrouded Nerscylla) — **meta** |
| Solar Cry | — | — | Kinship Gauge +30 to party (Dreadqueen Rathian, Boltreaver Astalos) |

### Wyvernsoul Damage (gauge depletion)

| Skill | Stam | WF | Notes |
|---|---|---|---|
| Pickaxe Beak | 15 | **40** | Stacks Wyvernsoul Def Down — top Wyvernfell move |
| Dracophage Shot | 20 | 30 | Wyvernsoul Def Down stacker |
| Dragon Blast | 50 | 30 | AoE Wyvernsoul Def Down + damage |
| Surface Break | — | 30 | Wyvernsoul Def Down (Egg Skill) |

### Support / Buffs

| Skill | Stam | Effect | Source |
|---|---|---|---|
| Solar Cry | — | +30 Kinship party | Dreadqueen/Boltreaver |
| Storm Veil | — | 4 buffs (Water ATK, Thunder ATK, Wyvernfell, Def) | Namielle |
| Bubbly Dance | 25 | Water ATK + Dodge + Regen | Mizutsune |
| Composure | — | Wyvernfell Up S (stackable) | Egg Skill |
| Magnificent Trio | weapon | Consumes all melodies, buffs party | HH weapon skill |
| Art of Friendship | 20 | Party Regenerate | Canyne (Lv30) |

### Control / Status

| Skill | Status | Source |
|---|---|---|
| Venom Flame | Paralysis + Noxious Poison | Espinas |
| Noxious Poison | Poison + DoT | Dreadqueen Rathian |
| Venom Queen | Severe poison AoE | Dreadqueen Rathian (XL) |
| Reverberating Roar | AoE Stun | Brute Tigrex |
| Sleep Needle+ | Sleep + Wyvernfell | Shrouded Nerscylla (S-rank) |
| Skill Seal | Locks enemy skills | Velkhana (XL) — **PvP dominant** |
| Foxflame Bubbles+ | Burn + Accuracy Down | Mizutsune (S-rank) |

### Sustain

| Skill | Stam | Effect |
|---|---|---|
| Night Parasites+ | 30 | Heals user based on damage dealt (Ebony Odogaron S-rank) |
| Devour+ | 25 | Lifesteal (Black Diablos S-rank, Nerscylla line) |
| Bloodblight | XL gene | Drains HP on hit (Malzeno) |
| Life Drain | M gene | HP recovery (Malzeno) |
| Egg Skill: Ardor Shard | 100 | Revives 1 Heart to an ally (Paolumu niche) |

## Affinity Variants

Active skills have affinity suffixes (STR, ATK, BRK, CRSH, HVY, BLNT, FLSH, STAB, XPRT, TLNT, LONG, ARC, CURE, HEAL). Each suffix is a trade-off. See [../genes/genes.md](../genes/genes.md) for the full Affinity Effects table.

## Power vs Wyvernfell

Every active skill has two key numbers:
- **Power**: damage to the enemy's HP
- **Wyvernfell**: damage to the enemy's **Wyvernsoul Gauge** (depletes faster with Wyvernfell)

**Tradeoff**: CRSH/HVY affinity boost Wyvernfell at the cost of Power. CRFT/ATK boost Power at the cost of Wyvernfell. Know your rotation's objective — deplete the gauge first (Wyvernfell), then Topple (guaranteed crits make Power more effective).

## Egg Skills

Skills beginning with "Egg Skill:" come from **Egg Powers** carried by eggs, not from regular gene channeling. Examples: Egg Skill: Ardor Shard, Egg Skill: Composure, Egg Skill: Thunderclap, Egg Skill: Dragon Feller.

List all egg skills:
```
grep "^Egg Skill:" skills/active-skills.psv
```

See [../eggs/egg-powers.md](../eggs/egg-powers.md) for egg power mechanics.

## Deep Lookup

- `cat skills/active-skills.psv` — full 281-skill catalog
- `grep -i "dragon" skills/active-skills.psv` — all Dragon-element skills
- `grep -i "| Deviljho" skills/active-skills.psv` — skills from Deviljho
- `awk -F'|' '$7>=30' skills/active-skills.psv` — high-Wyvernfell skills

## See Also

- [passive-skills.md](passive-skills.md) — always-on skills (not the same pool)
- [buffs-debuffs.psv](../skills/buffs-debuffs.psv) — 70-row buff/debuff reference
- [../genes/genes.md](../genes/genes.md) — affinity effects table
- [../combat/combat.md](../combat/combat.md) — Wyvernfell mechanics
