# Brewing Principles

Transferable theory. Applies to any coffee and, mostly, any setup. Machine-, grinder-, and brewer-specific findings live in `equipment/`.

---

## 1. Two-axis tasting vocabulary

Never diagnose from a single descriptor.

**Extraction** (how much came out)
| Term | Means |
|---|---|
| Sour | Sharp, acidic, thin finish, no sweetness. Under-extracted |
| Balanced | Sweetness present, notes distinguishable |
| Bitter | Harsh, drying, lingering. Over-extracted |
| Ashy | Burnt, charred. Far over |

**Strength** (how concentrated)
| Term | Means |
|---|---|
| Watery | No presence, dilute, notes wash out |
| Adequate | Has body, coats the mouth |
| Intense | Heavy, syrupy, hard to drink much of |

**Confusable terms:**
- **Muted** — flavours present but low-contrast. Usually *strength*
- **Flat** — flavours genuinely absent. Usually *extraction*, *water*, or *roast*
- **Astringent** — mouth-drying, grippy *texture*. Signals **channeling**, not over-extraction
- **Bitter** — a *taste*. Signals over-extraction

**Reporting format:**
```
Recipe: [dose, grind, water, temp, method, water source]
Pours (filter only): [bloom size/time, then each subsequent pour target]
Time: [total]
Extraction: sour / balanced / bitter / ashy
Strength: watery / adequate / intense
Other: [astringency, specific notes, how it changes as it cools]
```

**Grinder drive mode is assumed electric.** The Arco is a 2-in-1 and every brew here is electric-mode; only *hand-ground* brews need saying so, and then it's the one variable that moved. See `equipment/arco-grinder.md`.

---

## 2. Pressure is not a setting

**pressure ≈ flow rate × puck resistance**

One readout, two variables. Consequences:

- Full power at 6 bar → low resistance, coarse puck, high flow (~4 ml/s). **This is a turbo shot**
- 60% power at 6 bar → high resistance, finer puck, low flow (~2.5 ml/s). **This is low-pressure profiling.** Different technique, different cup
- The gauge cannot distinguish them
- A pump-power percentage is **not portable** — it depends on the puck it's pushing against

**Corollary:** to raise pressure, grind finer. Coarsening lowers it. This is counter-intuitive if you're used to thinking of low pressure as a symptom of a fine grind — in a pressure-limited context the logic inverts.

---

## 3. Turbo shots

| Parameter | Spec |
|---|---|
| Pressure | ~6 bar (not 3) |
| Ratio | 1:3 |
| Time | 7–20 s |
| Input flow | ~4.5 ml/s (water *into* the puck) |
| Output flow | ~2.5–3 g/s (what the scale sees) |
| Suits | Light, dense, hard-to-extract coffees |
| Doesn't suit | Dark roasts; already-sweet medium roasts |

**Measurement trap:** published turbo flow rates are *input* flow. The puck retains roughly 2 g water per gram of coffee. For 15 g: 45 g in the cup plus ~30 g retained = ~75 g through the pump.

**Troubleshooting rule:** sour → grind **finer** and shorten the yield. Never coarser.

**Grinder dependency is load-bearing**, not incidental. See `equipment/arco-grinder.md`.

**What turbo is for:** trading contact time for a wider, more even fluid front, so you get higher extraction without the bitter fraction. If a coffee produces no bitterness to begin with, turbo is solving a problem that doesn't exist while costing contact time you need.

---

## 4. Extraction and strength are independent

The brewing control chart has two axes for a reason.

- **Ratio sets strength.** Grind, temperature and contact time set extraction
- Sourness lives at **low extraction yield**, regardless of strength. Target 18–22% EY
- **The trap:** shortening the ratio without changing grind raises TDS without raising EY. That lands you top-left on the chart — ristretto territory, intense *and* sour. Same defect, concentrated
- **The fix for sour:** grind finer *and* shorten the ratio together. Extract more sugar, then concentrate it. Concentrating the sugar you already have is the failure mode
- **Bitter + watery** (bottom-right) needs the opposite response to **bitter + intense** (top-right)

**Bed geometry matters independently of ratio.** 15 g/225 g and 22 g/330 g are the same ratio but different brews — a shallow bed cools faster and runs long, pushing extraction up. Raising dose fixes wateriness *and* reduces over-extraction; cutting water fixes only the first.

---

## 5. Water

The single biggest variable and the easiest to get wrong.

**Tap water signature:** flat, muted, faintly chemical or medicinal sting, aromatics stripped, body can still be fine. Three mechanisms:

1. **Chlorine / chloramine** — strips aromatics, leaves a chemical edge. Chlorine off-gasses if water stands; chloramine survives boiling
2. **High bicarbonate** — neutralises coffee acids, and the acids carry fruit, floral and sweetness perception. Doesn't produce bitterness; produces *nothing*
3. **Calcium-dominant hardness** — magnesium is the extraction-active ion; calcium skews toward the dull fraction

**Targets:**
| Metric | Target |
|---|---|
| Bicarbonate (HCO₃⁻) | under 60 mg/L |
| Dry residue / TDS | 50–150 mg/L |

### Third Wave Water

| Profile | Composition | TDS | Alkalinity |
|---|---|---|---|
| Espresso | Mg sulfate, Na bicarb, K bicarb (no calcium) | ~132 ppm hardness | **~37 ppm** — very low buffering |
| Medium Roast | Mg sulfate, Ca citrate, Na bicarb | ~180 mg/L | ~135–140 ppm |
| Classic/Light | contains **sodium chloride** | — | ⚠️ keep out of espresso machines |

- **Scale safety:** TWW creates *permanent* hardness (sulfate/citrate), which does not form limescale. The risk to avoid is **chlorides**, which corrode
- **Concentration is the wrong knob.** Diluting or concentrating scales every ion together and cannot change the hardness-to-alkalinity ratio. Only a different formulation does
- Sulfate contributes a drying, drawing sensation — relevant if a cup already reads as dry

### Croatian bottled water (filter)

| Brand | HCO₃⁻ mg/L | Dry residue | Verdict |
|---|---|---|---|
| **Sveti Rok** | 177.2 | 181 | ✅ Best readily available. 7 L format |
| Jana | 358–381 | 277–286 | ❌ Too buffered |
| Studena | 406.5 | 336 | ❌ Worst |
| Cetina, Gacka, Goda, Aqua Sana, Santa, Viva | ? | ? | Check labels |

On the label, look for *hidrogenkarbonati* and *isparni ostatak*. Spring waters (*izvorska*) generally run lower than mineral waters (*mineralna*).

Sveti Rok at 177 is still roughly 3× ideal — a large improvement over tap, not as clean as TWW.

---

## 6. Temperature and the cooling curve

- Perceived **sweetness decreases as a drink cools** — well-replicated for sucrose
- Perceived **sourness is largely unaffected** by temperature
- Sweetness and sourness **suppress each other** in mixtures

**Therefore:** a cup that's good hot and sour cold isn't becoming more acidic. It's losing the sweetness that was masking the acid. Unmasking, not intensification.

This is why SCA cupping evaluates the same cup at three temperatures — sweetness and subtle defects become perceptible as it cools, and a good coffee holds up across the range. A cup that collapses on cooling is a recognised failure mode, and it points at insufficient dissolved solids rather than at the acid.

*Note: this chains three separate well-established findings rather than resting on a single study of espresso cooling.*

---

## 7. Method discipline

- **One variable per brew.** Violated twice here; both datasets were unusable
- **Record every field every time**, especially time
- **Bracket before narrowing.** Find both walls — sour *and* bitter — before making small adjustments. Small increments across an unknown gap waste brews
- **If a coffee never produces bitterness at any setting**, the problem is upstream of the recipe: roast development, rest, water, or grinder ceiling. Stop turning dials
- **Cross-check with a different method.** Filter immersion at boiling applies far more extraction force than espresso. If espresso can't over-extract but filter can, the espresso path is the limitation, not the bean
- **Measure if taste stalls.** Refractometer target 18–22% EY

---

## 8. Reading a shot as it runs

Flow rate isn't an independent variable — fix dose, yield and time and it's determined. But watching it live catches things a final time can't:

- **Healthy:** ramps over the first few seconds, then holds steady
- **Channeling:** accelerates mid-shot. A path has opened
- **Stalling:** decays steadily. Fines migration clogging the bed — too fine

Two shots can hit the same yield in the same time and be completely different cups. At the spouts, sudden thinning or a sputtering stream is the visible signature of a channel.

Let a shot finish even if it's clearly off. A short shot is still a data point and a reference taste; aborting gives neither.

---

## 9. Rest and degassing

- Espresso windows for medium roasts typically fall around two to four weeks. Naturals hold CO₂ longer than washed
- Dialing during the first ten days means dialing against a moving target
- **Low-pressure extraction is disproportionately affected.** Dissolved CO₂ stays in solution under pressure and evolves as pressure drops — at 9 bar it largely stays put, at 3–6 bar it comes out inside the puck, disrupting the flow front mid-extraction. Fresh coffee plus low pressure is the worst combination for erratic results
