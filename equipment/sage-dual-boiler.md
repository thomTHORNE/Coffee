# Sage Dual Boiler

Espresso machine. 58 mm portafilter, vibratory pump. Findings below are established by testing on this specific unit. **Where this contradicts general Breville/Sage or manufacturer guidance, trust this file.** Three procedures derived from general knowledge turned out to be wrong here.

---

## Confirmed

### Pre-infusion settings

Press both arrow buttons to access. Two values only:

| Setting | Range | Meaning |
|---|---|---|
| `Pr__` | 0–90 s | Pre-infusion duration |
| `PP__` | 55–99% | Pre-infusion pump power |

Factory default is `Pr07` / `PP60`.

There is **no multi-stage programming.** One profile: PP for Pr seconds, then full power.

### The low-pressure hack

Set `Pr` longer than the entire shot — e.g. `Pr40`. The machine never escalates, so the whole extraction runs at your `PP` setting. Stop the shot manually at target yield; it will not stop itself. Brewed on this unit (El Perezoso E4).

### Soak-then-escalate

Set `Pr` to the desired soak length (e.g. `Pr15`) at `PP55`. The machine escalates to full power automatically afterwards. At PP55 expect little or no output during the soak — that's correct, it's wetting the bed, not extracting. Start timing at the button, not at first drip. Brewed on this unit (El Perezoso E7).

### Button behaviour

⚠️ This is the opposite of what general Breville documentation suggests.

- **Manual button:** does *not* hold at PP. Runs the normal Pr + standard profile.
- **1-cup / 2-cup buttons:** holding them **skips** pre-infusion and jumps straight to full power.

Do not propose a "hold Manual to bloom" procedure. It does not work here.

### Other confirmed facts

- **Brew temperature ceiling: 96 °C.** Hard limit.
- **Calibrating PP on a blank portafilter is useless.** With no puck there is nothing to build pressure against; the gauge reads near zero regardless of power. Calibrate on a real puck.
- **The gauge reads puck resistance, not a setting.** See `principles.md` §2.
- Ulka vibratory pump free-flows roughly 6–8 ml/s, so there is headroom to reach ~4.5 ml/s at 6 bar. The pump is not the limiting factor.

---

## Pending / To verify

- **OPV setting.** Some units ship at 10.5 bar rather than 9, which would shift every gauge reading. Never checked.
- **Slayer-style water-knob mod** for manual flow profiling — mentioned as an option, never attempted.
