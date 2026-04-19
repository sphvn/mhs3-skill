# Kitchen & Meals — MHS3

The Kitchen system lets you cook meals that provide pre-battle buffs and stat bonuses. Different from consumable items (potions).

## Core Mechanics

- **Meals are cooked before expeditions** at Kitchen facilities in base camps.
- Each meal has **bonus HP / Attack / Defense / Stamina** values and a **Meal Buff** effect.
- Buffs persist until you rest at camp or take heavy damage.

## Meal Types

5 base meal types (from `items/meals.psv`):

| Base Meal | Meal Buff | Purpose |
|---|---|---|
| [Meal 1] | Increases starting Stamina | General utility |
| [Meal 2] | — | — |
| [Meal 3] | — | — |
| [Meal 4] | — | — |
| [Meal 5] | — | — |

(Currently only 4 meals extracted — the datamine has limited meal data. Cross-reference with in-game Kitchen menu.)

## Stat Bonuses

Each cooked meal provides combinations of:
- Bonus HP (flat max-HP increase for the expedition)
- Bonus Attack
- Bonus Stamina Attack (affects Stamina-based attacks)
- Bonus Defense
- Bonus Starting Stamina
- Bonus Stamina Recovery

## Ingredients

Meals require specific ingredients (listed per-meal in `meals.psv`). Common ingredients:
- Fish caught while fishing
- Meat from monster drops
- Vegetables from herb gathering
- Rare ingredients as quest rewards

## Strategy

- Cook a meal before **SR expeditions** (post-game) — stat boosts stack with Excursion stat bonuses and gene buffs.
- Match meal buff to the fight: +Stamina for long elder-dragon fights, +Defense for high-damage bosses.
- Favorite NPC mechanic: some meals are favorites/dislikes of specific NPCs, affecting interactions.

## Deep Lookup

```
cat items/meals.psv
```

Schema: `name|base_meal|description|purpose|report|bonus_hp|bonus_attack|bonus_stamina_attack|bonus_defense|bonus_starting_stamina|bonus_stamina_recovery|meal_buff_desc|base_meal_buff_desc|materials|quantities`.

## Note on Limited Data

Current extract pulled only 4 meals. For the full in-game menu, cross-reference:
- In-game Kitchen → Base Meals list
- Capcom manual → Kitchen section (`.xlsx-source/capcom-manual/by-category/facilities.md`)

## See Also

- [items.md](items.md) — consumables (potions, traps)
- [../progression/rider.md](../progression/rider.md) — rider HP/ATK scaling that meals stack on top of
- [../zones/](../zones/) — fishing / gathering spots for ingredients
