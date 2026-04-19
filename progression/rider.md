# Rider Progression — MHS3

The Rider (your hunter character) levels up separately from monsties. Each level grants stat increases across 8 stats.

100 levels total. Full data: `cat progression/rider.psv`.

Schema: `level|hp|attack|defense|initial_stamina|stamina_regen|stamina_attack|stamina_defense|regeneration|speed|affinity|skill_rate|next_xp`.

## Level Progression Highlights

### Level 1 (start)
- HP: 38, ATK: 8, DEF: 7, Start Stam: 50, Regen: 8

### Level 10 (~end of Azuria)
- Dramatically higher HP + ATK; still using basic armor

### Level 50 (mid-Tarkuan / start-Serathis)
- HP has grown 3–4×, ATK proportionally; Crit builds become viable

### Level 100 (max)
- All stats capped; gene/armor/weapon optimization does more than leveling

## Stat Scaling Notes

- **HP growth** is gradual early, then accelerates in mid-game (~Lv 40-60).
- **ATK** scales linearly with level.
- **DEF** scales slower than ATK — armor makes up the difference.
- **Speed** is mostly flat from leveling; most speed comes from gene/armor skills.
- **Affinity** (crit) starts at 0 — comes almost entirely from Critical passive genes/decos.

## Where XP Comes From

- Winning battles
- Completing quests (main story + side stories)
- **Barrel Felynes** at night (trap-style XP burst)
- Post-game expedition boss defeats

**Night XP boost**: Night fights give ~10% more XP than day. Pair with Barrel Felyne farming for fast leveling.

## Grinding Strategy

1. **Azuria (Lv 1–15)**: story XP is enough; don't grind.
2. **Canalta (Lv 15–30)**: clear Barrel Felynes at night once every few quests.
3. **Tarkuan (Lv 30–50)**: Invasive Shogun Ceanataur farm (see [../genes/builds.md](../genes/builds.md) for optimal rotation) — best XP/time in mid-game.
4. **Serathis / Post-game (Lv 50+)**: Elder Dragon SR runs give massive XP + guaranteed gene drops.

## Reading the PSV

```
grep "^{level}|" progression/rider.psv
```

Example at Lv 50:
```
grep "^50|" progression/rider.psv
```

## Rider vs Monstie Leveling

- Rider and monstie level **independently**.
- Monsties level from battle XP (splits with party).
- Rider XP is full share (not split).
- **Keep them roughly equal** — over-leveled monsties compensate for under-leveled rider only up to a point.

## Skill Rate

The `skill_rate` column reflects... (not fully documented in launch data — likely AI-partner skill frequency, or crit-damage multiplier). Worth checking in-game at high levels.

## Deep Lookup

- `awk -F'|' 'NR>2 {print $1"\t"$2"\t"$3"\t"$4}' progression/rider.psv | head -10` — first 10 levels
- `grep "^100|" progression/rider.psv` — max-level stats

## See Also

- [stages.md](stages.md) — where you fight each zone's monsters
- [../genes/builds.md](../genes/builds.md) — how rider stats interact with archetype builds
- [../items/meals.md](../items/meals.md) — meals add flat stat bonuses on top of level stats
