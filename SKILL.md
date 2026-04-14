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

This skill is the **source of truth** for Monster Hunter Stories 3: Twisted Reflection.
LLMs will hallucinate MHS3 data from MH World, Rise, or Stories 2. **Never answer MHS3
questions from training data alone.** Always load the appropriate reference file first.

## CORE FACTS (always in context)

### Game Overview
- **Title**: Monster Hunter Stories 3: Twisted Reflection
- **Launch**: March 13, 2026 | PS5, Xbox Series X|S, Switch 2, PC (Steam)
- **Genre**: Turn-based RPG (NOT action — this is the Stories spinoff)
- **Monsties**: 88 hatchable | Ranks 1–7
- **Regions**: Azuria (start), Canalta (mid), Tarkuan (mid-late), Serathis (late)
- **Multiplayer**: PvP Network Battles only. **No co-op.** Story is single-player.

### Starter Monsties
- **Ratha (Rathalos)**: Fire/Power — your first monstie, King of the Skies
- **Tobi-Kadachi**: Thunder/Speed — early addition
- **Yian Kut-Ku**: Fire/Speed — early addition
These three cover Power + Speed (no early Technical — fill this gap from dens)

### Day/Night Cycle
- Different monsters spawn day vs night; some are night-exclusive
- Elder Dragons (post-game) are **night-only** spawns
- Rest at camp to change time of day

### Attack Type Triangle
```
Power (red)  → beats Speed
Speed (blue) → beats Technical
Technical (green) → beats Power
```

### Elemental Matchups
| Element   | Strong vs | Weak to |
|-----------|-----------|---------|
| Fire      | Ice       | Water   |
| Water     | Fire      | Thunder |
| Thunder   | Water     | Ice     |
| Ice       | Thunder   | Fire    |
| Dragon    | Dragon    | Dragon  |
| Non-Elem  | —         | —       |

### Weapon Types (6 total)
| Weapon       | Damage  | Mechanic             |
|--------------|---------|----------------------|
| Great Sword  | Slash   | Charge Gauge         |
| Long Sword   | Slash   | Spirit Gauge/Stances |
| Hammer       | Blunt   | Stun / Head targeting|
| Hunting Horn | Blunt   | Melody buffs (RGB)   |
| Bow          | Pierce  | Coatings / Status    |
| Gunlance     | Pierce  | Shells / Guard       |

Slash → tails/wings | Blunt → heads/shells | Pierce → bodies/soft spots

### Rite of Channeling (MHS3 change from MHS2)
- **No monstie sacrifice required** — transfer genes freely between monsties
- Genes can be rearranged within a monstie's grid at any time
- Use Gene Search (L3/V) to find which species carry specific genes

## READING SCREENSHOTS

When the user shares a monstie screenshot, the icons next to the monstie name read:
**(attack type) (element) (bonus element)**

- First icon: Power (red triangle) / Speed (blue triangle) / Technical (green triangle)
- Second icon: Primary element (Fire/Water/Thunder/Ice/Dragon/Non-Elem)
- Third icon: Bonus element from Dual Element system (absent if single-element)

The stat panel shows: HP, Attack, Crit Rate, Wyvernfell, Speed, Defense, Stamina (Starting/Max/Recovery), Kinship Gauge, Elem Res, and the 3×3 gene grid.

**Caution icon**: The dragon-shaped icon above overworld monsters (red/yellow) means the monster is a much higher level than you. Can be toggled in Options > Game Settings > Caution Icon Display.

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
1. Freely reference zones 1 through N (current zone and earlier)
2. For zone N+1+: do NOT name specific monsties, weapons, armor, or story events
3. If the best answer requires future-zone data, say: "There's a better option available later. Want me to share it?"
4. Gene farming: offer best CURRENT-zone source first, then mention "better versions exist later" without naming the monster
5. Post-game/Elder Dragon content is ALWAYS gated unless user has post-game context
6. **Opt-out**: If user says "I don't care about spoilers" or similar, disable spoiler gates for the conversation

**Zone-aware recommendations**: When the user asks "what should I build?" or "best X for my zone?", filter weapons (Zone column), armor (Zone column), and gene sources by their current zone or earlier.

## REFERENCE FILE ROUTING

Based on the user's question, load the appropriate reference file **before answering**.

| Question About | Load This File | Examples |
|---|---|---|
| Monstie stats, locations, types, riding actions | `references/monsties.md` | "What type is Zinogre?" "Where do I find Deviljho?" |
| Tier rankings, best monsties, team composition, regional teams | `references/monsties.md` (tier section) | "Best monsties?" "S tier?" "Best team for Canalta?" |
| Gene system, bingo, passive skills, builds, affinity effects | `references/genes-and-builds.md` | "Best genes for Nergigante?" "How does bingo work?" |
| Gene farming — which monstie carries a gene, what zone | `references/gene-sources.md` | "Where do I get Critical Eye?" "Genes in Canalta?" |
| Combat mechanics, head-to-head, kinship, weapon mechanics | `references/combat-weapons.md` | "How do double attacks work?" "How does spirit gauge work?" |
| Comparing weapons across types, general weapon recs | `references/weapons-index.md` | "Best fire weapon?" "Weapon comparison" |
| Specific Great Sword options | `references/weapons-great-sword.md` | "Best great sword?" "GS with dragon element?" |
| Specific Long Sword / Katana options | `references/weapons-long-sword.md` | "Best long sword?" "Kadachi katana?" |
| Specific Hammer options | `references/weapons-hammer.md` | "Best hammer?" "Blunt weapons list?" |
| Specific Hunting Horn options | `references/weapons-hunting-horn.md` | "Best hunting horn?" "HH with healing?" |
| Specific Bow options | `references/weapons-bow.md` | "Best bow?" "Bow with paralysis?" |
| Specific Gunlance options | `references/weapons-gunlance.md` | "Best gunlance?" "GL with fire?" |
| Armor sets, defense, armor skills | `references/armor.md` | "Best fire armor?" "Armor with crit skills?" |
| Skills, decorations, weapon decos, armor decos, deco slots | `references/skills-and-decorations.md` | "What does Attack Boost do?" "How do decorations work?" "What decos for my bow?" |
| Egg identification, patterns, den types, potency | `references/eggs.md` | "What pattern is an Elder Dragon egg?" |
| Advanced building: tendencies, dual element, ecosystem rank | `references/building-guide.md` | "How do tendencies work?" |
| Battle allies / partner characters | `references/battle-allies.md` | "Who should I bring?" "Best partner?" |
| Zone-specific progression advice | `zones/{region}.md` | "What should I do in Canalta?" "Best build for Azuria?" |

**Weapon routing heuristic**: If the user names a weapon TYPE, load that type's file. If comparing across types, load `weapons-index.md`. If asking about weapon MECHANICS (charge gauge, spirit gauge, coatings), load `combat-weapons.md`. Weapon and armor files now have a **Zone column** — use it to filter recommendations by player progression.

**If the question spans multiple domains**, load the most relevant file first, answer that part, then load additional files as needed.

## SEARCH FLAG: WHEN TO SEARCH THE WEB

The local data is based on launch-window sources (March–April 2026). **Search the web** when:
- User asks about **balance patches or updates** after launch
- User asks about **DLC monsties** or new content drops
- User asks about **current meta** or whether tier rankings have shifted
- User references a **monstie, gene, or mechanic you don't find** in the reference files
- User asks about **community discoveries** or speedrun strategies

When searching, prefer these sources: mhstories3.wiki, game8.co (MHS3 section),
lescarnetsdelawycademie.fr, monsterhunterwiki.org (MHST3 pages).

## ANTI-HALLUCINATION RULES

1. If a monstie is NOT in `references/monsties.md`, do NOT guess its stats — say it's not in your database and offer to search.
2. Do NOT mix MHS3 data with MH World, Rise, Sunbreak, or Stories 2 mechanics. They differ significantly.
3. Gene names, skill effects, and stat numbers must come from the reference files or a verified search. Never fabricate gene effects.
4. MHS3 has **no co-op multiplayer**. Only PvP Network Battles. Do not claim otherwise.
5. The Rite of Channeling does **not** sacrifice the donor monstie in MHS3. This changed from MHS2.
