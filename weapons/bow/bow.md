# Bow — MHS3

Damage: **Pierce** (best vs bodies/soft spots). Mechanic: **Coatings** (one active at a time, switching resets Charge Gauge, applying costs 0 stamina). **Charge Gauge 1–5**. 37 weapons.

For mechanics detail, see [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md).

## Best Picks by Role & Zone

| Zone | Flexibility | Crit / DPS | Wyvernsoul |
|---|---|---|---|
| Azuria | Felyne Bow (Non-Elem, 7 skills incl. Flash+Para, 0 deco) | Spongia Bow (Water, Wyvernfell king) | Spongia Bow (Water, Exhaust) |
| Canalta | Arzuros Bow (Non-Elem, Spread Shot BRK) | Blue Blade Bow (Water, Dragon Piercer CRFT) | Dawn Ray Bow (Non-Elem) |
| Tarkuan | Mud Shot (Water) | Type 64 Multibow (Water, Aerial Aim HVY) | — |
| Serathis | Weaver of Flame (Fire, Dragon Piercer FLSH) | Iceflinger (Ice, Deft Hands L) | — |
| Post-game | Veldian Arcum (Dragon, Deft Hands L, 3 deco) | Iceflinger (Ice) | — |

## Standout Picks

- **Veldian Arcum** (Dragon) — Deft Hands (L), 3 deco slots, best all-around bow
- **Iceflinger** (Ice) — Deft Hands (L) + Aerial Aim (ATK), strong ice damage
- **Felyne Bow** (Non-Elem) — 7 skills including Flash + Paralysis Coating, status king (0 deco)
- **Weaver of Flame** (Fire) — Battle Ready (M), Dragon Piercer (FLSH) for crit
- **Blue Blade Bow** (Water) — Dragon Piercer (CRFT) + Deft Hands (M)
- **Spongia Bow** (Water) — Bow Mastery (S) + highest Wyvernfell + Exhaust Coating — top Wyvernsoul Topple bow

## Coating Strategy

Only one coating active at a time. Switching **resets Charge Gauge**. Applying costs 0 stamina and deals weapon-element damage.

| Coating | Use Case |
|---|---|
| Power | +bow damage (DPS) |
| Poison / Paralysis / Sleep / Flash | Status control |
| Exhaust | **Boosts Wyvernsoul damage** (top Wyvernsoul pick) |
| Attack Down / Accuracy / Defense Down | Debuff the enemy |

**Battle Ready** (passive): auto-activates a random coating at battle start; higher tiers also start with charge levels. **Deft Hands** (passive): +1 guaranteed charge on coating switch, chance for more at higher tiers — core for coating-swap builds.

## Deep Lookup

- `cat weapons/bow/weapons.psv` — all 37 bows
- `grep -i "deft hands" weapons/bow/weapons.psv` — bows with Deft Hands
- `grep "^Veldian Arcum" weapons/bow/params.psv` — per-level data

## See Also

- [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md) — Coatings, Charge Gauge, Battle Ready
- [../weapons.md](../weapons.md) — cross-type
