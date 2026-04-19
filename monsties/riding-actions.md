# Riding Actions — MHS3

Riding actions are overworld traversal abilities. Each monstie has a fixed set. You switch mounts freely from the field.

## Action Categories

**Utility:** Fly, Stealth, Roar
**Exploration:** Jump, Wall Climb, Swim, Ground Dive (unique to Canyne/Palamute)
**Combat:** Melee Attack, Breath

## How to Use

Hold the active monstie indicator, then map an action button. Some actions unlock passages you can't otherwise cross: Fly (gaps), Swim (water bodies), Wall Climb (vertical walls), Ground Dive (burrow passages), Stealth (avoid patrols/triggers).

## Finding a Monstie With an Action

Grep the PSV directly:

```
grep -i "^{name}" monsties/riding-actions.psv       # one monstie
grep -i "|swim=true" monsties/riding-actions.psv    # (pseudo) all swimmers
```

Actual schema:
```
monstie|general|jump|climb|swim|fly|underground|stealth|breath|...
```

So for "all Fly monsties":
```
awk -F'|' 'NR>2 && $6=="True" { print $1 }' monsties/riding-actions.psv
```

## Quick Reference — Action Holders (highlights)

| Action | Monsties |
|---|---|
| **Fly** | Most Flying Wyverns: Rathalos line, Rathian line, Nargacuga line, Astalos, Legiana, Paolumu, Diablos line, Seregios, Elder Dragons (Velkhana, Teostra, Kushala Daora, Namielle, Kirin, Nergigante), Malzeno |
| **Jump** | Nearly every monstie (default action) |
| **Wall Climb** | Zinogre line, Tobi-Kadachi, Nargacuga line, Silverwind, **Canyne/Palamute**, Goss Harag, Lunagaron, Magnamalo, Odogaron |
| **Swim** | Leviathans (Mizutsune, Lagiacrus, Royal Ludroth, Soulseer, Aurora Somnacanth), Plesioth, Tetranadon, Royal Ludroth, Shogun Ceanataur, Daimyo Hermitaur, Namielle |
| **Ground Dive** | **Canyne/Palamute only** — unique. Opens underground passages |
| **Stealth** | Nargacuga line, Silverwind, Purple Gypceros, Bishaten, Kirin |
| **Breath** | Rathalos line, Lagiacrus line, Astalos, Elder Dragons, Deviljho, Namielle |
| **Roar** | Most bosses (Flying Wyverns, Brute Wyverns, Fanged Wyverns, Elder Dragons) |

## Best Exploration Monsties

**Canyne (Palamute)**: unique Ground Dive + Wall Climb + Jump + Roar + Melee. Best all-around exploration monstie.

**Silverwind Nargacuga**: Jump + Wall Climb + Stealth — top for bypassing patrols on cliffs.

**Namielle**: Swim + Fly + Breath + Roar — rare combo, great for post-game water + air traversal.

## Deep Lookup

- `grep "^Canyne" monsties/riding-actions.psv` — one monstie's action flags
- `awk -F'|' '$6=="True"' monsties/riding-actions.psv | head` — all fliers

## See Also

- [monsties.md](monsties.md) — tier list + role picks
- [../habitats/habitats.md](../habitats/habitats.md) — which zones require which traversal
