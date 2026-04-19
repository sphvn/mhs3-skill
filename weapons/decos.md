# Weapon Decorations — MHS3

Weapon decorations are **active combat skills** slotted into weapon deco slots. They appear as selectable attacks / stances / coatings in battle. Different from armor decos (which are passive rider buffs).

**CRITICAL**: Weapon decos ≠ armor decos. They are separate pools. Don't mix.

Weapon decos use **affinity suffixes** (STR, SKL, BRK, CRSH, HVY, BLNT, FLSH, STAB, XPRT, TLNT, LONG, ARC, CURE, HEAL) instead of S/M/L/XL tiers. Same affinity system as gene skills — see [../genes/genes.md](../genes/genes.md) for the full effect table.

## Universal Decorations (any weapon)

| Deco | Cost | Effect |
|---|---|---|
| Cheer | 15 st | Grants Speed Up to all allies |
| Absolute Evasion | 50 st | Guarantees dodge of any attack for 1 turn |

## Per-Weapon-Type Decoration Pools

Each weapon type has its own deco pool. For the full active-skill catalog with affinity variants, see the type-specific cheat sheet:

- [great-sword/great-sword.md](great-sword/great-sword.md) — Charged Slash, Charge Burst, Wide Slash, Rage Slash, GS Mastery, Audacious Rage
- [long-sword/long-sword.md](long-sword/long-sword.md) — Spirit Blade, Lunge Stance, Retaliation Stance, Counter Boost, Spirit Roundslash, Spirit Release Slash, Spirithelm Breaker, Sakura Spiritblade, LS Mastery, Iai Mastery
- [hammer/hammer.md](hammer/hammer.md) — Sweet Spot, Meteor Hammer, Perfect Crush, Spinning Meteor, Windmill Bash, Chain Scrap, Perfect Strike, Backlash Blitz, Striking Secret, Hammer Mastery, Soulbreak
- [hunting-horn/hunting-horn.md](hunting-horn/hunting-horn.md) — Rousing Riff, Magnificent Trio, Defensive Ditty, Critical Chant, Power Paean, Rallying Refrain, Lyrical Legato, Militant March, Springy Staccato, Mending Musician, Polychrome Performer, HH Mastery
- [bow/bow.md](bow/bow.md) — Dragon Piercer, Aerial Aim, Rapid Shot, Quick Shot, Piercing Shot, Spread Shot, Coatings (Poison/Para/Sleep/Flash/Exhaust/Debuff), Battle Ready, Deft Hands, Bow Mastery
- [gunlance/gunlance.md](gunlance/gunlance.md) — Shelling, Burst Fire, Charged Shelling, Wyvern's Fire, Wyvern's Blaze, Hail Cutter, Guard Reload, Derring Guard, Taunt, Tactical Reload, Audacious Wyvern, GL Mastery

## Affinity Suffix Quick Reference

| Suffix | Effect |
|---|---|
| STR / ATK | +skill power, +stamina (ATK = stronger) |
| SKL / CRFT | +skill power, -Wyvernfell (CRFT = stronger) |
| BRK / CRSH | +Wyvernfell, +stamina (CRSH = stronger) |
| BLNT / HVY | +Wyvernfell, -skill power (HVY = stronger) |
| STAB / FLSH | +crit rate, +stamina (FLSH = stronger) |
| XPRT / TLNT | -stamina, -skill power (TLNT = stronger) |
| LONG / ARC | +buff duration, +stamina |
| CURE / HEAL | +HP recovery, +stamina |

See [../genes/genes.md](../genes/genes.md) for the full effects table.

## How to Obtain

| Source | Details |
|---|---|
| **Fully upgrading gear** | Max-level weapon unlocks a decoration. **Primary source for weapon decos** |
| **Melynx Emporium** | Buy with Trade Points. Inventory expands with story progression |
| **Treasure chests** | Throughout the world |
| **Quest rewards** | Specific quests grant specific decorations |

**Not crafted.** Smithy crafts/upgrades weapons — decos come from fully upgrading.

## Deep Lookup

- `cat weapons/decos.psv` — all 18 universal/mixed weapon decorations
- Per-type deco pools: grep relevant `weapons/{type}/weapons.psv` (decos are the skills column)

## See Also

- [../armor/decos.md](../armor/decos.md) — armor decorations (separate pool!)
- [../genes/genes.md](../genes/genes.md) — affinity suffix effects
- [../combat/weapon-mechanics.md](../combat/weapon-mechanics.md) — how each weapon's skills interact
