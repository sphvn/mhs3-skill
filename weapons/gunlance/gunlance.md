# Gunlance — MHS3

Damage: **Pierce** (best vs bodies/soft spots). Mechanic: **Shell system (8 shells)** + Guard + Taunt. Shell damage ignores monster defense. 33 weapons.

For mechanics detail, see [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md).

## Best Picks by Role & Zone

| Zone | Tank | DPS/Shell | Aggro |
|---|---|---|---|
| Azuria | Princess Panoply (Fire, Guard Chance S) | Lagia Burst (Thunder, Hail Cutter + Burst Fire CRFT) | Iron Gunlance (Non-Elem, Taunt) |
| Canalta | Almudron Gunlance (Water, Wyvern's Fire ATK) | Aknosom Gunlance (Fire, GL Mastery M) | Hellsting (Ice, HVY-heavy) |
| Tarkuan | — | Ajara Gunpike (Fire, Burst Fire FLSH) | — |
| Serathis | — | — | — |
| Post-game | Fiore Nulo Black (Dragon, 3 deco) | — | — |

## Standout Picks

- **Lagia Burst** (Thunder) — GL Mastery (M), Hail Cutter (SKL) + Burst Fire (CRFT), best offensive GL
- **Aknosom Gunlance** (Fire) — GL Mastery (M), clean skill-focused fire option
- **Hellsting** (Ice) — 5 skills, HVY-heavy for Wyvernfell builds
- **Kadachi Striker** (Thunder) — 6 skills incl. Single Combat, versatile
- **Fiore Nulo Black** (Dragon) — 3 deco slots, flexible Dragon pick

## Shell + Guard Playstyle

Core loop:
1. **Guard Reload** → +2 shells + Guard buff (reduces damage)
2. **Shelling** or **Charged Shelling** → consumes shells for fixed-damage attacks
3. **Burst Fire** → all 8 shells for massive damage + Guard (L), **3× stamina**
4. **Wyvern's Fire / Wyvern's Blaze** → big explosion, high stamina, cooldown

**Taunt** forces enemies to target you — use when a squishy ally is about to take a hit.

**Derring Guard** — brace 1 turn, boosts ATK/DEF proportional to damage taken. Counter-style pick.

## Deep Lookup

- `cat weapons/gunlance/weapons.psv` — all 33 gunlances
- `grep "^Lagia Burst" weapons/gunlance/params.psv` — level data
- `grep -i "burst fire" weapons/gunlance/weapons.psv` — GLs with Burst Fire

## See Also

- [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md) — Shell system, Wyvern's Fire, Guard
- [../weapons.md](../weapons.md) — cross-type
