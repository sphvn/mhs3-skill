# Monster Parts — MHS3

Each monster has body parts with separate HP pools and **damage multipliers per weapon type**. Hitting the right part with the right weapon = breaks faster + more damage.

## General Rules

| Damage Type | Weapons | Best vs Parts |
|---|---|---|
| Slash | Great Sword, Long Sword | **Tails, wings** (cutting) |
| Blunt | Hammer, Hunting Horn | **Heads, shells** (impact) |
| Pierce | Bow, Gunlance | **Bodies, soft spots** (penetration) |

These are general defaults. Per-monster multipliers override — always check `monsters/parts.psv`.

## Reading parts.psv

```
schema: parts_id|monster|part_num|max_hp|slash_parts_dmg|blunt_parts_dmg|pierce_parts_dmg|monster_parts_dmg|slash_hp_dmg|blunt_hp_dmg|pierce_hp_dmg|monster_hp_dmg|broken_parts_id|sp_dmg|is_blightstone|break_bonus
```

- **parts_id**: `ID_PARTS_EM0001_00_00_1` (monster + part number)
- **monster**: the EM code (use `monsters/monster-book.psv` or `monsters/monsters.psv` to resolve to name)
- **part_num**: 1/2/3/... — index into monster's part list (head, body, tail, etc.)
- **max_hp**: part's HP pool (when depleted = broken)
- **slash_parts_dmg / blunt_parts_dmg / pierce_parts_dmg**: **multiplier to the PART HP** from that damage type. Higher = the part breaks faster.
- **slash_hp_dmg / blunt_hp_dmg / pierce_hp_dmg**: multiplier to the MONSTER'S HP from attacking that part. Higher = more overall damage.
- **break_bonus**: reward tier for breaking the part (materials)

### Example reading:

```
grep "ID_PARTS_EM0001_00_00_" monsters/parts.psv
```

If part 1 (head) has `slash_parts_dmg=30, blunt_parts_dmg=30, pierce_parts_dmg=-30`:
- Slash and Blunt both +30% to head HP → break with GS/LS/Hammer/HH
- Pierce: -30% to head HP → **don't use Bow or Gunlance on the head**

If part 2 (tail) has `slash_parts_dmg=30, blunt_parts_dmg=-30, pierce_parts_dmg=-30`:
- **Slash only** — Hammer/HH/Bow/GL do reduced part damage
- Cut the tail with Great Sword or Long Sword

## Finding Weak Points

Workflow for "best weapon vs X":

1. `grep "^X|" monsters/monsters.psv` → get `slash_dmg`, `blunt_dmg`, `pierce_dmg` (global body damage multipliers)
2. `grep "^ID_PARTS_{monster_code}" monsters/parts.psv` → per-part multipliers
3. Match damage type to highest multiplier

**Example — Rathalos**:
- Global: slash moderate, blunt moderate, pierce slightly higher (head weak)
- Parts: head high slash + blunt; tail high slash only; wings high slash; body balanced
- **Best strategy**: Great Sword or Long Sword → break wings/tail for materials; Bow for body pressure.

## Break Bonuses

When a part breaks:
- **Extra materials** drop (often unique to the part)
- Monster may **lose abilities** (broken tail = weaker tail swipes, broken horn = weaker magic)
- Status applications may become easier

Weapons with **Partbreaker** passive (armor skill) increase part damage — stack with break-focused plays.

## Blightstone Parts

Some parts have **Blightstone** variants — break these to weaken specific monster mechanics (e.g., Astalos's crest disables lightning). Flag: `is_blightstone=True` in parts.psv.

## Deep Lookup

- `grep "^ID_PARTS_EM0001" monsters/parts.psv` — all Rathian-line parts
- `awk -F'|' '$5>20 { print $1, $4 }' monsters/parts.psv` — parts with high slash multiplier
- Map EM codes to names: `grep "EM0001" monsters/monster-book.psv`

## Part Break → Gene / Material Unlocks

Some genes only drop from broken parts, and many armor/weapon upgrades require break-only materials. Check:
- `grep "^X|" monsters/monsters.psv` field `break_materials` for the break-only loot table
- Cross-ref with armor/weapon recipes in `armor/params.psv` and `weapons/{type}/params.psv`

## See Also

- [monsters.md](monsters.md) — enemy data, status hit rates, global damage types
- [../weapons/weapon-mechanics.md](../combat/weapon-mechanics.md) — Slash/Blunt/Pierce by weapon
- [../combat/combat.md](../combat/combat.md) — Wyvernsoul Gauge interacts with part breaks
