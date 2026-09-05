# CLAUDE.md

Coffee brewing journal and knowledge base. This file tells you how to work here. It deliberately contains no brewing data — that lives in the files below.

---

## Repo map

| File | Contains | Open it when |
|---|---|---|
| `context.md` | Standing constraints, gear inventory, brewing prehistory | Start of any session |
| `equipment.md` | Verified machine and grinder behaviour | Before suggesting any Sage procedure or grinder diagnosis |
| `corrections.md` | Previously wrong answers and tested dead ends | Before repeating a suggestion that "sounds obviously right" |
| `principles.md` | Transferable brewing theory | When reasoning about extraction, water, or technique |
| `coffees/*.md` | Per-bag logs: specs, every brew, tasting notes | When working on a specific coffee |

Read `context.md` first. Read the others when the task calls for them — don't load everything by default.

---

## Before you suggest anything

**Check `corrections.md`.** It records suggestions that were already tried and failed, and answers I previously got wrong. Several of them are the first thing a fresh session would reach for. Regenerating them wastes the user's coffee and time.

**Check `equipment.md` before any machine or grinder advice.** General Breville/Sage guidance does not match this unit. Three procedures derived from general knowledge turned out to be wrong on this machine. Trust the file over your training.

---

## Tasting vocabulary — use this in both directions

Never diagnose from a single descriptor. Every cup gets one term from each axis.

**Extraction:** sour → balanced → bitter → ashy
**Strength:** watery → adequate → intense

Four terms that get confused and mean different things:
- **Muted** — flavours present but low-contrast. Usually a *strength* problem
- **Flat** — flavours genuinely absent. Usually *extraction*, *water*, or *roast*
- **Astringent** — a drying, grippy *texture*. Signals channeling
- **Bitter** — a *taste*. Signals over-extraction

`bitter + watery` and `bitter + intense` need opposite responses. Ask for the second axis if it's missing.

---

## Standing constraints

These are stable facts. Recommendations that ignore them are wrong before they're evaluated.

- **Distilled water is reserved for the espresso machine.** Bought at a convenience store, provenance unknown, not trusted for drinking in filter volumes. Do not propose Third Wave Water for filter brewing.
- **TWW is a cost constraint**, not a default. Filter water comes from bottled spring water.
- **Location: Croatia.** Source recommendations accordingly.
- **Sage Dual Boiler brew temperature ceiling is 96 °C.** Any advice above that is unusable.

---

## Working preferences

- **One variable per brew.** If the user reports a result where two things changed, say so before interpreting it.
- **Ask what was actually done**, not what was recommended. These have diverged more than once.
- **Bracket before narrowing.** When a coffee's range is unknown, find both walls — sour *and* bitter — before making small adjustments. Small increments across an unknown gap waste brews.
- **Distinguish sourced fact from inference.** The user pushes back on unsupported claims and is right to. If a chain of reasoning is assembled from separate findings rather than a direct source, say so.
- **Expect correction.** The user has caught real errors here. Take the correction, revise the position, don't defend it.
- **Numbers over adjectives.** Flow rates, ratios, and gauge readings, not "a bit finer."

---

## Logging

When a brew is reported, append it to the relevant `coffees/*.md` table. Keep espresso, filter, and other methods in separate tables. Record what was done, not what was planned.

**Grind settings are electric-mode unless the entry says hand-ground.** The Arco is a hand/electric 2-in-1; every brew logged so far is electric, and that's the standing default. Don't add a mode column and don't ask which mode on a routine brew — only a hand-ground brew needs flagging.

When a finding generalises beyond one bag, it belongs in `principles.md`. When it's specific to this machine or grinder, `equipment.md`. When it's a rejected approach, `corrections.md`.
