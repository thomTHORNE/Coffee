# Corrections & Dead Ends

Things already tried and rejected, and answers previously given that were wrong. **Check this before proposing something that sounds obviously right** — most entries here sounded obviously right too.

---

## Previously wrong answers

Recorded so they aren't regenerated. Each was given confidently and was incorrect.

### "Dose up to 18 g — you have headspace in the basket"
**Wrong.** The basket is a **VST 15 g** (VST-152740r), not an 18 g. At 16 g the puck was already over-rated, not under-dosed. The weak pressure was never a puck-collapse problem — it was grind. Always confirm basket rating before reasoning about headspace.

### "Calibrate pump power on a blank portafilter"
**Wrong.** With no puck there's nothing to build pressure against; the gauge reads near zero at any power setting. Calibration only works on a real puck.

### "Hold the Manual button to bloom, release for full pressure"
**Wrong on this unit.** Manual runs the normal Pr + standard profile. It's the 1-cup/2-cup buttons that skip pre-infusion when held. Use `Pr15`/`PP55` for a programmed soak instead.

### "If you need 99% power to reach 6 bar, the grind is too fine"
**Backwards.** High power means high flow; if pressure is still only 6 bar, resistance must be *low* — the puck is too **coarse**. Work the equation (`pressure ≈ flow × resistance`) rather than reasoning from intuition.

### "As espresso cools, perceived acidity climbs"
**Imprecise.** Research indicates sourness from citric acid is largely unaffected by temperature. What actually happens is *unmasking*: sweetness fades with cooling, and sweetness was suppressing the sourness. The acid was constant. See `principles.md` §8.

### Prescribing from a single descriptor
Happened twice. "Bitter" alone pointed at grind; "bitter **and watery**" pointed at dose and ratio, and needed the opposite response. Always get both axes before diagnosing.

### Reaching for a 9-bar reference shot when the question was about turbo
The user's actual question was why turbo shots were failing. Defaulting to "establish a conventional baseline first" sidestepped it. Legitimate as a diagnostic, but it wasn't what was asked.

### Reasoning from the recommended recipe rather than the executed one
Happened twice. Ask what was actually done.

---

## Tested and rejected — espresso

| Approach | Result |
|---|---|
| Coarsening to fix low pressure | Backwards. Less resistance = less pressure. Dropped to 1 bar |
| Grind steps of 2–4 clicks | Too timid for an unknown range. Wasted brews across 12 clicks |
| Ratios beyond 1:3 (up to 1:3.75) | Dilutes an under-extracting puck. Never helped |
| Throttling PP to reach 6 bar | Achieves the gauge reading by forcing a finer grind and *lower* flow — the opposite of turbo. See `principles.md` §2 |
| Running 0/26 at full 9 bar | Coarse puck at full pressure = the original week-one failure. Undrinkable |
| Raising temperature | 96 °C is the ceiling. Cannot be tested further |
| Increasing dose to raise pressure | Adds path length, not surface area, and suppresses flow. Wrong lever for turbo |

---

## Tested and rejected — water

| Approach | Result |
|---|---|
| Tap water for filter | The cause of flat, muted, chemically-stinging cups. Discard all data from tap-water brews |
| Changing TWW packet concentration | Scales every ion together; cannot change the hardness-to-alkalinity ratio, which is the actual defect. Concentrating also raises sulfate, worsening dryness |
| TWW for filter brewing | Blocked by constraint — see `context.md`. Not a cost or logistics question to re-litigate |

---

## Deferred, not rejected

Set aside deliberately to control variables. Worth returning to once fundamentals are stable.

- **MHW-3Bomber Rain splitter** — distribution tool, currently an uncontrolled variable
- **Hario Switch immersion mode** — a real extraction lever for stubborn coffees, but the second experiment, not the first
- **TWW Medium Roast profile, or a 50/50 blend with Espresso** (~85–90 ppm alkalinity, chloride-free) — for espresso only
- **Refractometer** — DiFluid tier, not a €25 optical. Espresso is opaque and cheap optical units can't resolve the boundary line
- **Resting El Perezoso to day 18–20** before further espresso attempts
- **OPV verification** on the Sage — never checked, could shift every gauge reading
