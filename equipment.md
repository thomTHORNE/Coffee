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

**Nitrided steel Italmill conical burrs, 32 mm inner** (outer diameter disputed — see below). One grinder, two drive modes: crank it by hand, or twist it into the Arco Power Dock (bayonet mount) and a motor turns the same burrs at 360 rpm.

**All logged brews to date are electric-mode.**

The dock changes **how the burrs are turned, and nothing else.** Burr geometry, alignment, preload, the adjustment collar and the zero point are shared hardware. Any difference in the cup therefore has to come from burr **speed**, or from what speed drags along with it.

### Specifications

From the official Goat Story product page. **Not measured on this unit.**

| Spec | Value |
|---|---|
| Burrs | Conical, nitrided steel, **Italmill**. Outer diameter disputed — see below. Inner **32 mm** |
| Drive shaft | 10 mm steel, twin ball bearings |
| Body | Aluminium unibody, milled from a single piece |
| Adjustment | External setting ring. 60 clicks per rotation, 240 settings total (0/0 – 3/60) |
| Electric burr speed | **360 rpm.** High-speed AC motor, reduced |
| Hand burr speed | Not published. Hand cranking is roughly 60–120 rpm — *inference, not a source* |
| Duty cycle (electric) | ~6 espresso doses per 20 min. After 3 min continuous, rest 20–30 min |
| Noise (electric) | 65 dB |
| Catch cup | 50 g max — magnetic catch/doser, single-dose by design |
| Power | 110 V / 220 V |
| Size — hand grinder alone | 800 g, 180 × 63 × 190 mm |
| Size — docked (2-in-1) | **2,820 g**, 280 × 92 × 190 mm |

**The docked unit is 3.5× the weight of the grinder alone.** The dock is the mass. Relevant only in that the 2-in-1 is not a travel object once assembled — the hand grinder detaches and is.

⚠️ **Burr outer diameter: the official page contradicts itself.**

| Where | Figure |
|---|---|
| "Built to last" exploded diagram | `CONICAL BURR 47/32 NITRIDED STEEL` |
| Same page, body copy | "Premium **47/32mm** Italmill burrs" |
| Same page, Technical Specifications block | "Burr dimensions: **42mm** (outer)/32mm (inner)" |

Inner diameter agrees at 32 mm; outer is 47 in two places and 42 in one. Press coverage says 47, but that most likely inherits the marketing copy rather than confirming it independently — two sources repeating one source is still one source.

**Unresolved. Calipers settle it, nothing else will.** It changes no brewing decision — it changes only how this grinder reads against others, where 47 mm is Kinu-M47 territory and 42 mm is a step down. Previously this file recorded **38 mm**, which is wrong on either reading. See `corrections.md`.

### Calibration — verified sound

- Burrs chirp at `0/0`
- **1–2 further clicks to full lock.** This is normal burr preload. 1–2 is healthy; 5+ would indicate flex, wear, or a loose retaining nut
- Zero point is trustworthy. Rule out grinder mechanics as a source of variance
- The zero point is a **mechanical property of the collar and burrs**, so it does not move when you dock the grinder. What is untested is whether the same *gap* yields the same *particle distribution* under motor drive — see the mode-equivalence protocol below

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

**The chart is mode-blind.** It gives one number per method and does not say which drive mode it was derived on. Do not assume it applies to both. Note that every setting recorded in this journal was reached on the **electric** dock, so the working settings here are calibrated against that mode, not against hand.

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

**Every documented failure on this setup happened at 360 rpm.** The El Perezoso espresso work — sour at every setting, astringent until 0/26, never once bitter — is entirely electric-mode data. The one lever the low-rpm argument points at has never been pulled.

That matters for a specific reason. `principles.md` §7 says: *if a coffee never produces bitterness at any setting, the problem is upstream of the recipe — stop turning dials.* El Perezoso hit that wall. Eight espresso shots, no bitter wall found, the coarse end bracketed and the fine end never reaching over-extraction. The standing explanation is the conical uniformity ceiling below. **Hand mode is a way to test that explanation without buying a grinder** — same burrs, same gap, different rpm.

- If hand mode narrows the distribution, the shots should move *toward* the bitter wall at the same setting: more resistance, longer time, and finally something to over-extract against.
- If four hand-ground shots behave identically to electric, the ceiling is the burr geometry rather than the speed, and the remaining answers are a different grinder or a different bean.

Either result is worth having, and the second is worth as much as the first — it closes a line of inquiry that would otherwise sit open indefinitely.

Turbo's sensitivity to distribution is also why a *small* rpm effect might be visible here at all, when it would be invisible in a four-minute V60. That cuts both ways: it is the most sensitive available test, and the most likely to be swamped by noise.

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

- **Electric stays the default.** It is what every logged brew used, so it keeps new data comparable with old, and it removes your arm as a source of variance — worth more in practice than a contested fines argument. Switching the default now would orphan the existing dataset.
- **Hand is an experiment, not a habit** — run it as the deliberate A/B above, on the coffees the ceiling is known to punish (light, dense, hard-to-extract, on turbo). Don't drift into it casually; that just adds an untracked variable to a journal that has been bitten by exactly that twice.
- **Expect hand mode to be hard work at these settings.** The journal's espresso range is 0/26–0/32, well below the manufacturer's "espresso" band, on a 42–47 mm conical. Cranking a 15 g dose that fine is not a casual act, and grinding rate will vary through the dose in a way the motor's does not — which is itself a confound in the comparison. Crank as steadily as you can and note if you had to stop.
- **Mind the duty cycle** on electric: ~6 espresso doses per 20 min, and 20–30 min of rest after 3 minutes continuous. Not a constraint for one or two shots; a real one for a cupping session or a batch of filter doses.

### Logging — ELECTRIC IS THE DEFAULT

**Every brew in this journal is electric-mode unless the entry explicitly says hand-ground.** Past and future, no exceptions.

- **All brews logged to date: electric.** Confirmed by the user, not inferred. Every El Perezoso espresso and every filter brew is a 360 rpm data point.
- **Going forward: electric**, unless the user states otherwise for a specific brew.
- **Hand-ground brews get flagged in the entry.** An unflagged entry is electric — do not add a mode column, and do not ask which mode was used on a routine brew.

Consequences worth holding onto:

- The historical dataset is **mode-consistent**, so it is internally comparable. Nothing in it needs re-reading or discounting.
- **Hand mode has never been used for a logged brew.** Any hand-ground entry that appears is by definition an experiment, and the mode is then the one variable that moved.

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

| Source | Used for | Weight |
|---|---|---|
| **Official Goat Story product page** — "Built to last" diagram + Technical Specifications, supplied directly | All hardware specs: burrs, Italmill, shaft, motor 360 rpm, 65 dB, dimensions, weights, power, catch cup | Primary |
| Home-Barista Arco thread | Reports that the setting differs between modes | Forum-level, unconfirmed |
| Home Grounds; greenestbean | Laser-diffraction grind testing, the hand-mode low-rpm argument | Review-level |
| ManualsLib / retailer copies of the Arco manual | 60 clicks per rotation, 240 settings, duty cycle | Secondary |
| Coffee ad Astra, *"What I learned from analyzing 300 particle size distributions for 24 espresso grinders"* | Rpm does not cleanly predict uniformity across grinders | Strong, and it argues *against* the rpm claim |
| *Scientific Reports* (Mar 2024) | Grinder design affects share of fines independently of median size | Peer-reviewed |

**On provenance:** the hardware specs above are now first-party — read off Goat Story's own page rather than press coverage. The one thing the official page does *not* settle is its own burr outer diameter, and it says nothing at all about hand-versus-electric grind quality or setting equivalence. **The manufacturer makes no claim that the two modes differ.** The claim that they do is entirely forum and reviewer material, which is why it is written up above as a question with a protocol rather than as a finding.
