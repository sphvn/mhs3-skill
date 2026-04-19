# Weapon Mechanics — MHS3

For general combat (PST, H2H, Kinship, Wyvernfell, status), see [combat.md](combat.md).

## Damage Categories

| Category | Weapons | Best vs Body Parts |
|---|---|---|
| Slash | Great Sword, Long Sword | Tails, wings |
| Blunt | Hammer, Hunting Horn | Heads, shells |
| Pierce | Bow, Gunlance | Bodies, soft spots |

Part-specific damage multipliers per monster live in `monsters/parts.psv` — grep by monster name.

## Great Sword (Slash)

- **Strengths**: High damage per hit, good part breaking, beginner-friendly
- **Pairs with**: Power monsties for consistent H2H coverage
- **Phase**: Strong all game, especially early

**Charge Gauge (3 levels)**: Fills via skills (Quick Charge) and winning H2Hs. Higher charge = more powerful consumer skills.

- **Charged Slash**: Consumes charge, heavy single-target damage
- **Charge Burst**: High-damage charge finisher
- **Wide Slash / True Wide Slash**: Consumes charge, AoE damage
- **Rage Slash**: 3-charge heavy single-target hit (unlocks ~Tarkuan)
- **GS Mastery** (passive): Slight chance to gain +1 extra charge level when filling
- **Audacious Rage** (passive): +Rage Slash damage, +damage taken

## Long Sword (Slash)

- **Strengths**: Flow-based combat, sheathe counters, sustained DPS
- **Pairs with**: Technical or Speed monsties for variety
- **Phase**: Rewarding mid-to-late game once mastered

**Spirit Gauge (multi-segment)**: Fills via Spirit Blade skills and winning H2Hs. Stances require ≥1 segment and consume 1/turn.

- **Spirit Blade**: Builds Spirit Gauge + deals damage
- **Lunge Stance**: Costs 1 gauge/turn. Deals damage, launches follow-up attacks after allies attack. Ends with Special Sheathe.
- **Retaliation Stance**: Costs 1 gauge/turn. Deals damage, launches counterattacks after enemies attack. Ends with Special Sheathe.
- **Special Sheathe**: After stance ends — regular attacks deal more + unique Unsheathing attack. Length determined by Spirit Gauge level at activation.
- **Spirit Release Slash**: Consumes ALL Spirit Gauge, grants Critical Eye, counters one enemy attack. Removes Special Sheathe on counter or turn end.
- **LS Mastery** (passive): Slight chance for +1 Spirit Gauge level when filling
- **Iai Mastery** (passive): Slight chance to negate Spirit Gauge reduction during Special Sheathe
- **Counter Boost** (passive): Reduces damage taken during Special Sheathe + slight damage boost

## Hammer (Blunt)

- **Strengths**: Highest raw damage, excellent Wyvernsoul damage, simple
- **Pairs with**: Power monsties for maximum impact
- **Phase**: Strong all game

**No unique gauge** — simplest weapon mechanically. **Unique trait: only weapon where basic attacks damage the Wyvernsoul Gauge** (all others need Active Skills).

- **Perfect Strike**: AoE + heavy Wyvernsoul + Stun chance
- **Sweet Spot**: AoE + Wyvernsoul + Stun chance
- **Perfect Crush**: AoE + heavy Wyvernsoul + Stun chance
- **Spinning Meteor**: High-damage blunt finisher
- **Meteor Hammer**: Single target + heavy part damage
- **Hammer Mastery** (passive): Reduces Stamina cost on H2H win
- **Striking Secret** (passive): Normal attacks deal more to Wyvernsoul Gauge
- **Soulbreak** (passive): Greatly increases damage to broken monster parts

## Hunting Horn (Blunt)

- **Strengths**: Party support (ATK/DEF up, healing, status cleanse), blunt damage
- **Pairs with**: Support/survivability builds, long fights
- **Phase**: Shines in endgame team scenarios

**Note system**: Attacks generate colored notes — Red (Power), Blue (Speed), Green (Technical). H2H wins and Double Attacks generate **Rainbow Notes** (wildcards for any color). Notes display on a melody staff; new notes push older ones off.

**Melody system**: Each HH has unique melodies activated by specific note sequences.
- **Two-note melodies**: Faster to build (e.g., Frigid Melody: Ice ATK & DEF Up)
- **Four-note melodies**: More powerful, require 4 specific notes in order
- Effect types: ATK Up, DEF Up, Evade All (1 turn), Speed Up, HP Drain, Wyvernfell Up, Elem Res Up, Part Damage Up
- **Magnificent Trio**: Consumes ALL stored melodies — damage scales with melodies consumed, grants all melody buffs to allies simultaneously
- **Polychrome Performer** (passive): Chance to turn notes into Rainbow Notes when adding
- **HH Mastery** (passive): Slight Speed boost after performing a melody
- **Mending Musician** (passive): Recovers HP when performing a melody

For the full 27-melody catalog: grep `weapons/hunting-horn/melodies.psv`.

## Bow (Pierce)

- **Strengths**: Ranged safety, status control, flexible
- **Pairs with**: Status-focused monsties (Purple Gypceros, Dreadqueen Rathian)
- **Phase**: Great mid-to-late for control

**Charge Gauge (Level 1–5)**: Fills via Rapid Shot (+2), Quick Shot (+1), H2H wins. Higher charge = stronger coatings.

**Coating system — ONLY ONE COATING ACTIVE AT A TIME.** Using a new coating replaces the current one. **Switching resets the Charge Gauge.** Applying a coating costs **0 stamina** and deals weapon-element damage to one enemy.

Coatings: Power, Poison, Paralysis, Sleep, Flash, Exhaust (boosts Wyvernsoul), Attack Down, Accuracy, Defense Down.

Key skills:
- **Rapid Shot**: +2 Charge + damage. STAB variant at L5: consumes charge for high crit damage
- **Dragon Piercer**: Consumes charge, unleashes coating, single-target
- **Aerial Aim**: Consumes charge, unleashes coating, single-target
- **Battle Ready** (passive): Auto-activates a random coating at battle start; higher tiers start with charge
- **Deft Hands** (passive): +1 guaranteed charge on coating switch, chance for another +1 at higher tiers
- **Bow Mastery** (passive): Slight chance to gain +1 extra charge when filling

## Gunlance (Pierce)

- **Strengths**: Tankiest weapon, aggro drawing, shell damage ignores hitzones
- **Pairs with**: Any monstie that needs protection
- **Phase**: Great for defensive playstyles, endgame survivability

**Shell system (8 shells)**: Load via Guard Reload (2 shells + Guard) or H2H wins. Shell damage is fixed (ignores defense).

- **Shelling**: Consumes 2 shells, elemental damage + Guard
- **Charged Shelling**: Higher damage, more shells
- **Burst Fire**: Consumes ALL 8 shells for massive damage + Guard (L). 3× stamina cost
- **Wyvern's Fire**: Heavy explosion, massive damage, high stamina
- **Hail Cutter**: Overhead shell attack (manages Wyvern's Fire cooldown)
- **Derring Guard**: Brace 1 turn — boosts ATK/DEF relative to damage taken
- **Taunt**: Forces enemies to target you (aggro draw)
- **GL Mastery** (passive): Slight chance to load +2 extra shells
- **Audacious Wyvern** (passive): Increases Wyvern's Fire / Wyvern's Blaze damage

## Part Breaking

- Specific damage types deal bonus damage to specific parts (see `monsters/parts.psv`)
- Breaking parts: extra materials + can disable monster abilities (broken tail = weaker tail swipes)
- Focus fire on weak points for faster kills and better drops

## Weapon Progression (general)

| Phase | Recommendation |
|---|---|
| Early | Great Sword or Hammer — simple, powerful, easy to upgrade |
| Mid | Add Long Sword or Bow for variety |
| Late | All 6 have viable endgame builds; Hunting Horn + Gunlance shine in teams |

Weapons craft/upgrade using monster materials. Farm specific monsters for parts. See `weapons/{type}/params.psv` for per-level material costs.

## Field Tips

- **Hold A to gather** — much faster for bulk collection
- **Combining Menu** is for crafting potions/traps/consumables — recipes purchased from vendors (not auto-discovered)
- Swap weapons between fights freely — match damage type to the encounter

## Recommended Settings

- **Options > Camera > Auto-Centering → OFF**: Default is on (camera follows movement direction). Off gives manual analog stick control — run while looking behind, scout surroundings.
- **Options > Game Settings > Caution Icon Display**: Toggles dragon icon on much-higher-level overworld monsters.

## See Also

- [combat.md](combat.md) — combat fundamentals, Wyvernfell
- [weapons/weapons.md](../weapons/weapons.md) — cross-type weapon picks
- [monsters/parts.md](../monsters/parts.md) — part-break targeting
