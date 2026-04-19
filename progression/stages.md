# Stages & Regions — MHS3

40 stages total (maps/dungeons across 4 regions + post-game).

Full data: `cat progression/stages.psv`. Schema: `stage_id|name|region|stage_type|size_x|size_y`.

## Region → Stage Summary

### Azuria (R0)

Starting region. Rank 1–5 content. Story chapters 1–8.

| Stage ID | Name | Type |
|---|---|---|
| st100 | Azuria | Overworld hub |
| dg100 | Ashen Pass | Dungeon |
| (more in PSV) | Sunpetal Plains, Broadleaf Basin, Mirror Lake, Blightstone Woods | Fields |

### Canalta Timberland (R1)

Mid-game. Rank 3–6 content.

| Stage ID | Name | Type |
|---|---|---|
| st200 | Canalta Timberland | Overworld hub |
| dg200 | Narrow Passage | Dungeon |
| Mt. Canalta, Howlinyowl Forest, Blessing Hill, Cataracts, Frozen Grotto | Fields |

### Tarkuan (R2)

Mid-late game. Rank 4–6 content.

| Stage ID | Name | Type |
|---|---|---|
| st300 | Tarkuan | Overworld hub |
| Bountiful Dunes, Rococo Rocks, Colossal Dragon's Remains, Death's Maw | Fields |

### Serathis (R3)

Late game. Rank 5–7 content. Endgame prep.

| Stage ID | Name | Type |
|---|---|---|
| st400 | Serathis | Overworld hub |
| Glacial Gaps / Glacial Caps, Old Capital Road, Sacrosanctum / Lazlion | Fields |

### Post-game

Elder Dragon fights + SR Expedition dens spread across all regions at night.

## Stage Types

| Type Code | Description |
|---|---|
| 2 | Overworld hub (fields, ~3072×3072 cells) |
| 3 | Dungeon (enclosed, smaller) |
| (other) | Special fight arenas, story-specific |

## Story Order (Recommended Progression)

1. **Azuria** — Complete chapters 1–8. Unlock Feral Brachydios → Habitat Restoration.
2. **Canalta** — Chapters 9–15. Clear Invasive Arzuros for Canyne / Shogun Ceanataur for Invasives/Endangered unlocks.
3. **Tarkuan** — Chapters 16–20. Feral Glavenus unlock.
4. **Serathis** — Chapters 21–end. Story finale.
5. **Post-game** — Elder Dragons + SR farming.

## Zone Element Mapping

See [../habitats/habitats.md](../habitats/habitats.md) for area → element mapping (dual-element farming). Example: Azuria's Sunpetal Plains = Fire element; releasing fire-line monsties there raises Fire ecosystem rank.

## Deep Lookup

- `cat progression/stages.psv` — all 40 stages
- `grep "^st" progression/stages.psv` — overworld hubs
- `grep "^dg" progression/stages.psv` — dungeons
- `grep "Azuria" progression/stages.psv` — Azuria-region stages

## See Also

- [rider.md](rider.md) — level scaling per region
- [../habitats/habitats.md](../habitats/habitats.md) — zone elements, ecosystem rank
- [../zones/](../zones/) — curated zone progression advisors (recommended monsties + gear)
