# Items — MHS3

1172 items in total (full catalog in PSV). This cheat sheet covers **essentials** — the items you'll use most. For everything else, grep.

## Healing & Recovery

| Item | Effect | Source |
|---|---|---|
| Potion | Restores small HP | Herb + Stone crafting / shop |
| Mega Potion | Restores moderate HP | Honey + Potion |
| Lifesoot | Revives a fainted monstie with some HP | Herb + Stone |
| Nulberry Elixir | Universal single-target status cure | Shop / craft |
| Antidote | Cures Poison (single) | Crafted |
| Antidote Powder | Cures Poison + Negates future (AoE) | Crafted |
| Burn Ointment / Paracare / Intuitizer / Zest Pill / Soap Scud | Cure specific statuses | Crafted |
| Energy Drink | Wakes a Sleeping target | Crafted |
| Sushifish | Cure Bleeding + Regen | Field item |

## Stamina

| Item | Effect |
|---|---|
| Energy Drink | +30 Stamina (also wakes Sleep) |
| Nourishing Pinecones | 0-cost active — recovers user's stamina (from Blood Orange Bishaten, Tarkuan) |

## Trap & Control

| Item | Effect |
|---|---|
| Pitfall Trap | Pits monster in place (misses turn) |
| Shock Trap | Stun trap (Thunder damage + skip) |
| Mad Trap | AoE damage + confuse |
| Sonic Bomb | Stun chance — powerful vs enemies with high `sonic_bomb_rate` |
| Paintball | Marks monster — forces retreat to nest for egg farming |

## Eggs & Farming

| Item | Effect |
|---|---|
| SR Expedition Ticket | **100 Bottle Caps** at Bottle Cap Trader. Guarantees high-rank den |
| Training Talisman | Excursion currency — Melynx Emporium, Silver Trade Points |

## Consumables Marked "Egg Skill:"

Some items trigger specific egg-skill effects on the field. Most useful in Expedition farming.

## Currency & Trade

| Currency | Use |
|---|---|
| Zenny | Standard currency |
| Bronze Trade Points | Melynx Emporium basic goods |
| Silver Trade Points | Training Talismans, mid-tier decorations |
| Gold Trade Points | Rare decorations, high-tier materials |
| Bottle Caps | SR Expedition Tickets (100 each) |

## Crafting Recipes (36)

All crafting recipes: `cat items/recipes.psv`. Schema: `result|ing1|qty1|ing2|qty2|ing3|qty3|recipe_flag`.

Examples:
- **Potion**: Herb × 1
- **Mega Potion**: Potion × 1 + Honey × 1
- **Antidote**: Antidote Herb × 1
- **Shock Trap**: Thunderbug × ?, Trap Tool × ?

Grep for specific recipes:
```
grep "^IT_MEDICINE_001 (Herb)" items/recipes.psv    # all recipes using Herb
grep "Mega Potion" items/recipes.psv
```

## Materials

Most items are crafting materials rather than direct-use consumables. Categories:
- **Monster materials** (hide, scale, fang, claw, horn, etc.) — for weapons/armor upgrades
- **Ore & minerals** — Low-Grade Ore, High-Grade Ore, etc.
- **Bug materials** — Rachnoid Silk, Dragonbug Juice, Hercudrome, etc.
- **Trace items** — items dropped by visiting nests (Monster Book items)

Full material list: `cat items/items.psv` (1172 rows — use grep).

## Deep Lookup

- `grep -i "potion" items/items.psv` — all potion variants
- `grep -i "trap" items/items.psv` — trap items
- `grep "^IT_MEDICINE" items/items.psv` — medicine category
- `grep "^IT_MATERIAL_024 (Stone)" items/items.psv` — one specific item

## See Also

- [meals.md](meals.md) — kitchen system (separate from items)
- [../allies/allies.md](../allies/allies.md) — partner-specific unlocks
- [../eggs/eggs.md](../eggs/eggs.md) — SR tickets, paintball trick
- [../zones/](../zones/) — where to find region-specific materials
