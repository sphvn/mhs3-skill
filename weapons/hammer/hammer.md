# Hammer — MHS3

Damage: **Blunt** (best vs heads/shells). **Unique trait: basic attacks damage the Wyvernsoul Gauge** (only weapon type that does). Stuns on head hits. 37 weapons.

For mechanics detail, see [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md).

## Best Picks by Role & Zone

| Zone | Raw DPS | Wyvernsoul | Support |
|---|---|---|---|
| Azuria | Kut-Ku Pick (Fire, Hammer Mastery S) | Cluster Hammer (Non-Elem) | Ludroth Splashhammer (Water) |
| Canalta | Almudron Hammer (Water) | Yeti Hammer (Ice, HVY Perfect Strike) | Plesioth Head (Water) |
| Tarkuan | Diablos Hammer (Non-Elem) | Shell Hammer (Fire, HVY Perfect Strike) | Scorching Isshata (Fire) |
| Serathis | Sinister Hammer (Non-Elem) | Hammer of the Winter Moon (Ice) | — |
| Post-game | Azure Elder Hammer (Dragon) | Duke Smiter (Dragon) | Veldian Malleus (Dragon) |

## Standout Picks

- **Azure Elder Hammer** (Dragon) — Hammer Mastery (L), 5 skills with CRFT focus
- **Diablos Hammer** (Non-Elem) — Striking Secret (L) + Perfect Strike (ATK), raw power
- **Yeti Hammer** (Ice) — Perfect Strike (HVY) + Striking Secret (L), Wyvernsoul king
- **Usurper's Thunder** (Thunder) — Hammer Mastery (L), Thunder skill-focused
- **Hammer of the Winter Moon** (Ice) — Soulbreak (L) + Backlash Blitz (CRFT)
- **Scorching Isshata** (Fire) — Hammer Mastery (L), clean fire pick
- **Devil's Due** (Dragon) — Striking Secret (L), 5 skills

## Wyvernsoul Topple Pick: HVY Skills

HVY affinity massively boosts Wyvernfell (gauge damage). Top HVY hammers:
- **Yeti Hammer** (Ice) — Perfect Strike (HVY) + Striking Secret (L)
- **Shell Hammer** (Fire) — Perfect Strike (HVY) + Soulbreak (L), 6 skills
- **Tetranadon Edge** (Water) — True Wide Slash (HVY)

Pair with Dragon Buster passive (+25 Wyvernfell flat) for maximum gauge damage.

## Deep Lookup

- `cat weapons/hammer/weapons.psv` — all 37 hammers
- `grep "^Azure Elder Hammer" weapons/hammer/params.psv` — level data
- `grep -i "perfect strike" weapons/hammer/weapons.psv` — hammers with Perfect Strike

## See Also

- [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md) — Stun, Striking Secret, Soulbreak
- [../../combat/combat.md](../../combat/combat.md) — Wyvernfell formula
- [../weapons.md](../weapons.md) — cross-type
