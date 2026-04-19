# Passive Skills — MHS3

Passive skills are **always-on** effects (no stamina cost). Sources:
- **Armor sets** — built-in skills on the Rider's armor
- **Armor decorations** — slotted into armor deco slots (passive only)
- **Monstie genes** — some gene cells are passive (vs active)

357 passive skill rows (including S/M/L/XL tiers). For the full tier table: `cat skills/passive-skills.psv`.

Schema: `name|skill_family|level|description`.

- `name`: the full name with tier (e.g., "Critical (XL)")
- `skill_family`: the base skill family (e.g., "Critical")
- `level`: 1–4 (1=S, 2=M, 3=L, 4=XL)

## Tier Upgrade Rules

- S < M < L < XL
- **Same-name passives do NOT stack** — only highest tier applies
- Duplicate armor decorations auto-upgrade to the next tier
- No equal-tier stacking either — Critical (L) + Critical (L) still = Critical (L)

## Top Passives by Role

### Offense

| Family | XL Effect |
|---|---|
| Critical | +15% crit rate |
| Critical Kinship | +15 Kinship per crit |
| [Elem] Atk Boost | +20% elemental damage **multiplicative** |
| All-Out | +30% skill damage (×1.2 stamina) |
| Salt in Wound | +20% damage vs status-afflicted |
| Dragon Buster | +25 flat Wyvernfell |
| Weak Point | +damage to broken parts |
| Elemental Assault | +50% against elemental weaknesses (XL Dragon Buster synergy) |
| Dancer | +20% dmg / -20% taken at full HP |

### Defense

| Family | XL Effect |
|---|---|
| Health Boost | +20% max HP |
| All-Elem Def Boost | -10% all elem damage |
| [Elem] Def Boost | -30% specific element damage |
| Tenacity | Survive 1 fatal hit (>50% HP req) |
| Anti 1-Hit KO | Prevents one-hit kills |
| Darkness Resistance | -darkness effect severity |
| Fortify | +stats after fainting |
| Divine Blessing | Medium chance to halve damage |

### Sustain

| Family | XL Effect |
|---|---|
| Self-Heal | 20% max HP per turn |
| Crit-Heal | 30% max HP on crit |
| Panacea | Negate abnormal statuses |
| Stamina Surge | +6 stamina recovery/turn |
| Stamina Boost | +20 starting stamina |

### Kinship

| Family | XL Effect |
|---|---|
| Soul Kinship | ×1.4 Kinship fill rate |
| Kinship Skill+ | Powers up Kinship Skills |
| Synchronize | Rider-Monstie sync boost (ambiguous but powerful — Aelucanth/Arkvulcan armor) |
| HtH Master | +12 Kinship per H2H win |
| Partner | ×2 Kinship gen at <50% HP |

### Under 50% HP (risk/reward)

| Family | XL Effect |
|---|---|
| Heroics | +25% damage |
| Vigilance | +40% crit rate |
| Potential | +ATK + DEF |

### Status Resistances

Antivenom, Antiparalysis, Antiburn, Antibleed, Insomniac (sleep), Sealbreaker (Velkhana's Skill Seal), Nullify Burn / Paralysis / Blind (full negation at S+).

### Utility

| Family | XL Effect |
|---|---|
| Inflict Rate Up | +status infliction chance |
| Partbreaker | +part break damage |
| Slugger | +stun damage |
| Quick | +action speed |
| Evasion Ability | +evasion chance |
| Evasion Instinct | Triggers evasion more often |
| Item Saver | Chance to not consume items |
| Den Protector | Bonus rewards from dens |
| **Heroic Testament** | +HP + DMG - DMG taken (only from slaying Calamitous Elder Dragons) |

## Same-Name Stack Rule Examples

**Critical (L) + Critical (XL)** → Only XL applies. Second gene is a **dead slot** — replace with a Bingo-contributing gene.

**Health Boost (XL) + Health Boost (XL)** → Only one XL applies. Double dip is always wasted.

**Different passives stack normally**: Critical (XL) + Critical Kinship (XL) = both apply.

## How Tier Values Scale

Most passives follow **5/10/15/20% linear scaling** (S/M/L/XL). Some (Critical, Self-Heal, etc.) scale non-linearly. Specific values: `grep "Health Boost" skills/passive-skills.psv`.

## Deep Lookup

- `cat skills/passive-skills.psv` — full 357-row catalog
- `grep "^Critical (" skills/passive-skills.psv` — all Critical tiers
- `grep "skill_family=HP_UP" skills/passive-skills.psv` — (approximate) Health Boost family
- Find passives with specific keywords: `grep -i "kinship" skills/passive-skills.psv`

## See Also

- [active-skills.md](active-skills.md) — battle abilities
- [../genes/genes.md](../genes/genes.md) — passive gene placements on the 3×3 grid
- [../armor/decos.md](../armor/decos.md) — armor decoration source for passives
