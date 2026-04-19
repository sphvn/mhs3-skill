# Armor Decorations — MHS3

Armor decorations are **passive rider skills** slotted into armor deco slots. They are always-on buffs. Different from weapon decos (which are active combat skills).

**Tier upgrades**: Armor decos come in **S < M < L < XL**. Obtaining a duplicate auto-upgrades to the next tier. Same-name skills from different sources do NOT stack — only the highest tier applies.

## How to Obtain

| Source | Details |
|---|---|
| **Melynx Emporium** | Buy with Bronze/Silver/Gold Trade Points. Inventory expands with story |
| **Fully upgrading gear** | Max-level armor unlocks a decoration. **Primary source** |
| **Treasure chests** | In dens, overworld |
| **Quest rewards** | Specific quests |
| **Elder Dragon slays** | **Heroic Testament** only from SLAYING (not repelling) Calamitous Elder Dragons. Upgrades with each slay |

## Skill Categories

### Offense

| Skill | Effect |
|---|---|
| Critical | +Crit Rate |
| Critical Kinship | +Kinship on crits (+15 at XL) |
| All-Out | +active skill damage (×1.2 stamina) |
| Vicious | +damage dealt |
| [Element] Atk Boost | +damage for that element (XL = +20% multiplicative) |
| Non-Elem Atk Boost | +non-elemental damage |
| Salt in Wound | +damage vs status-afflicted targets (+20% XL) |
| Weak Point | +damage to broken parts |
| Elemental Assault | +elemental damage |
| Elemental Breaker | +elemental part breaking |
| Dragon Buster | +25 Wyvernfell (flat) at XL |

### Defense

| Skill | Effect |
|---|---|
| Health Boost | +max HP (+20% XL) |
| Divine Blessing | chance to halve damage taken |
| All-Elem Def Boost | -all elemental damage (-10% XL) |
| [Element] Def Boost | -specific elemental damage (-30% XL) |
| Tenacity | survive 1 fatal hit (>50% HP req) |
| Fortify | +stats after fainting |
| Anti 1-Hit KO | prevents one-hit kills |
| Darkness Resistance | -darkness effect |

### Sustain

| Skill | Effect |
|---|---|
| Self-Heal | HP regen per turn (20% max HP XL) |
| Crit-Heal | HP on crit (+30% max HP XL) |
| Panacea | negate abnormal statuses |
| Stamina Surge | +stamina recovery (+6/turn XL) |
| Stamina Boost | +starting stamina (+20 XL) |

### Kinship

| Skill | Effect |
|---|---|
| Soul Kinship | ×1.4 Kinship fill rate (XL) |
| Kinship Skill+ | +Kinship Skill damage |
| Synchronize | Rider-Monstie sync boost |
| HtH Master | +12 Kinship per H2H win (XL) |
| Partner | ×2 Kinship gen at low HP (XL) |

### Status / Utility

| Skill | Effect |
|---|---|
| Inflict Rate Up | +status infliction chance |
| Item Saver | chance to not consume items |
| Quick | +action speed |
| Evasion Ability | +evasion chance |
| Evasion Instinct | triggers evasion more often |
| Dancer | +20% dmg / -20% taken at full HP (XL) |
| Partbreaker | +part break damage |
| Slugger | +stun damage |
| Den Protector | bonus rewards from dens |
| **Heroic Testament** | +max HP, +dmg, -dmg taken. Only from slaying Calamitous Elder Dragons (S→M→L→XL per slay) |

### Status Resistance

Antivenom (poison), Antiparalysis, Antiburn, Antibleed, Insomniac (sleep), Sealbreaker (skill seal), Darkness Resistance, Blightproof (all blights).

### Under 50% HP (risk/reward)

| Skill | Effect |
|---|---|
| Heroics | +25% damage (XL) |
| Vigilance | +40% crit rate (XL) |
| Potential | +ATK + DEF |
| Partner | +100% Kinship gen (XL) |

## Deep Lookup

- `cat armor/decos.psv` — all 59 armor decorations with skill IDs
- `grep -i "critical (xl)" armor/decos.psv` — find a specific XL deco
- `cat skills/passive-skills.psv | grep -i "{skill}"` — full tier data for any passive

## See Also

- [armor.md](armor.md) — armor sets with built-in skills
- [../skills/passive-skills.md](../skills/passive-skills.md) — full passive skill catalog
- [../weapons/decos.md](../weapons/decos.md) — weapon decorations (separate pool!)
