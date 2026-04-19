---
name: mhs3
description: >
  Factual reference database for Monster Hunter Stories 3: Twisted Reflection (MHS3).
  Use this skill whenever the user asks ANYTHING about MH Stories 3 — monsties, genes,
  builds, eggs, combat, weapons, tier lists, walkthrough advice, or game mechanics.
  This skill exists because LLMs confidently hallucinate MH data from other titles
  (MH Rise, MH World, MH Stories 2). ALWAYS consult this skill instead of relying on
  training data for MHS3-specific facts. Trigger on: Monster Hunter Stories 3, MHS3,
  MH Stories 3, monsties, monstie builds, gene bingo, rite of channeling, egg patterns,
  kinship gauge, head-to-head, Azuria, Canalta, Tarkuan, Serathis, Twisted Reflection,
  or any monster name in a Stories 3 context.
---

# MHS3 Factual Reference Skill

## PURPOSE

**Source of truth** for Monster Hunter Stories 3: Twisted Reflection. LLMs will hallucinate MHS3 data from MH World, Rise, or Stories 2 — **do not answer MHS3 questions from training data alone**. Load the appropriate domain cheat sheet first.

## ARCHITECTURE (3 tiers)

1. **SKILL.md** (always in context) — router, core facts, grep patterns, spoiler protocol.
2. **`{domain}/{domain}.md` cheat sheets** (routed load) — curated "best picks / key mechanics / deep lookup" overviews.
3. **`{domain}/*.psv` lookup data** (grep-addressable, never loaded whole) — raw catalog rows for deep lookup. Pipe-separated. First two lines are generation header + schema.

**Flow for a query**: match topic → load the domain's cheat sheet → grep the PSV if deeper detail is needed.

## CORE FACTS (always in context)

### Game Overview

- **Title**: Monster Hunter Stories 3: Twisted Reflection
- **Launch**: March 13, 2026 | PS5, Xbox Series X|S, Switch 2, PC (Steam)
- **Genre**: Turn-based RPG (NOT action — the Stories spinoff)
- **Monsties**: 88 hatchable | Ranks 1–7
- **Regions**: Azuria (start) → Canalta → Tarkuan → Serathis → Post-game (Elder Dragons)
- **Multiplayer**: PvP Network Battles only. **No co-op.** Story is single-player.

### Starter Monsties

- **Ratha (Rathalos)**: Fire/Power — your first monstie, King of the Skies
- **Tobi-Kadachi**: Thunder/Speed — early addition
- **Yian Kut-Ku**: Fire/Speed — early addition

Starters cover Power + Speed (no early Technical — fill this gap from dens).

### Attack Type Triangle

```
Power (red)       → beats Speed
Speed (blue)      → beats Technical
Technical (green) → beats Power
```

### Elemental Matchups

| Element | Strong vs | Weak to |
|---|---|---|
| Fire | Ice | Water |
| Water | Fire | Thunder |
| Thunder | Water | Ice |
| Ice | Thunder | Fire |
| Dragon | Dragon | Dragon |
| Non-Elem | — | — |

### Weapon Types (6)

| Weapon | Damage | Mechanic |
|---|---|---|
| Great Sword | Slash | Charge Gauge |
| Long Sword | Slash | Spirit Gauge / Stances |
| Hammer | Blunt | Stun / Head targeting |
| Hunting Horn | Blunt | Melody buffs (party support) |
| Bow | Pierce | Coatings / Status |
| Gunlance | Pierce | Shells / Guard |

Slash → tails/wings | Blunt → heads/shells | Pierce → bodies/soft spots

### Rite of Channeling (key MHS3 change from MHS2)

- **No monstie sacrifice required** — transfer genes freely between monsties
- Genes can be rearranged within a monstie's grid at any time
- Use Gene Search (L3/V) to find which species carry specific genes

## READING SCREENSHOTS

### Monstie Header Icons

When the user shares a monstie screenshot, the icons next to the monstie name read:
**(attack type) (element) (bonus element)**

- First: Power (red triangle) / Speed (blue triangle) / Technical (green triangle)
- Second: Primary element (Fire/Water/Thunder/Ice/Dragon/Non-Elem)
- Third: Bonus element from Dual Element system (absent if single-element)

### Stat Panel

HP, Attack, Crit Rate, Wyvernfell (36–60 base + bingo bonus), Speed, Defense, Stamina (Starting/Max/Recovery), Kinship Gauge, Elem Res, 3×3 gene grid.

### Gene Grid Visual Language (3×3)

**Color = Element**: Fire (red), Water (blue), Thunder (yellow), Ice (light blue/cyan), Dragon (purple), Non-Elem (grey/white), Rainbow Gene (multicolored).

**Icon = Attack Type**: Power (claw/fist), Speed (wing/feather), Technical (eye/target), No Type (blank).

**Border = Tier**: S/M thin, L thicker, XL prominent glow.

**Bingo lines**: Completed bingo lines glow across the grid.

### Skill Description Display

Name + affinity suffix (e.g., "Charged Slash (BRK)"). Three stats: **Power / Wyvernfell / Stamina cost**. Type icon (P/S/T). Element icon. Active vs Passive indicator.

### Overworld Icons

**Caution icon** (dragon shape, red/yellow): monster is much higher level than you. Toggle in Options > Game Settings > Caution Icon Display.

## PROGRESSION CONTEXT & SPOILER PROTOCOL

**Zone order**: Azuria (1) → Canalta (2) → Tarkuan (3) → Serathis (4) → Post-game (5)

**Detect player context** from their messages:
- "I'm in Azuria" / "early game" / "just started" → Zone 1
- "I'm in Canalta" / "mid game" → Zone 2
- "I'm in Tarkuan" / "mid-late" → Zone 3
- "I'm in Serathis" / "late game" → Zone 4
- "post-game" / "beat the story" / "elder dragons" → Zone 5
- If unclear, ask: "Which region are you in? This helps me avoid spoilers."

**Spoiler rules** (when player context is known):
1. Freely reference zones 1 through N (current and earlier)
2. For zone N+1+: do NOT name specific monsties, weapons, armor, or story events
3. If best answer requires future-zone data, say: "There's a better option available later. Want me to share it?"
4. Gene farming: offer best CURRENT-zone source first, then mention "better versions exist later" without naming
5. Post-game / Elder Dragon content is ALWAYS gated unless user has post-game context
6. **Gear material sources**: In-game, crafting materials show as **???** until discovered. When asked "what materials do I need for X armor/weapon?", **ask if they want spoilers** before revealing source monster. Lookup tables are for internal resolution (e.g., "Pink Rathian armor" → Rath Heart) — use freely for identification, but gate the material source reveal.
7. **Opt-out**: "I don't care about spoilers" disables spoiler gates for the conversation.

**Zone-aware recommendations**: When user asks "what should I build?" or "best X for my zone?", filter weapons/armor/gene sources by their current zone or earlier (use the Zone column in weapons-per-type or armor data).

## ROUTING TABLE

Find the user's question topic below; load the cheat sheet, then grep the PSV if needed.

| Question type | Load cheat sheet | Deep PSV lookup |
|---|---|---|
| Monstie stats, locations, tier rankings | `monsties/monsties.md` | `grep "^{Name}\|" monsties/monsties.psv` |
| By-species classification (Flying/Brute/Leviathan/etc.) | `monsties/species-guide.md` | — |
| Riding actions (swim/fly/climb/dig/stealth) | `monsties/riding-actions.md` | `grep "^{Name}\|" monsties/riding-actions.psv` |
| Gene mechanics, bingo, affinity, rainbow, passive tier values | `genes/genes.md` | `grep -i "skill" skills/passive-skills.psv` |
| Gene → monstie farming | `genes/sources.md` | — (supplement from MonsterBuddy if needed) |
| Build archetypes + **stamina rotations** | `genes/builds.md` | `grep -i "^{Name}" monsties/monsties.psv` for base stats |
| Combat mechanics (PST/H2H/Kinship/Wyvernfell/status effects) | `combat/combat.md` | — |
| Per-weapon mechanics (Charge Gauge, Spirit Gauge, Melodies, Coatings, Shells) | `combat/weapon-mechanics.md` | — |
| Cross-type weapon picks, role/zone best-in-slot | `weapons/weapons.md` | — |
| Specific weapon type | `weapons/{type}/{type}.md` | `cat weapons/{type}/weapons.psv` |
| Per-level weapon attack / material costs | same | `grep "^{name}" weapons/{type}/params.psv` |
| Armor sets, defense, skills, monster→armor lookup | `armor/armor.md` | `cat armor/armor.psv` |
| Armor decorations (passive skills, Heroic Testament, tiers) | `armor/decos.md` | `cat armor/decos.psv` |
| Weapon decorations (active skills by type) | `weapons/decos.md` | `cat weapons/decos.psv` + per-type weapons.psv |
| Hunting Horn melodies | `weapons/hunting-horn/melodies.md` | `cat weapons/hunting-horn/melodies.psv` |
| Active skills catalog (damage, Wyvernfell, buffs) | `skills/active-skills.md` | `grep -i "{name}" skills/active-skills.psv` |
| Passive skills catalog (tier values) | `skills/passive-skills.md` | `grep -i "{name}" skills/passive-skills.psv` |
| Buffs / debuffs (names, effects, sources) | — | `grep -i "{name}" skills/buffs-debuffs.psv` |
| Enemy monsters (non-hatchable, bosses, invasives) | `monsters/monsters.md` | `grep "^{Name}\|" monsters/monsters.psv` |
| Part breaks (Slash/Blunt/Pierce per part) | `monsters/parts.md` | `grep "^ID_PARTS_{EM_code}" monsters/parts.psv` |
| Elder Dragons (unlock, spawn, fight notes) | `monsters/elder-dragons.md` | — |
| Invasive / Endangered categories | `monsters/invasives-endangered.md` | `cat monsters/invasives-endangered.psv` |
| Monster lore / regions / trace items | — | `grep "^{Name}\|" monsters/monster-book.psv` |
| Enemy level scaling per stage | — | `grep "{name}" monsters/enemy-levels.psv` |
| Monster skills (what moves enemies use) | — | `grep -i "{name}" monsters/enemy-skills.psv` |
| Spawns, day/night, mutations, ecosystem rank, dual-element farming | `habitats/habitats.md` | `cat habitats/{nests\|ecology-rank\|mutations}.psv` |
| Excursions, Environment Skills, stat bonuses | `excursions/excursions.md` | — |
| Eggs (patterns, potency, dens, SR tickets) | `eggs/eggs.md` | — |
| Egg Powers (S/A/B tier skills on eggs) | `eggs/egg-powers.md` | `grep "^Egg Skill:" skills/active-skills.psv` |
| Items (potions, traps, paintball, tickets, crafting recipes) | `items/items.md` | `grep -i "{name}" items/items.psv`, `cat items/recipes.psv` |
| Meals / Kitchen | `items/meals.md` | `cat items/meals.psv` |
| Battle Allies / partners (Ogden/Kora/Simon/Thea/Eleanor/Gaul) | `allies/allies.md` | `cat allies/partners.psv` |
| Rider level scaling | `progression/rider.md` | `grep "^{level}\|" progression/rider.psv` |
| Stages / region map | `progression/stages.md` | `cat progression/stages.psv` |
| PvP / Network Battles | `multiplayer/network-battles.md` | — |
| Zone-specific progression advice | `zones/{region}.md` | — |

**If the question spans multiple domains**, load the most relevant cheat sheet first, answer that part, then load additional domain files as needed.

## GREP PATTERN EXAMPLES

PSV rows start with the key field (monstie name, weapon name, part ID, etc.). Typical patterns:

```bash
# Monstie base stats (including bingo bonuses)
grep "^Rathalos|" monsties/monsties.psv

# All Rathalos-family weapons (any type)
grep -i "rathalos" weapons/*/weapons.psv

# Per-level upgrade progression for one weapon
grep "^Epitaph Blade" weapons/great-sword/params.psv

# All armor with a specific passive skill
grep -i "Critical (XL)" armor/armor.psv

# All XL-tier passive skills
grep "(XL)" skills/passive-skills.psv

# Parts of a specific monster (need the EM code — resolve via monster-book.psv first)
grep "^ID_PARTS_EM0001" monsters/parts.psv

# Monster Book: lore + regions + trace items
grep "^Rathalos|" monsters/monster-book.psv

# Find which zones an enemy spawns in with levels
grep "Rathalos" monsters/enemy-levels.psv

# Nest contents for one area
grep "^A100" habitats/nests.psv
```

**Never load a PSV whole** unless grep returns nothing and you must browse. These are lookup files, not read-whole files.

## BUILD PLANNER (cross-file routing)

When user asks "best build for X?", pull from multiple domains:

| Role | Monstie (monsties.md) | Weapon (weapons.md) | Armor (armor.md) | Genes (builds.md) |
|---|---|---|---|---|
| **DPS** | Boltreaver Astalos, Magnamalo, Ruiner Nergigante, Dreadking Rathalos | Epitaph Blade (GS), Reaver "Cruelty" (LS), Diablos Hammer | Rath Soul (Crit XL, Crit Kinship L, All-Out L) | Glass Cannon archetype |
| **Wyvernsoul Topple** | Deviljho (Dragonblast), Chatacabra (61 WF), Paolumu (60 WF) | Yeti Hammer, Spongia Bow, Veldian Sibilus (HH) | Goss Harag (Dragon Buster L), Diablos Nero | Wyvernsoul Topple archetype |
| **Status Control** | Espinas (Para+Poison), Brute Tigrex (AoE Stun), Dreadqueen Rathian | Veldian Arcum (Bow), Iceflinger (Bow) | Espinas Armor (Inflict Rate Up L, Salt in Wound M) | Status Disruptor archetype |
| **Tank / Sustain** | Malzeno (self-heal), Namielle (4-buff Storm Veil), Dreadqueen Rathian | Lagia Burst (GL), Aknosom GL | Rimeguard (Kinship Skill+ XL, Divine Blessing L), Malzeno Armor (Self-Heal XL) | Tank/Sustain archetype |
| **Support** | Canyne (Palamute), Namielle | Hydros Horn (HH), Duke's Grail (HH) | Aelucanth (Synchronize XL, Stamina Surge L) | Support Palamute archetype |
| **Crit-Kinship** | Ruiner Nergigante, Boltreaver Astalos, Magnamalo | Any high-skill-count weapon | Rath Soul, Zinogre U (Dragon Atk Boost XL) | Crit-Kinship Engine archetype |

**Zone-aware**: Filter recommendations by player's current zone. If best-in-slot is in a future zone, offer current-zone alternative first + mention future option (spoiler gated).

**When user asks about a specific weapon type or monstie**: Start with their choice, then recommend best role-matching armor + genes. Don't force a role — adapt to what they're using.

## STAMINA ROTATION QUICK REFERENCE

Identify the monstie's Stamina Regen total (base + bingo + habitat + Stamina Surge XL + meals) → find the breakpoint:

| Regen | Rotations |
|---|---|
| ≤9 | Burst build |
| 10–11 | (10, repeat), (0, 20) |
| 15–16 | (15), (10, 20), (0, 30), (10, 10, 25) |
| 20–21 | (20), (15, 25), (10, 30) — **Fruit Frenzy+ spam, meta** |
| 25–26 | (25), (20, 30) — **Immortal Dog / Devour+ spam, cheesy** |

Full table: `genes/builds.md` Stamina Archetypes section.

## SEARCH FLAG: WHEN TO SEARCH THE WEB

Local data is from launch window (March–April 2026). **Search the web** when:
- User asks about **balance patches or updates** after launch
- User asks about **DLC monsties** or new content drops
- User asks about **current meta** or whether tier rankings have shifted
- User references a **monstie, gene, or mechanic** not in the reference files
- User asks about **community discoveries** or speedrun strategies

Prefer these sources: mhstories3.wiki, game8.co (MHS3), monsterbuddy.app/3, lescarnetsdelawycademie.fr.

## ANTI-HALLUCINATION RULES

1. If a monstie is NOT in `monsties/monsties.psv`, do NOT guess its stats — say it's not in the database and offer to search.
2. Do NOT mix MHS3 data with MH World, Rise, Sunbreak, or Stories 2 mechanics. They differ significantly.
3. Gene names, skill effects, and stat numbers must come from the reference files or a verified search. Never fabricate.
4. MHS3 has **no co-op multiplayer**. Only PvP Network Battles. Do not claim otherwise.
5. The Rite of Channeling does **not** sacrifice the donor monstie in MHS3. This changed from MHS2.
