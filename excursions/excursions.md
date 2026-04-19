# Excursions — MHS3

Excursions send a monstie temporarily to an ecosystem for stat bonuses and **Environment Skills**. Separate system from Habitat Restoration (which raises the zone's Ecosystem Rank permanently).

## Excursions vs Habitat Restoration

| Feature | Habitat Restoration | Excursions |
|---|---|---|
| **Purpose** | Raise Ecosystem Rank, unlock mutations, dual-element eggs | Gain Environment Skills + stat bonuses |
| **Action** | Release monsties permanently | Send monstie temporarily (Training Talisman required) |
| **Cost** | Monsties consumed | Training Talisman (Melynx Emporium, Silver Trade Points) |
| **Result** | Zone-wide benefits | Individual monstie benefits |
| **Limit** | 5 per species per zone | One monstie at a time |

## Stat Increases via Excursions

Send a monstie to a specific ecosystem. At **3★ rank**, they gain **2 stat increase slots** with these options:

| Bonus | Value |
|---|---|
| Attack | +80 |
| Defense | +80 |
| HP | +120 |
| Stamina Recovery | **+5 per turn** |

Use these to cover weaknesses:
- Odogaron (low def) → Defense +80 + HP +120 to survive AoE
- Paolumu (low attack) → Attack +80 for added kick
- **Any monstie** → Stamina Recovery +5 enables the next regen breakpoint (see [../genes/builds.md](../genes/builds.md) stamina rotations)

## Environment Skills from Excursions

A monstie can hold **3 Environment Skills** max. Can mix skills from different regions. Sending to a region where not released grants stat bonuses only (no Environment Skills).

| Region | Stat Bonus | B-Rank Skill | A-Rank Skill | S-Rank Skill |
|---|---|---|---|---|
| Azuria | Max HP | Power Resilience | High Morale (+buff duration) | — |
| Canalta | Stamina Recovery | Speed Resilience | High Morale | **Unscathed** (negate H2H damage + bonus dmg) |
| Tarkuan | Defense | — | Best Buds (Riding Kinship faster) | Resonance (Kinship boost at battle start) |
| Serathis | — | — | Perseverance (revive once after Heart loss) | Muster Forces (Kinship boost on Heart loss) |

**Ratha** (your starting monstie) is treated as S-Rank in all regions by default — no need to send for Environment Skills.

**Environment Skills have improved versions** triggered by specific genes in your Bingo:
- Example: Battle Thirst+ requires at least one Fire gene in Bingo → easier on Fire monsties

## Excursion Strategy by Archetype

| Archetype | Primary Excursion | Secondary |
|---|---|---|
| Glass Cannon (Odogaron, Boltreaver Astalos, Rajang) | Canalta — Stamina Recovery | Azuria HP for survivability insurance |
| Tank / Sustain | Tarkuan — Defense | Canalta — Stamina Recovery (heal rotations) |
| Crit-Kinship Engine | Tarkuan — Defense | Canalta — Stamina Recovery |
| Wyvernsoul Topple | Canalta — Stamina Recovery | Azuria HP (stay alive) |
| Status Disruptor | Canalta — Stamina Recovery | Tarkuan Defense |
| Support Palamute (Canyne) | Canalta — Stamina Recovery (**crucial**) | — |

## S-Rank Benefits (3 things on top of Excursion stats)

When a monstie reaches S-rank in an environment:

1. **Species S-Rank Attack Skill**: each species has a base attack gene and an S-rank variant with improved stats. S-rank skills can only come from eggs hatched in an environment where the species is S-ranked.
   - Examples: Draconic Flurry → Draconic Flurry+ (50 → 60 Power), Night Parasites → Night Parasites+ (35 → 30 stamina), Poison Spike +10 Wyvernfell, Hell Horn +10 Power.
2. **Environment Skill slot** (above).
3. **Dual Element access** — gain the zone's element as a secondary (see [../habitats/habitats.md](../habitats/habitats.md)).

## SR Expeditions (Post-game)

Separate from regular Excursions. SR = "Super Rare" — post-game expedition tickets used to unlock high-rank dens for Elder Dragon farming. See [../eggs/eggs.md](../eggs/eggs.md) for SR ticket mechanics.

## Deep Lookup

Region skill data: `grep "REGION_SKILL" habitats/` (or the raw region data):
```
# Region skills are in the datamine but not currently in a dedicated PSV — 
# reference .xlsx-source/Monster Hunter Stories 3.xlsx → regionskillparamdata
```

## See Also

- [../habitats/habitats.md](../habitats/habitats.md) — Ecosystem Rank, mutations, zone elements
- [../genes/builds.md](../genes/builds.md) — which Excursion bonuses feed which builds
- [../eggs/eggs.md](../eggs/eggs.md) — SR Expedition Tickets for post-game farming
