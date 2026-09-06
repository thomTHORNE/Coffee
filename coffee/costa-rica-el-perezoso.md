# Costa Rica — El Perezoso

## Bag details

| Field | Value |
|---|---|
| Roaster | Goat Story (EQUA d.o.o., Ljubljana) |
| Roast date | 25.08.2026 |
| Bag size | 500 g |
| Variety | Caturra / Catuai |
| Process | Natural |
| Altitude | 1,300–1,600 m |
| Roast level | Medium |
| Cupping score | 85 |
| Roaster tasting notes | Sour cherry, chocolate, winey dryness |
| Link | https://goat-story.com/products/costa-rica-el-perezoso |

### Roaster's recommended recipes
- **Espresso:** 18 g in → 40–42 g out, 27 s, 94 °C, grind ~250 µm
- **Filter:** not recorded — check bag/site if needed

---

## Equipment used for this bag
- **Espresso:** Sage Dual Boiler, VST 15 g ridgeless basket (VST-152740r)
- **Filter:** Hario Switch
- **Grinder:** Arco by Goat Story 2-in-1 (47/32 mm conical), zero point verified — chirp at 0/0, 1–2 clicks to full lock.
  **All brews below are electric (360 rpm)** — the standing default. Hand mode is untried on this coffee; a hand-ground brew would be flagged as such. See `equipment/arco-grinder.md`
- **Water (espresso):** Third Wave Water Espresso profile, 1 packet / 2 L
- **Water (filter):** ⚠️ tap water used for all filter brews to date — see notes

---

## Espresso log

### Phase 1 — before pre-infusion hack (machine at default Pr7 / PP60)

| # | Date | Grind | Dose | Yield | Time | Pressure | Temp | Extraction | Strength | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| E1 | ~30.08 | 0/32 | 16 g | 55–59 g | 23 s | 3 | 96 | sour | — | astringent; 1:3.6, flow 2.5 g/s |
| E2 | ~30.08 | 0/32 | 16 g | 44–47 g | — | 3 | 96 | sour | — | astringent |
| E3 | ~30.08 | 0/38 | 16 g | 48 g | — | 1 | 96 | sour | — | astringent; coarsened — wrong direction |

**Phase 1 conclusion:** astringency = channeling. Grind far too coarse; gauge readings were transient, not plateaus.

### Phase 2 — pre-infusion hack (Pr40, PP throttled)

| # | Date | Grind | Dose | Yield | Time | Pressure | Temp | Extraction | Strength | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| E4 | ~02.09 | 0/26 | 16 g | 45 g | 30 s | plateau 6 (PP-capped) | 96 | sour | adequate | **Astringency gone** — channeling solved. No bitterness at all. Flow 1.5 g/s |
| E5 | ~03.09 | 0/29 | 15 g | 50 g | 19 s | 3–4 | 96 | sour | watery | ⭐ **Best shot.** Sour cherry, chocolate cherry, winey dryness at first sip — roaster's notes hit. Faded to prominently sour on cooling |

### Phase 3 — reverting and re-testing

| # | Date | Grind | Dose | Yield | Time | Pressure | Temp | Extraction | Strength | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| E6 | 04.09 | 0/26 | 16 g | 47 g | 26 s | pinned 9, climbing | 96 | sour | — | Pr7/PP75, normal mode. Undrinkable. Puck restrictive even at 9 bar |
| E7 | 05.09 | 0/28 | 16 g | 60 g | 30 s | 5→3 | 96 | sour | — | Pr15/PP55 soak-then-escalate. Undrinkable. 1:3.75 |
| E8 | 05.09 | 0/26 | 16 g | 60 g | — | 6→5 | 96 | sour | — | Undrinkable |

**Espresso conclusion:** 12 clicks of grind, 1–9 bar, 19–30 s, 1:2.8–1:3.75, three pressure profiles. **Never once produced bitterness.** Espresso path could not reach adequate extraction on this coffee.

---

## Filter log

| # | Date | Method | Dose | Water | Grind | Temp | Time | Water source | Extraction | Strength | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| F1 | 05.09 | Switch open, percolation | 15 g | 250 g | 1/30 | boiling | — | tap | bitter | watery | Muted, nothing stands out. Bottom-right of brew chart: high EY, low TDS |
| F2 | 05.09 | Switch open, percolation | 22 g | 330 g | 1/30 | boiling | 3:00 | tap | ambiguous | adequate | Body fixed. Completely flat — "tasteless medicine." Stinging edge, neither clearly sour nor bitter |
| F3 | 06.09 | Switch open, percolation | 22 g | 330 g | 1/30 | boiling | 3:00 | Sara natural mineral water diluted 1:1 with distilled (~129 mg/L HCO₃, ~101 mg/L dry residue, inferred) | sour | adequate | Bloom 50 g/45 s → 200 g → 330 g, matching F2 exactly bar water. **Medicinal sting completely gone** — chlorine mechanism confirmed. Flat, no characteristics, **zero sweetness**. Clean, pleasant acidity/brightness once cooled. Possible bitterness while hot — **low confidence**, palate untested that morning (only water beforehand), not treated as verdict |

**⚠️ F1/F2 used chlorinated tap water — that data stays invalid.** F3 is the first clean (non-tap) filter data point on this bag. Flat + chemical sting + adequate body was the tap water signature; F3 confirms the sting was chlorine specifically — it's gone with dechlorinated water, while the flatness/no-sweetness persisted. That isolates flatness as *not* a chlorine effect, but doesn't yet say what it is: grind has never been varied on filter (all three brews at 1/30), so it hasn't been ruled out as the cause. See pending steps.

---

## Pending / next steps

- [x] ~~Re-brew F2 recipe with Sveti Rok~~ — done with diluted Sara (1:1 distilled) instead, as the only available option that morning; F3 above. Provenance caveat on the distilled component still stands, unresolved
- [ ] **Next: isolate grind on filter.** All three filter brews used 1/30 — grind has never been the varied factor. F3 read as textbook "sour" (sharp/acidic, thin, no sweetness) per `principles.md` §4's extraction table, and strength already reads adequate, so the indicated single-variable fix is finer grind alone (not ratio — that's only for when strength also needs correcting). Keep dose, ratio, water, temp, and pours identical to F3; move grind a real step finer, not a token click or two (see `corrections.md` on timid steps costing brews across an unknown range). Watch drawdown time — a finer grind should extend it on its own
- [ ] Holding off on "underdeveloped roast" as a conclusion. It remains one open hypothesis, not the diagnosis — grind is untested on filter and needs ruling out first, especially since `equipment/arco-grinder.md` flags the manufacturer's per-method grind chart as unreliable in general (already shown wrong for espresso)
- [ ] If a meaningfully finer grind still comes back sour/flat/no-sweetness → that starts to look like a real cross-check per `principles.md` §7 ("if espresso can't over-extract but filter can, the espresso path is the limitation, not the bean" — the converse: if filter *also* can't push past sour even pushed hard, the limitation is upstream of both methods)
- [ ] If clean filter cup is sweet → coffee is fine, espresso path is the problem
- [ ] Consider resting bag to day 18–20 before further espresso attempts
- [ ] Untried espresso variable: nothing left of consequence. 96 °C is the machine ceiling

## Open hypotheses

1. **Underdeveloped roast** — one candidate, not concluded. Sourness with no sweetness is consistent with it, but grind has never been varied on filter, so it hasn't been isolated from a simple under-extraction explanation yet
2. **Insufficient rest** — all espresso pulled at day 5–10 on a dense natural; filter (F3) was day 12
3. **Arco conical distribution ceiling** — at espresso settings, bimodal grind means boulders under-extract while fines channel
4. **Palate mismatch** — the roaster's "sour cherry" may simply read as plain sour
5. **Filter grind untested, not just water** — every filter brew to date sits at the same 1/30 setting; the flat/no-sweetness result survived removing chlorine, but hasn't yet been tested against a real change in extraction via grind

## Reference: comparison coffee

**Ethiopia Sidama Yaye** — a similar turbo recipe was noticeably more satisfying on this coffee. Consistent with turbo's documented domain (light, dense, hard-to-extract coffees).
