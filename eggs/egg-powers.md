# Egg Powers — MHS3

Egg Powers (also called "Egg Skills") are special skills tied to eggs, separate from regular genes. Each egg can carry one Egg Power. They provide unique passive effects not available via standard genes.

## Rarity Tiers

Egg Powers have 3 rarity tiers. Higher-rarity = more impactful passive.

| Rarity | Effect Strength |
|---|---|
| **S** | Strongest — signature effects |
| **A** | Mid-tier passives |
| **B** | Minor resilience/utility |

## Catalog

Source: [MonsterBuddy /3/egg-powers](https://monsterbuddy.app/3/egg-powers).

| Power | Rarity | Effect |
|---|---|---|
| **Battle Thirst** | S | Recovers Stamina after winning a H2H or performing a Double Attack |
| **Unscathed** | S | Negates damage after winning a H2H + increases damage dealt |
| **Resonance** | S | Increases Kinship Gauge at battle start |
| **Muster Forces** | S | Increases Kinship Gauge once when losing a Heart |
| **Hardiness** | A | Slightly recovers Stamina after taking damage |
| **High Morale** | A | Slightly extends duration of buffs applied by own skills |
| **Best Buds** | A | Riding Kinship Gauge fills slightly faster |
| **Perseverance** | A | Revives with newly-applied buffs once upon losing a Heart |
| **Pwr Resilience** | B | Slightly reduces Power-type damage taken |
| **Spd Resilience** | B | Slightly reduces Speed-type damage taken |
| **Tech Resilience** | B | Slightly reduces Technical-type damage taken |
| **EX Resilience** | B | Slightly reduces No-Type damage taken |

## Categorization

**By effect type:**
- **Offensive**: Unscathed (H2H damage bonus)
- **Defensive**: Resilience set, Perseverance
- **Kinship**: Resonance, Muster Forces, Best Buds
- **Sustain**: Battle Thirst, Hardiness, High Morale

## Regional Origins

Egg Powers are discovered/drop by region: Azuria, Canalta Timberland, Tarkuan, Serathis. Specific monstie → egg-power mapping not fully documented in launch-window data — grep `monsties/monsties.psv` for egg-power-related columns as they become available, or check MonsterBuddy per-monstie pages.

## Egg-Power-Driven Builds

- **Muster Forces** — Kinship on Heart loss. Pair with high-HP tanks (Dreadqueen Rathian, Malzeno) for a comeback loop.
- **Resonance** — Kinship at battle start. Strong opener for riding early (first-turn Kinship Attack).
- **Unscathed** — Best offensive egg power. Pair with Power-type monsties for guaranteed H2H wins.
- **Best Buds** — Faster riding Kinship. Stack with Soul Kinship (XL) for extreme Kinship uptime.
- **Perseverance** — Auto-revive with buffs. Clutch for hardest content; pair with Buff-heavy setups (Solar Cry, Storm Veil).

## Deep Lookup

Egg Powers are embedded in egg data — they're not in `genes.psv` directly. If you see an active skill beginning "Egg Skill:" in the wild, that's an egg-power-granted skill (e.g., Egg Skill: Ardor Shard, Egg Skill: Composure, Egg Skill: Thunderclap, Egg Skill: Dragon Feller). Grep `skills/active-skills.psv` for "Egg Skill" to see the full list.

```
grep "^Egg Skill:" skills/active-skills.psv
```

## See Also

- [eggs.md](eggs.md) — egg patterns, dens, SR tickets
- [../habitats/habitats.md](../habitats/habitats.md) — nest tables, ecosystem rank
- [../genes/builds.md](../genes/builds.md) — builds that leverage specific egg powers (Paolumu Ardor Shard, etc.)
