# MHS3 — Monster Hunter Stories 3 Factual Reference Skill

A Claude skill providing verified, non-hallucinated game data for **Monster Hunter Stories 3: Twisted Reflection**.

## Why This Exists

LLMs confidently hallucinate MHS3 data from other Monster Hunter titles (World, Rise, Stories 2). This skill serves as a local source of truth with factual game data sourced from [mhstories3.wiki](https://mhstories3.wiki), [Game8](https://game8.co), and [Les Carnets de la Wycadémie](https://lescarnetsdelawycademie.fr/building-the-perfect-monstie/).

## Architecture

Designed for Sonnet and lighter models with progressive context loading. Hybrid architecture: global reference files for direct factual lookups + zone advisor files for progression-aware recommendations.

```
mhs3/
├── SKILL.md                          (~1.8K tokens — routing, core mechanics, spoiler protocol, screenshot rules)
├── references/
│   ├── monsties.md                   (~2.5K tokens — 88 monsties + tier list + regional team recs)
│   ├── genes-and-builds.md           (~2K tokens — gene system, affinity effects, bingo, passives, builds)
│   ├── gene-sources.md               (~1.5K tokens — gene → monstie → region mapping, zone farming guide)
│   ├── building-guide.md             (~1.8K tokens — tendencies, dual element, ecosystem rank, archetypes)
│   ├── combat-weapons.md             (~1K tokens — PST triangle, H2H, weapon mechanics, field tips)
│   ├── weapons-index.md              (~600 tokens — cross-type overview + standout picks)
│   ├── weapons-great-sword.md        (~500 tokens — 29 Great Swords + Zone column)
│   ├── weapons-long-sword.md         (~500 tokens — 29 Long Swords / Katanas + Zone column)
│   ├── weapons-hammer.md             (~600 tokens — 37 Hammers + Zone column)
│   ├── weapons-hunting-horn.md       (~500 tokens — 29 Hunting Horns + Zone column)
│   ├── weapons-bow.md                (~400 tokens — 19 Bows + Zone column)
│   ├── weapons-gunlance.md           (~400 tokens — 17 Gunlances + Zone column)
│   ├── armor.md                      (~1.5K tokens — ~85 armor sets sorted by defense + Zone column)
│   ├── skills-and-decorations.md     (~800 tokens — skill system overview + decoration mechanics)
│   ├── eggs.md                       (~1.2K tokens — patterns, potency, locations, SR tickets, farming)
│   └── battle-allies.md              (~750 tokens — 6 partners, tier rankings, scenario picks)
├── zones/                            (curated progression advisors — NOT data copies)
│   ├── azuria.md                     (~500 tokens — early game progression guide)
│   ├── canalta.md                    (~500 tokens — mid game progression guide)
│   ├── tarkuan.md                    (~500 tokens — mid-late game progression guide)
│   ├── serathis.md                   (~500 tokens — late game progression guide)
│   └── postgame.md                   (~500 tokens — elder dragons & endgame guide)
└── README.md
```

**Typical query**: ~2–3K tokens (SKILL.md + 1 reference file)
**Zone advisory**: ~2.3K tokens (SKILL.md + zone file)
**Full build planning**: ~5.5K tokens (SKILL.md + zone + genes + gene-sources)
**Full load**: ~18K tokens (all files)

Weapon catalog is split by type — asking about Long Swords loads only the 29 katanas (~500 tokens), not all 160+ weapons. All weapon and armor files now include a **Zone column** (Shop/Az/Ca/Ta/Se/PG) for progression-aware filtering.

## What's Covered

- **88 monsties** — element, attack type, rank, region, species classification, regional team recs
- **Gene system** — 3×3 grid, Bingo mechanics (multiplicative stacking), Rainbow Gene strategy
- **Affinity Effects** — all 16 skill modifier suffixes (STR, ATK, SKL, CRFT, etc.)
- **Passive skills** — full table with actual stat values from in-game testing
- **Tier list** — S through D rankings with search flag for post-launch updates
- **Combat** — PST triangle, Head-to-Head, Double Attacks, Kinship, Wyvernsoul
- **Weapon catalog** — 160+ weapons split by type (GS, LS, Hammer, HH, Bow, GL) with elements, deco slots, skills
- **Armor catalog** — ~85 armor sets with defense, deco slots, skills, sorted by defense + top picks by role
- **Skills & decorations** — rider skill system overview, decoration mechanics, common skills reference
- **Eggs** — patterns by genus, potency levels, locations by region, SR Expedition Tickets
- **Battle allies** — all 6 partners with weapons, elements, monsties, per-scenario recommendations
- **Gene sources** — gene → monstie → region mapping for farming answers
- **Advanced building** — tendencies, dual element math, ecosystem rank, excursion bonuses, build archetypes
- **Zone progression** — curated advisor guides for Azuria, Canalta, Tarkuan, Serathis, Post-game
- **Spoiler protocol** — zone-aware recommendations that avoid revealing future content
- **Elder Dragons** — unlock pipeline, unique abilities, night-only spawns
- **Screenshot interpretation** — monstie icon reading (attack type / element / bonus element)

## Data Freshness

Base data sourced from launch window (March–April 2026). The skill includes search flags instructing Claude to web-search for:
- Balance patches and updates
- DLC content
- Meta shifts and tier changes
- Community-discovered strategies

## Installation

Drop the `mhs3/` directory into your project's skill folder, or symlink it:

```bash
# As a project skill
cp -r mhs3/ /path/to/project/.claude/skills/mhs3

# As a user skill (available across all repos)
cp -r mhs3/ ~/.claude/skills/mhs3
```

## Contributing

As you play MHS3, add factual data (screenshots, stat tables, mechanics) via PR. The skill is most valuable for data that models would otherwise fabricate from mainline MH knowledge.

## Sources

- [mhstories3.wiki](https://mhstories3.wiki) — Primary wiki/database
- [Les Carnets de la Wycadémie](https://lescarnetsdelawycademie.fr/building-the-perfect-monstie/) — Advanced building methodology (Masuku)
- [Game8 MHS3](https://game8.co/games/Monster-Hunter-Stories-3/archives/584376) — Monstie data cross-reference
- In-game screenshots and testing
