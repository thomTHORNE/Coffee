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

## Arco by Goat Story

38 mm **conical** burrs, hand grinder.

### Calibration — verified sound

- Burrs chirp at `0/0`
- **1–2 further clicks to full lock.** This is normal burr preload. 1–2 is healthy; 5+ would indicate flex, wear, or a loose retaining nut
- Zero point is trustworthy. Rule out grinder mechanics as a source of variance

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

### The conical uniformity ceiling

This is the most consequential limitation of the setup, and it may be a hard ceiling on turbo shots specifically.

**Setting sensitivity improves as you coarsen.** A 10 µm change against an 800 µm target is proportionally smaller than against 250 µm. Per click, coarse settings move you less.

**Particle uniformity gets worse as you coarsen.** Fines production is roughly constant in *absolute* terms regardless of burr gap — it comes from fracture mechanics and burr rubbing, not from the setting. At a fine setting those fines sit near the target size and the distribution is tight. At 700 µm you're still making 50 µm fines, so the spread widens dramatically. At wide gaps a fragment can also pass with fewer fracture events, making exit size more dependent on orientation. Conicals are worse at this than flats.

**Short contact time punishes spread.** A 900 µm boulder gives up something in a four-minute V60. In a 15-second turbo it contributes nothing while the fines over-extract. Same distribution, radically different consequence — and the reason turbo is grinder-dependent in a way filter brewing isn't.

**Counterpoint:** burr *alignment* error matters relatively more at fine settings, since fixed runout is a bigger fraction of a small gap. It's a genuine trade-off, not one-way.

**Implication:** Lance Hedrick's turbo work runs high-uniformity flat burrs. That isn't incidental to the technique. Sour *and* astringent simultaneously — which happened repeatedly on El Perezoso — is the signature of wide particle distribution under short contact time.
