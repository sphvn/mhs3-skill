# Hunting Horn Melodies — MHS3

27 melodies in total. Each HH has a unique set (2 or 4 melodies). Activated by note sequences on the staff; **Magnificent Trio** consumes ALL stored melodies for damage + simultaneous buffs.

Notes: Red = Power, Blue = Speed, Green = Technical. Rainbow notes (from H2H wins / Double Attacks) count as any color.

## Melody Types

**Two-note melodies** (faster to build, simpler effects):
- Wyvernfell Melody (Wyvernfell Up M)
- Elementless Melody (Non-Elem ATK Up S + Non-Elem DEF Up S)
- Various elemental single-stat buffs

**Four-note melodies** (more powerful, longer build):
- Multi-effect melodies combining ATK + DEF + special (e.g., Frigid Melody for Ice ATK & DEF)

## Key Melody Categories

| Effect Type | Example Melodies |
|---|---|
| **ATK Up** | Militant March, Bolstering Ballad |
| **DEF Up** | Defensive Ditty |
| **Element ATK/DEF** | Frigid Melody (Ice), Blazing Melody (Fire), [similar per element] |
| **Evade All (1 turn)** | Critical Chant |
| **Speed Up** | Springy Staccato |
| **HP Drain/Heal** | Mending Musician triggers, Soothing Song |
| **Wyvernfell Up** | Wyvernfell Melody |
| **Elemental Res Up** | Resistance-themed melodies |
| **Part Damage Up** | Soulbreak-themed melodies |
| **Kinship boost** | Kinship Chorale |

## Magnificent Trio

Consumes ALL stored melodies. Deals damage scaling with melodies consumed. Grants ALL melody buffs to allies simultaneously. **Best party-wide buff in the game.**

Affinity suffixes on Magnificent Trio: CRSH (Wyvernfell+), ATK (damage+), LONG (duration+).

## Deep Lookup

```
cat weapons/hunting-horn/melodies.psv
```

Each row: `melody_id|name|description|notes|partner_notes|turn|value`

- **notes**: the sequence needed to activate on YOUR staff
- **partner_notes**: what a partner's HH needs to combo-trigger
- **turn**: base duration of the buff

## See Also

- [hunting-horn.md](hunting-horn.md) — HH weapon picks and roles
- [../../combat/weapon-mechanics.md](../../combat/weapon-mechanics.md) — Note system, Rainbow Notes, Polychrome Performer
