# MHS3 Skills & Decorations Reference

## Skill Sources

Skills come from three places in MHS3:

1. **Weapons** — Each weapon has built-in skills (weapon-specific attacks + passive effects)
2. **Armor** — Each armor set provides passive skills for the Rider
3. **Genes** — Monstie gene grid skills (see `genes-and-builds.md` for full gene skill list)
4. **Decorations** — Slotted into deco slots on weapons and armor (see below)

Weapon/armor skills affect the **Rider**. Gene skills affect the **monstie**. They are separate systems.

## Decoration System

**CRITICAL DISTINCTION: Weapon decorations and armor decorations are completely separate pools.**

| Slot Type | What Goes In | Effect |
|---|---|---|
| **Weapon deco slots** | Active combat skills | Appear as selectable actions in battle (attacks, stances, coatings) |
| **Armor deco slots** | Passive rider skills | Always-on buffs (crit rate, HP, elemental defense, etc.) |

**Do NOT recommend passive skills (Critical, Health Boost, etc.) for weapon deco slots. Do NOT recommend active skills (Charged Slash, Lunge Stance, etc.) for armor deco slots.**

- Weapons and armor have **0–3 decoration slots** each
- Slots may increase when you upgrade gear at the Smithy
- Decorations can be freely swapped between equipment of the same type
- Weapon decorations carry **affinity variants** (STR, SKL, BLNT, etc.) — same system as built-in weapon skills
- No slot size system — any decoration fits any slot of its type

### How to Obtain Decorations

| Source | Details |
|---|---|
| **Melynx Emporium** | Buy from Merchant Melynx at camps/towns using Bronze/Silver/Gold Trade Points. Inventory expands with story progression |
| **Fully upgrading gear** | Upgrading a weapon or armor piece to max level unlocks a decoration. This is the primary source for most weapon decos |
| **Treasure chests** | Found throughout the world in dens and overworld |
| **Quest rewards** | Specific quests grant specific decorations |
| **Elder Dragon slays** | Heroic Testament (armor deco) obtained by slaying — not repelling — Calamitous Elder Dragons. Upgrades S→M→L→XL with each slay |

**Decorations are NOT crafted.** The Smithy crafts and upgrades weapons/armor — decorations come as a byproduct of fully upgrading gear, or from the other sources above.

### Decoration Tier Upgrades (Armor Decos)

Armor decorations come in tiers: **(S) < (M) < (L) < (XL)**. Obtaining multiple copies of the same decoration automatically upgrades it to the next tier:
- S → M → L → XL
- Same-name skills from different sources do NOT stack — only the highest tier applies

Weapon decorations use **affinity variants** instead of tiers (STR, SKL, BRK, CRSH, etc.). See `genes-and-builds.md` for the full affinity effects table.

---

## Weapon Decorations by Type

These are **active combat skills** slotted into weapon deco slots. Each weapon type has its own pool.

### Universal (Any Weapon)
| Deco | Cost | Effect |
|---|---|---|
| Cheer | 15 st | Grants Speed Up to all allies |
| Absolute Evasion | 50 st | Guarantees dodge of any attack for 1 turn |

### Great Sword
| Deco | Key Variants | Effect |
|---|---|---|
| Charged Slash | STR, BRK, SKL | Consumes Charge Gauge — elemental damage, single target |
| Charge Burst | S, M, L | High-damage Charge Gauge finisher |
| Wide Slash / True Wide Slash | BLNT, HVY, CRFT, FLSH | AoE Charge Gauge consumer |
| Rage Slash | CRFT, CRSH | 3-charge heavy single hit (unlocks ~Tarkuan) |
| Strong Charged Slash | CRFT, CRSH | High-power charged attack |
| GS Mastery | S, M, L | Passive: chance for +1 extra Charge Gauge level |
| Audacious Rage | S, M, L | Conditional damage boost |

### Long Sword
| Deco | Key Variants | Effect |
|---|---|---|
| Spirit Blade | STR, STAB, BLNT | Spirit Gauge attack |
| Lunge Stance | SKL, STAB, BLNT | Elemental damage + assumes Lunge stance (follow-up after ally attacks). Req: Spirit Gauge 1+ |
| Retaliation Stance | SKL, STAB, BLNT | Counter stance — counters enemy attacks |
| Counter Boost | S, M, L | Enhances counter damage |
| Spirit Roundslash | SKL, BRK, BLNT | Spirit Gauge finisher |
| Spirit Release Slash | TLNT, ATK, CRSH | Spirit Gauge consumer |
| Spirithelm Breaker | FLSH, ATK, CRSH | Heavy Spirit Gauge attack |
| Sakura Spiritblade | FLSH, ATK, CRSH | Multi-hit Spirit finisher |
| LS Mastery | S, M, L | Passive: Spirit Gauge generation bonus |
| Iai Mastery | S, M, L | Passive: sheathe counter bonus |

### Hammer
| Deco | Key Variants | Effect |
|---|---|---|
| Sweet Spot | BLNT, STR, SKL | Elemental AoE + Wyvernsoul damage + Stun chance |
| Meteor Hammer | STR, SKL, STAB | Single target + heavy part damage |
| Perfect Crush | BLNT, STR, SKL | AoE + heavy Wyvernsoul + Stun chance |
| Spinning Meteor | ATK, FLSH, CRFT | High-damage blunt finisher |
| Windmill Bash | STAB, BRK, SKL | AoE blunt attack |
| Chain Scrap | STAB, BRK, SKL | Multi-hit / follow-up attack |
| Perfect Strike | ATK, HVY, CRFT | Precision single-target |
| Backlash Blitz | CRFT, BRK, FLSH | Counter-style hammer attack |
| Striking Secret | S, M, L | Special Hammer technique |
| Hammer Mastery | S, M, L | Passive: chance for +2 extra shells when loading |
| Soulbreak | S, M, L | Conditional damage boost |

### Hunting Horn
| Deco | Key Variants | Effect |
|---|---|---|
| Rousing Riff | SKL, BRK, LONG | Damage + Attack Up & Accuracy Up to all allies |
| Magnificent Trio | ATK, CRSH | Consumes melodies — damage scales with melodies consumed, allies get all melody buffs |
| Defensive Ditty | SKL, BRK, LONG | Defensive melody |
| Critical Chant | STAB, SKL | Crit-focused melody attack |
| Power Paean | STR, BRK | Team attack buff melody |
| Rallying Refrain | STAB, SKL, LONG | Buff melody |
| Lyrical Legato | STR, BRK | Melody-based buff |
| Militant March | STR, LONG, SKL | Team movement/priority buff |
| Springy Staccato | STR, BRK | Quick melody attack |
| Mending Musician | S, M, L | Passive: HP recovery melody |
| Polychrome Performer | S, M, L | Passive: enhanced melody effects |
| HH Mastery | S, M, L | Passive: melody generation bonus |

### Bow
| Deco | Key Variants | Effect |
|---|---|---|
| Dragon Piercer | CRFT, CRSH, FLSH | Piercing shot through enemies |
| Aerial Aim | ATK, HVY | Elevated shot with Power Coating |
| Rapid Shot | BRK, STAB | Charge Gauge +2 levels + elemental damage |
| Quick Shot | HVY, CRSH | Fast single-target attack |
| Piercing Shot | STAB, SKL | Pierce-type damage |
| Spread Shot | STR, BRK, STAB | AoE shot |
| Poison Coating | — | Elemental + Poison chance. Scales with Charge Gauge. 0 stamina cost |
| Paralysis Coating | — | Elemental + Paralysis chance |
| Sleep Coating | — | Elemental + Sleep chance |
| Flash Coating | — | Elemental + Flash chance |
| Exhaust Coating | — | Elemental + Exhaust chance |
| Attack/Accuracy/Defense Down Coating | — | Debuff coatings |
| Battle Ready | S, M | Passive: applies random coating at battle start |
| Deft Hands | S, M, L | Passive: coating power scales with Charge Gauge |
| Bow Mastery | S, M, L | Passive: Bow mechanic bonus |

### Gunlance
| Deco | Key Variants | Effect |
|---|---|---|
| Shelling | BLNT, SKL, STAB | Consumes 2 shells — elemental damage + Guard |
| Burst Fire | HVY, CRFT, FLSH | Multi-shell rapid fire |
| Charged Shelling | SKL, BLNT | High-damage shelling, more ammo cost |
| Wyvern's Fire | HVY, ATK, TLNT | Heavy shell attack |
| Wyvern's Blaze | HVY, TLNT | Wyvern fire special |
| Hail Cutter | SKL, STAB | Overhead shell attack |
| Guard Reload | — | Loads 2 shells + grants Guard |
| Derring Guard | — | Brace 1 turn — boosts ATK/DEF relative to damage taken |
| Taunt | — | Forces enemies to target you (aggro) |
| Tactical Reload | — | Tactical shell management |
| Audacious Wyvern | S, M | Conditional Wyvern attack boost |
| GL Mastery | S, M | Passive: chance for +2 extra shells when loading |

---

## Common Armor Decorations (Passive Rider Skills)

These are slotted into **armor deco slots only**. Same skills that appear built-in on armor pieces.

### Offense
| Skill | Effect |
|---|---|
| Critical | Increases Crit Rate |
| Critical Kinship | Bonus Kinship on critical hits |
| All-Out | Increases active skill damage (costs more stamina) |
| Vicious | Increases damage dealt |
| [Element] Atk Boost | Increases damage for that element |
| Non-Elem Atk Boost | Increases non-elemental damage |
| Salt in Wound | Bonus damage vs status-afflicted targets |
| Weak Point | Bonus damage to broken parts |
| Elemental Assault | Boosts elemental damage |
| Elemental Breaker | Bonus to elemental part breaking |

### Defense
| Skill | Effect |
|---|---|
| Health Boost | Increases max HP |
| Divine Blessing | Chance to reduce damage taken |
| All-Elem Def Boost | Reduces all elemental damage taken |
| [Element] Def Boost | Reduces damage from specific element |
| Tenacity | Survive one fatal hit (above 50% HP) |
| Fortify | Boosts stats after fainting |
| Anti 1-Hit KO | Prevents one-hit kills |

### Sustain
| Skill | Effect |
|---|---|
| Self-Heal | Recover HP each turn |
| Crit-Heal | Heal on critical hits |
| Panacea | Can negate abnormal statuses |
| Stamina Surge | Increases stamina recovery |
| Stamina Boost | Increases starting stamina |

### Kinship
| Skill | Effect |
|---|---|
| Soul Kinship | Increases Kinship Gauge fill rate |
| Kinship Skill+ | Powers up Kinship Skills |
| Synchronize | Boosts Rider-Monstie sync effects |
| HtH Master | Bonus Kinship from winning Head-to-Head |
| Partner | Boosts Kinship Gauge generation |

### Status / Utility
| Skill | Effect |
|---|---|
| Inflict Rate Up | Increases status infliction rate |
| Item Saver | Chance to not consume items |
| Quick | Increases action speed |
| Evasion Ability | Increases evasion chance |
| Evasion Instinct | Triggers evasion more frequently |
| Dancer | Attack + Defense boost at full HP |
| Partbreaker | Increases part break damage |
| Slugger | Increases stun damage |
| Den Protector | Bonus rewards from dens |
| Heroic Testament | Increases max HP, damage dealt, reduces damage taken. From slaying Calamitous Elder Dragons (S→M→L→XL) |

### Status Resistance
Antivenom, Antiparalysis, Antiburn, Antibleed, Insomniac (sleep), Sealbreaker (seal), Darkness Resistance, Blightproof (all blights)

### Under 50% HP (risk/reward)
| Skill | Effect |
|---|---|
| Heroics | Damage dealt increased |
| Vigilance | Crit Rate increased |
| Potential | Attack and Defense increased |
| Partner | Kinship Gauge generation increased |

## Affinity Suffixes on Weapon Skills

Weapon skills show affinity suffixes like (STR), (ATK), (FLSH), etc. These are trade-off modifiers.
For the full affinity effects table, see `genes-and-builds.md` — the system is identical for weapon and gene skills.
