# Elder Dragons — MHS3

Post-game endgame content. Rank 7 hatchable monsties AND the game's toughest boss fights.

## Unlock Pipeline

1. **Complete main story** and defeat the final boss.
2. Unlocks **High Rank expeditions**.
3. Elder Dragons spawn at **night only** in random regions.
4. Use **SR Expedition Tickets** (100 Bottle Caps each at Bottle Cap Trader) for **guaranteed high-rank dens**.
5. Elder Dragon eggs have a distinctive **star pattern** — look for them in SR dens at night.

## The Eight Elder Dragons

| Name | Element | Type | Signature Ability | PvE Notes |
|---|---|---|---|---|
| **Nergigante** | Dragon | P | Self-healing spikes — regenerates HP as it deals damage | Top PvE; farm for Ruiner |
| **Ruiner Nergigante** | Dragon | P | Enhanced self-heal + strongest raw Power damage | **Best PvE endgame monstie** |
| **Velkhana** | Ice | T | **Skill Seal** — disables opponent skills | **PvP dominant** |
| **Teostra** | Fire | P | Explosive fire burst — Emperor of Flame, devastating Power/Fire | Supernova AoE |
| **Kushala Daora** | Ice | S | Wind disruption — fast, hard to pin, battlefield control | Evasive fighter |
| **Namielle** | Water | T | Water/lightning hybrid AoE — unique dual-element Technical | Storm Veil grants 4 party buffs |
| **Kirin** | Thunder | S | Thunder evasion — fast, hard to hit, Speed/Thunder specialist | Glass cannon |
| **Yama Tsukami** | Dragon | T | Environmental control — unique battlefield manipulation | Complex fight |

## Slay vs Repel

**Slaying** a Calamitous Elder Dragon unlocks the **Heroic Testament** armor decoration:
- +max HP, +damage dealt, -damage taken
- Upgrades S → M → L → XL with each slay
- **Repelling does NOT count** — you must slay to progress the tier

Slaying requires:
- High-rank gear + Rank 7 monstie party
- Element-appropriate weapon (mind the Elder Dragon's resists)
- Kinship uptime (SR ticket runs are stamina-intensive)

## Genes to Farm from Elder Dragons

| Elder | Signature Genes |
|---|---|
| Nergigante | Power Rise (S), Tenacity (M), All-Elem Def Boost (M) |
| Ruiner Nergigante | Crit-Heal (XL), Dragon Atk Boost (S) |
| Velkhana | **Skill Seal (XL)**, **Panacea (XL)**, Evasion (S), Ice Atk Boost (S) |
| Teostra | Supernova (M), Warmth (L), Fire Atk Boost (M+), Elder Seal (S–M) |
| Kushala Daora | Wind-based evasion genes |
| Namielle | Water Atk Boost, Storm Veil (buff-stacking active) |
| Kirin | Thunder-based evasion genes |
| Yama Tsukami | Battlefield-manipulation actives |

For farming specifics, see [../genes/sources.md](../genes/sources.md) Post-game section.

## Recommended Setup

### For Slaying (Damage)

| Role | Pick |
|---|---|
| DPS Monstie | **Ruiner Nergigante** (Power/Dragon, Self-Heal + crit) OR **Boltreaver Astalos** (Technical/Thunder, crit-kinship) |
| Support Monstie | **Namielle** (Storm Veil = 4 buffs) OR **Malzeno** (self-sustain + Dragon) |
| Weapon | Element-appropriate (Fire for Velkhana, Ice for Teostra, Dragon if neutral) |
| Armor | **Rimeguard** (endgame survival) or **Rath Soul** (endgame DPS) |
| Partner | **Ogden** (default) or **Kora** (tank-up for Teostra) |

### For Repelling (Gene Farming)

You can repel elder dragons — the fight ends when their first HP gauge hits zero and they flee. Faster than slaying, still drops some genes. Use glass-cannon monsties + burst damage.

## Fight Notes by Elder

**Velkhana**: applies Skill Seal → you lose access to ALL skills for multiple turns. Counter with **Sealbreaker** armor passive or **Zest Pill** items. Velkhana is the only source of Skill Seal (XL) — the PvP top-tier gene.

**Teostra**: Supernova is unavoidable AoE that hits hard. High Fire Defense armor + Fire-resistant monsties (Rathalos, etc.) mandatory. Ice monsties (Velkhana, Barioth) excellent offensive pick.

**Nergigante**: self-healing spikes mean damage races. Out-DPS its regen, or use Partbreaker to destroy spikes and disable the heal.

**Kushala Daora**: wind status reduces accuracy. Apply Accuracy Down coatings back, or just bring high-crit Power monsties.

**Namielle**: dual-element (Water + Thunder). Both elements resist means you need neutral Dragon damage or break her element gauge.

**Kirin**: extremely evasive. Bring **Accuracy Up**, Partbreaker for horn break.

**Yama Tsukami**: battlefield control. Each phase shifts the fight mechanics. Rotate monsties to match phases.

## Deep Lookup

- `grep "^Nergigante" monsters/monsters.psv` — enemy stats + resistances
- `grep "^Nergigante" monsties/monsties.psv` — if you have one hatched, monstie stats
- `grep "ID_PARTS_EM0{xx}" monsters/parts.psv` — part-break data for each elder
- `grep "Nergigante" monsters/monster-book.psv` — lore / habitat

## See Also

- [monsters.md](monsters.md) — all enemy stats
- [parts.md](parts.md) — part-break targeting
- [../monsties/monsties.md](../monsties/monsties.md) — hatched monstie versions (tier list)
- [../genes/sources.md](../genes/sources.md) — gene farming by monster
- [../eggs/eggs.md](../eggs/eggs.md) — SR tickets, night farming
- [../zones/postgame.md](../zones/postgame.md) — post-game zone advisor
