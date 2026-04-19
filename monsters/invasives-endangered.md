# Invasives & Endangered Species — MHS3

Two special enemy categories with mechanics distinct from regular wildlife.

## Invasive Species (9)

Hostile monsters that **invade zones at night**. Each must be **defeated to unlock the endangered species population** in that zone. Drop Invasive materials used for the **Veldian series** (Arkveld-line weapons/armor).

| Monster | Level | Region | Location |
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

**Night only**: Rest at camp to shift time.
**Stat boost**: Invasives are significantly stronger than their non-invasive counterparts.
**Materials**: Unique Invasive materials unlock the Arkvulcan armor / Veldian weapon line.

## Endangered Species (21+)

Endangered monsters become available for **egg collection** AFTER defeating the invasive in that region. Many are boss-level with signature abilities.

### Confirmed Endangered List (from datamine)

From `monsters/invasives-endangered.psv` (`ENDANGERED` row):

Rathian, Pink Rathian, Dreadqueen Rathian, Tigrex, Brute Tigrex, Grimclaw Tigrex, Nargacuga, Green Nargacuga, Silverwind Nargacuga, Barioth, Sand Barioth, Lagiacrus, Ivory Lagiacrus, Zinogre, Stygian Zinogre, Thunderlord Zinogre, Astalos, Boltreaver Astalos, Mizutsune, Soulseer Mizutsune, **Canyne (Palamute)**.

### Regional Unlocks (after defeating the invasive)

| Region | Unlocks |
|---|---|
| Azuria | Rathian, Lagiacrus, Astalos |
| Canalta | Nargacuga, **Canyne**, Mizutsune |
| Tarkuan | Tigrex, Zinogre |
| Serathis | Barioth |

**Canyne's Ward unlock**: Chapter 13 quest — defeat Invasive Arzuros at Blessing Hill, collect Canyne egg from the Endangered Den.

## Why They Matter

Endangered species are mostly high-rank (Rank 5+) and include **all the mutation lines** (subspecies → deviant). Without defeating invasives, you cannot:
- Hatch Rathian-line monsties
- Progress to Dreadqueen, Silverwind, Thunderlord, etc.
- Access the top-tier genes these species carry

**Priority**: Clear invasives early-to-mid game to maximize endangered farming time.

## Deep Lookup

- `cat monsters/invasives-endangered.psv` — raw INVASIVE + ENDANGERED categorical data
- `grep "INVASIVE" monsters/monsters.psv` — invasive monsters with full stats
- `grep "^Invasive" monsters/monsters.psv | cut -d'|' -f1,4-10` — invasive resistances

## See Also

- [monsters.md](monsters.md) — full enemy catalog
- [../habitats/habitats.md](../habitats/habitats.md) — night/day mechanics, ecosystem rank
- [../monsties/monsties.md](../monsties/monsties.md) — hatched endangered monsties in tier list
- [../eggs/eggs.md](../eggs/eggs.md) — egg farming for endangered species
