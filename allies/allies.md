# Battle Allies (Partners) — MHS3

You bring **one partner per quest**. Each has a fixed weapon, element, attack type, and companion monstie. 6 unlockable partners + Ratha-line starting companion.

## Unlocks

New ranger equipment and monsties for partners are unlocked by **completing Side Stories** — not crafting or main story.

## Roster

| Tier | Name | Type | Weapon | Element | Monstie | Monstie Type |
|---|---|---|---|---|---|---|
| S | Ogden | Technical | Hunting Horn | Non-Elem | Chirpy | Tech/Non-Elem |
| A | Kora | Power | Gunlance | Fire | Gravy | Fire/Power |
| A | Simon | Speed | Long Sword | Thunder | Fawn | Ice/Speed |
| B | Thea | Speed | Bow | Thunder | Kagachi | Thunder/Speed |
| B | Eleanor | Power | Great Sword | Fire | Angie | Fire/Power |
| C | Gaul | Speed | Long Sword | Ice | Legia | Ice/Speed |

## Partner Details

### Ogden (S Tier) — Best Overall

- **Role**: Buffer/Controller (Hunting Horn)
- **Strengths**: Party-wide ATK/DEF buffs, boss trap setups, Wyvernfell burst, works in every composition
- **Weaknesses**: Lower personal DPS, Chirpy has average coverage
- **When**: Default choice. Every team benefits from Ogden

### Kora (A Tier) — Tank

- **Role**: Damage soak, aggro redirect
- **Strengths**: Highest HP/DEF of all partners, Taunt redirects attacks, Gravy (Fire/Power) essential for hard content
- **Weaknesses**: Low damage, Fire overlaps with Eleanor
- **When**: Hard bosses, survival priority

### Simon (A Tier) — Early DPS

- **Role**: Fast Thunder damage dealer
- **Strengths**: Strong evasion, available from Act 1, Fawn (Ice/Speed) fills an early gap
- **Weaknesses**: Falls off endgame, Thunder overlap with Thea
- **When**: Acts 1–2 when Thunder coverage matters

### Thea (B Tier) — Status Specialist

- **Role**: Ranged status applicator
- **Strengths**: Poison/Paralysis, ranged (avoids melee AoE), Kagachi (Thunder/Speed) synergy
- **Weaknesses**: Lower damage than Simon, status useless vs high-resist bosses
- **When**: Fights where status sticks

### Eleanor (B Tier) — Glass Cannon

- **Role**: Burst Power damage
- **Strengths**: Highest burst damage, Great Sword dominates H2Hs, Angie doubles Fire/Power — speed clears
- **Weaknesses**: Fragile, Fire useless vs fire-resistant foes, late unlock
- **When**: Speed clears; pair with Ogden/Kora

### Gaul (C Tier) — Sustain

- **Role**: Party sustain, item conservation
- **Strengths**: Best self-sustain, Ice covers Dragon-weak, Legia (Ice/Speed), long expeditions
- **Weaknesses**: Lowest damage, healing less valuable than buffs/prevention
- **When**: Marathon exploration runs

## Recommended Partner by Scenario

| Scenario | Best Pick | Why |
|---|---|---|
| Story progression | Ogden | Buffs smooth any encounter |
| Early game (Acts 1–2) | Simon | Available early, Thunder + Ice |
| Hard boss fights | Kora or Ogden | Survival + buffs |
| Speed clears | Eleanor | Highest burst |
| Status-heavy fights | Thea | Debuffs reduce boss threat |
| Long expeditions | Gaul | Conserves items |

## Deep Lookup

- `cat allies/partners.psv` — 6 partners × monsties/region skills/unlock missions
- `grep "Ogden" allies/partners.psv` — unlock flags for Ogden

## See Also

- [../monsties/monsties.md](../monsties/monsties.md) — your own monsties (separate system)
- [../zones/](../zones/) — where each partner's Side Stories are accessible
