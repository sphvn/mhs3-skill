# Great Sword — MHS3

Damage: **Slash** (best vs tails/wings). Mechanic: **Charge Gauge** (3 levels). 32 weapons.

For mechanics detail (Charge Gauge, Charged Slash, Rage Slash, GS Mastery), see [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md).

## Best Picks by Role & Zone

| Zone | DPS | Wyvernsoul | Utility |
|---|---|---|---|
| Azuria (Shop/Az) | Flammenzahn (Fire) | Cat's Soul (Non-Elem, recipe) | Izuchi Blade (Non-Elem) |
| Canalta (Ca) | Sentoryu Raven (Non-Elem) | Epitaph Blade (Dragon, recipe) | Gossblade (Ice, Audacious Rage L) |
| Tarkuan (Ta) | Scorching Blazer (Fire) | Golm Blade (Non-Elem, CRSH stack) | Donnerzahn (Thunder, FLSH) |
| Serathis (Se) | Sinister Blade (Non-Elem) | Sword of the Winter Moon (Ice) | — |
| Post-game (PG) | Veldian Gladius (Dragon) | Azure Elder Great Sword (Dragon) | — |

## Standout Picks

- **Donnerzahn** (Thunder) — GS Mastery (L) + True Wide Slash (FLSH) for crit builds
- **Sword of the Winter Moon** (Ice) — Charge Burst (L), 4 balanced skills
- **Veldian Gladius** (Dragon) — 3 deco slots + Charge Burst (L), flexible
- **Scorching Blazer** (Fire) — Charge Burst (L) + Rage Slash (CRFT)
- **Gossblade** (Ice) — Audacious Rage (L) + Rage Clash (CRSH), aggressive playstyle
- **Epitaph Blade** (Dragon) — GS Mastery (M), CRSH-focused, huge Charged Slash damage

## Weapon List Summary

| Element | Count | Notable |
|---|---|---|
| Non-Elem | 10 | Sentoryu Raven, Cheda Blade, Sinister Blade, Epitaph Blade (Dragon subtype variant) |
| Fire | 6 | Scorching Blazer, Rosenbrett, Aknosom Blade |
| Ice | 3 | Sword of the Winter Moon, Gossblade, Frozen Speartuna |
| Thunder | 3 | Donnerzahn, Lagiacrus Blade, Khezu Shock Sword |
| Water | 2 | Tetranadon Edge, Ceanataur Blade |
| Dragon | 4 | Epitaph Blade, Berserker Sword, Veldian Gladius, Azure Elder Great Sword |

## Deep Lookup

- All GS with skills: `cat weapons/great-sword/weapons.psv`
- Per-level attack + materials: `grep "^Epitaph Blade" weapons/great-sword/params.psv`
- Find GS with specific skill: `grep -i "Audacious Rage" weapons/great-sword/weapons.psv`

## See Also

- [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md) — Charge Gauge mechanics
- [../../genes/genes.md](../../genes/genes.md) — skill affinity meanings (STR, BRK, CRSH, etc.)
- [../weapons.md](../weapons.md) — cross-type comparison
