# MHS3 — Monster Hunter Stories 3 Factual Reference Skill

A Claude skill providing verified, non-hallucinated game data for **Monster Hunter Stories 3: Twisted Reflection**.

## Why This Exists

LLMs confidently hallucinate MHS3 data from other Monster Hunter titles (World, Rise, Stories 2). This skill serves as a local source of truth with factual game data sourced from [mhstories3.wiki](https://mhstories3.wiki), [Game8](https://game8.co), and [Les Carnets de la Wycadémie](https://lescarnetsdelawycademie.fr/building-the-perfect-monstie/).

## Architecture

Designed for Sonnet and lighter models with progressive context loading:

```
mhs3/
├── SKILL.md                          (~1.1K tokens — always loaded, routing + core mechanics)
├── references/
│   ├── monsties.md                   (~2K tokens — all 84 monsties + tier list + Elder Dragon unlock)
│   ├── genes-and-builds.md           (~1.9K tokens — gene system, affinity effects, bingo, passives, builds)
│   ├── building-guide.md             (~1.8K tokens — tendencies, dual element, ecosystem rank, archetypes)
│   ├── combat-weapons.md             (~1K tokens — PST triangle, H2H, weapons, field tips)
│   ├── eggs.md                       (~1.2K tokens — patterns, potency, locations, SR tickets, farming)
│   └── battle-allies.md              (~750 tokens — 6 partners, tier rankings, scenario picks)
└── README.md
```

**Typical query**: ~2–3K tokens (SKILL.md + 1 reference file)
**Full load**: ~10K tokens (all files)

## What's Covered

- **84 monsties** — element, attack type, rank, region, species classification
- **Gene system** — 3×3 grid, Bingo mechanics (multiplicative stacking), Rainbow Gene strategy
- **Affinity Effects** — all 16 skill modifier suffixes (STR, ATK, SKL, CRFT, etc.)
- **Passive skills** — full table with actual stat values from in-game testing
- **Tier list** — S through D rankings with search flag for post-launch updates
- **Combat** — PST triangle, Head-to-Head, Double Attacks, Kinship, Wyvernsoul
- **Weapons** — all 6 types with damage categories and mechanics
- **Eggs** — patterns by genus, potency levels, locations by region, SR Expedition Tickets
- **Battle allies** — all 6 partners with weapons, elements, monsties, per-scenario recommendations
- **Advanced building** — tendencies, dual element math, ecosystem rank, excursion bonuses, build archetypes
- **Elder Dragons** — unlock pipeline, unique abilities, night-only spawns

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
