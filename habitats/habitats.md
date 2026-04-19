# Habitats — MHS3

Zones, spawn conditions, day/night, habitat restoration, ecosystem rank, mutations, and dual-element farming.

## Day/Night System

Toggle at any Catavan Stand. Night brings:
- Higher-level monsters (~10 levels higher)
- More Barrel Felynes (EXP farming)
- Dens can have **two gathering spots** (vs one during day)

### Night-Only: Invasive Monsters (9 total)

| Monster | Level | Zone | Location |
|---|---|---|---|
| Invasive Yian Garuga | 10 | Azuria | — |
| Invasive Plesioth | 15 | Azuria | Mirror Lake cave |
| Invasive Seregios | 18 | Azuria | NW Azuria (requires flight) |
| Invasive Arzuros | 23 | Canalta | — |
| Invasive Nerscylla | 23 | Canalta | Blessing Hill |
| Invasive Shogun Ceanataur | 27 | Canalta | Waterfall cave |
| Invasive Diablos | 38 | Tarkuan | Colossal Dragon's Remains |
| Invasive Odogaron | 40 | Tarkuan | Rococo Rocks |
| Invasive Khezu | 42 | Serathis | Glacial Caps |

Also night-only: **Brachydios** (Ancient Battlegrounds, Broadleaf Basin), **Elder Dragons** (post-game), **Blue (Super Rare) dens**.

See also [../monsters/invasives-endangered.md](../monsters/invasives-endangered.md) for complete lists.

## Habitat Restoration

### Unlock

Defeat the Feral Monster in each region:
- Azuria: **Feral Brachydios** (Blightstone Woods)
- Canalta: **Feral Espinas** (Mount Canalta)
- Tarkuan: **Feral Glavenus** (Bountiful Dunes)
- Serathis: Story progression

### Mechanics

Release hatched monsties into restoration slots at camps. **5-slot limit per unique species per zone.** Released monsties cannot be retrieved.

### Ecosystem Rank: B → A → S

Rank accelerators:
1. **Level before release** — higher level = more rank contribution (always level up first)
2. **Species stacking** — multiple of the SAME species in one zone increases multiplier
3. **Element stacking** — multiple of the SAME element boosts multiplier (don't need to match zone element)

### Rank Benefits

| Rank | Effect |
|---|---|
| B | Easier egg spawns, slightly elevated hatch levels, first Environment Skill |
| A | Better starting stats, A-rank Environment Skills, subspecies mutations unlock |
| S | S-Rank genes on hatched monsties, S-rank Environment Skills, **Deviant mutations**, consistent dual-element eggs |

## Zone Elements (for Dual-Element Farming)

Each camp/area has an associated element. Eggs from zones where ecosystem rank is raised can acquire that zone's element as a **secondary element**. Once applied, secondary element **cannot be removed**.

| Region | Area | Element |
|---|---|---|
| **Azuria** | Sunpetal Plains | Fire |
| | Broadleaf Basin | Thunder |
| | Mirror Lake | Water |
| | Blightstone Woods | Non-Elem |
| **Canalta** | Howlinyowl Forest | Fire |
| | Mt. Canalta | Thunder |
| | Cataracts | Water |
| | Blessing Hill | Non-Elem |
| | Frozen Grotto | Ice |
| **Tarkuan** | Bountiful Dunes | Fire |
| | Rococo Rocks | Thunder |
| | Colossal Dragon's Remains | Dragon |
| | Death's Maw | Non-Elem |
| **Serathis** | Glacial Caps | Water |
| | Old Capital Road | Ice |
| | Sacrosanctum/Lazlion | Dragon |

**Strategy**: Release a specific monstie into a specific zone to farm eggs with a desired second element.

### Dual Element Mechanics (Les Carnets)

- Using non-matching element → -10% damage penalty
- Dual element with matching zone element → penalty negated (= standard-element monstie with same ATK)
- No offensive downside to going dual element
- **Species-specific** resistance changes: dual element CAN alter elemental weaknesses

Resistance multipliers:
| Level | Damage Taken |
|---|---|
| Extra weak | 150% |
| Weak | 125% |
| Neutral | 100% |
| Resistant | 90% |
| Highly resistant | 70% |

**Trade-off**: Since Kinship Attack element is fixed per species, dual element may require TWO different elements in your Bingo grid, splitting elemental bingo lines.

## Mutations (17 Total)

### Subspecies Mutations (lower rank requirement)

| Mutation | Base Monstie | Rank | Stars |
|---|---|---|---|
| Pink Rathian | Rathian | B | 5★ |
| Ivory Lagiacrus | Lagiacrus | A | 6★ |
| Green Nargacuga | Nargacuga | A | 5★ |
| Stygian Zinogre | Zinogre | A | 6★ |
| Sand Barioth | Barioth | A | 5★ |
| Azure Rathalos | Rathalos | A | 6★ |
| Brute Tigrex | Tigrex | A | 6★ |

### Deviant Mutations (S-rank + companion conditions)

| Mutation | Base | Conditions |
|---|---|---|
| Dreadqueen Rathian | Rathian / Pink Rathian | S-rank + 3+ poison-type monsties in same habitat |
| Dreadking Rathalos | Rathalos / Azure Rathalos | S-rank + 4+ Flying Wyverns in same habitat |
| Silverwind Nargacuga | Nargacuga / Green Nargacuga | S-rank + 2+ wind monsties (Great Izuchi, Paolumu, Legiana) |
| Thunderlord Zinogre | Zinogre / Stygian Zinogre | S-rank + Mizutsune also at S-rank same habitat (reciprocal) |
| Soulseer Mizutsune | Mizutsune | S-rank + Zinogre also at S-rank same habitat (reciprocal) |
| Grimclaw Tigrex | Tigrex / Brute Tigrex | S-rank + 4+ Power-type monsties |
| Deadeye Yian Garuga | Yian Garuga | S-rank + 3+ monsties of equal or greater eco rank |
| Hellblade Glavenus | Glavenus | S-rank + 4+ razor-appendage monsties (Great Izuchi, Magnamalo, Seregios, Shogun Ceanataur) |
| Boltreaver Astalos | Astalos | S-rank + Thunder-element zone + 3+ Thunder monsties |
| Bloodbath Diablos | Diablos / Black Diablos | S-rank + **Bountiful Dunes (Tarkuan) only** |

**Notes:**
- Subspecies = prerequisite for deviants (Rathian → Pink Rathian → Dreadqueen Rathian)
- Thunderlord Zinogre and Soulseer Mizutsune are **reciprocal**
- Monsterpedia provides in-game hints
- Mutation eggs appear as "Endangered Species" eggs once conditions met

## Nest Tables & Ecosystem Rank Phases

The game uses three Risk Rank phases (Phase1, Phase2, Phase3) that control nest-rarity weighting:

```
grep "Phase1" habitats/ecology-rank.psv   # see B/A/S weights for early-story nests
```

Columns: `nest_rarity|nest_risk_rank|ecology_rank|weight_normal|weight_rare|weight_super_rare`.

For the 160 nest tables with enemy lists and fes rates:
```
grep "nt100" habitats/nests.psv           # Azuria nt100 area nests
grep "^A" habitats/nests.psv              # all Area A nests
```

## Excursions (Separate System)

Excursions are separate from Habitat Restoration — they send a monstie temporarily for stat bonuses and Environment Skills. See [../excursions/excursions.md](../excursions/excursions.md).

## Deep Lookup

- `cat habitats/nests.psv` — 160 nest rows with enemy lists
- `cat habitats/ecology-rank.psv` — 48 eco-rank weightings
- `cat habitats/mutations.psv` — 17 mutation recipes with Required Monsties
- `grep "Rathian" habitats/mutations.psv` — Rathian-line mutation conditions

## See Also

- [../eggs/eggs.md](../eggs/eggs.md) — egg patterns, potency, SR tickets
- [../excursions/excursions.md](../excursions/excursions.md) — Environment Skills, stat bonuses
- [../genes/builds.md](../genes/builds.md) — how to build around dual-element/ecosystem buffs
