# Coffee Journal

Brewing log and accumulated knowledge. Espresso on a Sage Dual Boiler, filter on a Hario Switch, Arco 2-in-1 grinder (hand + electric dock).

## Structure

```
CLAUDE.md          instructions for Claude — behaviour, not data
README.md          this file
context.md         constraints, gear, prehistory
equipment.md       verified Sage + Arco behaviour
corrections.md     dead ends and previously wrong answers
principles.md      transferable brewing theory
coffees/           one file per bag
```

## Why the split

Each file has a different lifespan and a different reason to be opened.

- **`principles.md`** is theory. It generalises to any coffee and any setup, and it should rarely need revising.
- **`equipment.md`** is specific to this machine and this grinder. Durable, but only while the hardware is.
- **`corrections.md`** stops known-bad suggestions from being regenerated. It grows and never shrinks.
- **`context.md`** is standing facts about constraints and history.
- **`coffees/*.md`** is the only place that holds volatile data — current dial-in state, open questions, per-bag results.

`CLAUDE.md` deliberately holds none of the above. It's a map and a set of working rules, so it doesn't go stale when the brewing does.

## Adding a coffee

Copy an existing file from `coffees/`, replace the bag details and roaster specs, empty the tables. Keep espresso, filter and other methods in separate tables.

## Reporting a brew

Two axes, always:

```
Recipe: [dose, grind, water, temp, method, water source]
Time: [total]
Extraction: sour / balanced / bitter / ashy
Strength: watery / adequate / intense
Other: [astringency, notes, how it changes as it cools]
```

Record what was actually done, not what was planned.
