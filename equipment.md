# Equipment — Verified Behaviour

Machine- and grinder-specific findings, established by testing on this hardware. **Where this contradicts general Breville/Sage or manufacturer guidance, trust this file.** Several procedures derived from general knowledge turned out to be wrong on this unit.

---

## Sage Dual Boiler

### Pre-infusion settings

Press both arrow buttons to access. Two values only:

| Setting | Range | Meaning |
|---|---|---|
| `Pr__` | 0–90 s | Pre-infusion duration |
| `PP__` | 55–99% | Pre-infusion pump power |

Factory default is `Pr07` / `PP60`.

There is **no multi-stage programming.** One profile: PP for Pr seconds, then full power.

### The low-pressure hack

Set `Pr` longer than the entire shot — e.g. `Pr40`. The machine never escalates, so the whole extraction runs at your `PP` setting. Stop the shot manually at target yield; it will not stop itself.

### Soak-then-escalate

Set `Pr` to the desired soak length (e.g. `Pr15`) at `PP55`. The machine escalates to full power automatically afterwards. At PP55 expect little or no output during the soak — that's correct, it's wetting the bed, not extracting. Start timing at the button, not at first drip.

### Button behaviour — CONFIRMED ON THIS UNIT

⚠️ This is the opposite of what general Breville documentation suggests.

- **Manual button:** does *not* hold at PP. Runs the normal Pr + standard profile.
- **1-cup / 2-cup buttons:** holding them **skips** pre-infusion and jumps straight to full power.

Do not propose a "hold Manual to bloom" procedure. It does not work here.

### Other confirmed facts

- **Brew temperature ceiling: 96 °C.** Hard limit.
- **Calibrating PP on a blank portafilter is useless.** With no puck there is nothing to build pressure against; the gauge reads near zero regardless of power. Calibrate on a real puck.
- **The gauge reads puck resistance, not a setting.** See `principles.md` §2.
- Ulka vibratory pump free-flows roughly 6–8 ml/s, so there is headroom to reach ~4.5 ml/s at 6 bar. The pump is not the limiting factor.

### Unverified

- OPV setting. Some units ship at 10.5 bar rather than 9, which would shift every gauge reading. Never checked.
- Slayer-style water-knob mod for manual flow profiling — mentioned as an option, never attempted.

---

## Arco by Goat Story — 2-in-1 (hand + electric dock)

**47 mm outer / 32 mm inner nitrided steel conical burrs.** One grinder, two drive modes: crank it by hand, or twist it into the Arco Power Dock (bayonet mount) and a motor turns the same burrs.

The dock changes **how the burrs are turned, and nothing else.** Burr geometry, alignment, preload, the adjustment collar and the zero point are shared hardware. Any difference in the cup therefore has to come from burr **speed**, or from what speed drags along with it.

### Specifications

Manufacturer- and press-sourced, **not measured on this unit.**

| Spec | Value |
|---|---|
| Burrs | 47 mm outer / 32 mm inner, nitrided steel, conical |
| Drive shaft | 10 mm, ball-bearing supported |
| Adjustment | 60 clicks per rotation, 240 settings total (0/0 – 3/60) |
| Electric burr speed | **360 rpm**, AC motor geared/belt-reduced (one source says ~350) |
| Hand burr speed | Not published. Hand cranking is roughly 60–120 rpm — *inference, not a source* |
| Duty cycle (electric) | ~6 espresso doses per 20 min. After 3 min continuous, rest 20–30 min |
| Noise (electric) | 62–65 dB |
| Catch cup | 50 g max — single-dose by design |
| Body | 800 g, 180 × 63 × 190 mm, aluminium unibody |

⚠️ **Burr size corrected.** This file and `context.md` previously recorded **38 mm**. Every source found says 47/32 mm. See `corrections.md`. Confirm with calipers when convenient — it does not change any brewing decision, but it does change how this grinder compares to others in reading.

### Calibration — verified sound

- Burrs chirp at `0/0`
- **1–2 further clicks to full lock.** This is normal burr preload. 1–2 is healthy; 5+ would indicate flex, wear, or a loose retaining nut
- Zero point is trustworthy. Rule out grinder mechanics as a source of variance
- Calibration was done by hand. **Whether the zero point reads identically under motor drive is untested** — see the mode-equivalence protocol below

### Manufacturer chart (Goat Story)

| Method | Range |
|---|---|
| Ibrik | 0/0–0/35 |
| Espresso | 0/30–0/60 |
| Moka pot | 1/0–1/40 |
| Filter | 1/30–2/20 |
| French press | 2/0–2/60 |
| Cold brew | 3/0–3/60 |

**Ignore the labels.** For 58 mm espresso at real pressure you will need far finer than the "espresso" band. Settings below 0/30 — nominally "ibrik" territory — are routinely correct.

**Ignore the "3 µm per click" claim.** It's a marketing figure; independent testing found resolution varies across the range. Adjust by result, never by micron arithmetic.

**The chart is mode-blind.** It gives one number per method and does not say which drive mode it was derived on. Given the open question below, treat it as a hand-mode chart by default.

---

## Hand vs electric — what actually differs

| Factor | Hand | Electric dock |
|---|---|---|
| Burr speed | Very low (~60–120 rpm, inferred) | **360 rpm**, motor-held |
| Speed stability *within* one dose | Varies — you slow on the hard part, speed up as it empties | Constant |
| Torque at the burr | Limited by your arm. Fine espresso settings are hard work and can bind | Gearbox. Does not stall at espresso fineness |
| Bean feed rate | Set by your crank rate | Set by the dock chute and burr speed |
| Heat into the grounds | Negligible | Low at 360 rpm, but non-zero — hence the duty cycle |
| Time for a 15 g espresso dose | Meaningful physical effort | Seconds |
| Operator technique as a variable | Present | Removed |

**The honest headline: this is a low-rpm mode versus a lower-rpm mode.** 360 rpm is slow for an electric grinder — many home electrics run four figures. The hand/electric gap here is far narrower than the phrase "hand versus electric" suggests, and that caps how large any quality difference can plausibly be.

### The quality claim, and how much to trust it

**The claim:** lower burr speed produces **fewer fines and a narrower particle distribution.** Mechanism: at higher rpm, fragments accelerate, struggle to exit the burr gap, bounce, and get re-fractured before they escape. Slower burrs let a particle leave once it is small enough. Reviewers make exactly this argument about the Arco — that hand mode is "about as low rpm as you can go," giving a conical a distribution closer to a flat's — and at least one frames the dual design as two taste profiles available at one setting.

**Where it weakens.** Cross-grinder data does not support rpm as a clean predictor:

- An analysis of ~300 particle size distributions across 24 espresso grinders found burr rpm **does not correlate clearly** with uniformity or unimodality. Some grinders made more fines at higher rpm; others did the reverse.
- A 2024 *Scientific Reports* paper found grinder design changes the share of fines **independently of median grind size** — two grinders can hit the same median and differ in fines.

So: rpm is a real mechanism, a poor cross-grinder predictor, and grinder-specific. Whether it moves *this* burr set by an amount the palate can find is **an open question, not a documented fact.** Nothing in this section has been tested on this unit.

*Distinguishing the layers: the 360 rpm figure and the hardware specs are sourced. The rpm→fines mechanism is sourced but contested. The claim that hand mode tastes better on this grinder is currently neither — it is a reviewer's assertion plus a plausible mechanism, and this journal has none of its own data on it.*

### Why it is worth testing here anyway

The conical uniformity ceiling below is the standing suspect behind **sour + astringent simultaneously** on El Perezoso turbo shots — wide distribution under short contact time. If hand mode narrows that distribution at all, it is a lever aimed at precisely that failure, and it costs effort rather than money. It is the cheapest remaining move against the ceiling, and it has never been tried deliberately, because until now the two modes were not being tracked as different.

That is also the ceiling on the claim: turbo's sensitivity to distribution is exactly why a *small* improvement might show up here when it would be invisible in a four-minute V60.

### Setting equivalence between modes — UNRESOLVED

Forum- and review-level reports say the **same setting number does not give the same grind** in hand versus electric. What is *not* established anywhere found:

- **Direction** — whether electric runs effectively finer or coarser
- **Magnitude** — how many clicks of offset, if any
- Whether Goat Story acknowledges it at all. No manufacturer statement was found

**Therefore: mode is a variable, not a convenience.** Switching modes mid-investigation without recording it breaks one-variable-per-brew as surely as changing the grind would. Do not carry a dialed-in setting across modes and assume it holds.

### Protocol to settle it — no refractometer required

The Sage gauge reads **puck resistance** (`principles.md` §2), and more fines means more resistance. The espresso machine is already the instrument; it does not need a refractometer to answer this.

1. **Fix everything but mode.** Same bag, same rest day, one setting, one dose, one basket, one `PP`, same puck prep.
2. **Alternate, don't batch.** Hand, electric, hand, electric — four shots. Alternating catches drift in bean rest and in your own puck prep.
3. **Record** plateau pressure, total time, and output flow in g/s. Watch the curve shape too (`principles.md` §8), not just the final number.
4. **Read it:**
   - *Electric slower / higher plateau* → electric is producing more fines or an effectively finer grind. Hand is the coarser-behaving mode, and the low-rpm argument holds on this unit.
   - *Hand slower / higher plateau* → the reverse, and the received wisdom does not apply here.
   - *No separation across four shots* → mode is not a meaningful lever at this setting. **Record that and stop spending brews on it.** A null result is the useful outcome, not a failed test.
5. **If they separate, get the conversion.** Move the other mode's setting in clicks until time and plateau match. That offset is the number worth having, and it belongs in this file.

**Cheaper cross-check on the Hario Switch:** open mode, fixed dose/grind/water/temperature, compare **drawdown time**. Slower drawdown = more fines. Filter costs less per data point than espresso and removes puck prep as a confound. Do this first if beans are short.

**Taste last, and only on a matched pair.** Once both modes are dialed to the *same* shot time and plateau pressure, a remaining taste difference is a distribution difference rather than a grind-size difference. That is the claim actually worth testing; comparing two shots at the same *setting* only tests whether the setting shifted.

### Practical selection, pending data

Until the above is run, this is preference and ergonomics, not quality:

- **Electric** for anything where repeatability matters more than a hypothesis — dialing in, filter, back-to-back comparisons of some *other* variable. It removes your arm as a source of variance, which is worth more than a contested fines argument.
- **Hand** where the effort is acceptable and the coffee is one the ceiling is known to punish — light, dense, hard-to-extract beans on turbo.
- **Mind the duty cycle** on electric: ~6 espresso doses per 20 min, and 20–30 min of rest after 3 minutes continuous. Not a constraint for one or two shots; a real one for a cupping session or a batch of filter doses.

### Logging

**Every brew from here records the mode.** A grind setting without a mode is now an incomplete record.

⚠️ Existing logs in the per-coffee files carry no mode column and predate the dock being documented. Unless corrected, read all of them as **hand-ground** — and treat that as an assumption, not a fact.

---

## The conical uniformity ceiling

This is the most consequential limitation of the setup, and it may be a hard ceiling on turbo shots specifically. It is a property of the **burrs**, so it applies in both drive modes — mode can only modulate it, not remove it.

**Setting sensitivity improves as you coarsen.** A 10 µm change against an 800 µm target is proportionally smaller than against 250 µm. Per click, coarse settings move you less.

**Particle uniformity gets worse as you coarsen.** Fines production is roughly constant in *absolute* terms regardless of burr gap — it comes from fracture mechanics and burr rubbing, not from the setting. At a fine setting those fines sit near the target size and the distribution is tight. At 700 µm you're still making 50 µm fines, so the spread widens dramatically. At wide gaps a fragment can also pass with fewer fracture events, making exit size more dependent on orientation. Conicals are worse at this than flats.

**Short contact time punishes spread.** A 900 µm boulder gives up something in a four-minute V60. In a 15-second turbo it contributes nothing while the fines over-extract. Same distribution, radically different consequence — and the reason turbo is grinder-dependent in a way filter brewing isn't.

**Counterpoint:** burr *alignment* error matters relatively more at fine settings, since fixed runout is a bigger fraction of a small gap. It's a genuine trade-off, not one-way.

**Implication:** Lance Hedrick's turbo work runs high-uniformity flat burrs. That isn't incidental to the technique. Sour *and* astringent simultaneously — which happened repeatedly on El Perezoso — is the signature of wide particle distribution under short contact time.

**Drive mode is the one untested lever against this ceiling.** See the protocol above. It is plausibly a small effect and may be none at all; it is worth four shots to find out, and it is worth *not* assuming.

---

## Sources

The official product page (`goat-story.com/products/arco-dual-coffee-grinder`) was **unreachable from the session that wrote this** — blocked by a network egress proxy — so the specs above come from press coverage, retail listings and the user manual as surfaced in search, not from the manufacturer directly. **Worth re-checking against the official page and the printed manual**, particularly the rpm figure and anything Goat Story says about mode equivalence.

| Source | Used for |
|---|---|
| Daily Coffee News, Arco launch coverage | Burrs, 10 mm drive shaft, motor |
| Sprudge, Arco 2-in-1 coverage | 360 rpm, belt drive, dock operation |
| Home Grounds; greenestbean | Reviews, laser-diffraction grind testing, the hand-mode low-rpm argument |
| Home-Barista Arco thread | Reports that the setting differs between modes |
| ManualsLib / retailer copies of the Arco manual | 60 clicks per rotation, 240 settings, duty cycle |
| Coffee ad Astra, *"What I learned from analyzing 300 particle size distributions for 24 espresso grinders"* | Rpm does not cleanly predict uniformity |
| *Scientific Reports* (Mar 2024) | Grinder design affects share of fines independently of median size |
