# Lab 2 Technical Summary — Frequency Response of Systems

Reference summary of the verified theory, experimental oscilloscope data, and audit corrections incorporated into `lab2_frequency_response/report/Lab_Report2.pdf` and `Lab_Report2.docx`.

---

## 1. Circuit & Transfer Function
- **Topology:** Series RC low-pass filter (`R = 1.5 kΩ`, `C = 0.01 µF = 10 nF`), output `vo(t) = vC(t)` measured across the capacitor.
- **Governing LCCDE:** `RC dv_o(t)/dt + v_o(t) = v_i(t)` with time constant `τ = RC = 15 µs`.
- **Frequency Response:**
  - `H(jω) = 1 / (1 + jωRC)`
  - `|H(jω)| = 1 / √(1 + (ωRC)²)`
  - `∠H(jω) = −arctan(ωRC)`
- **−3 dB Cut-Off Frequency:** `fc = 1 / (2πRC) = 10,610.3 Hz ≈ 10.61 kHz` (`|H| = 1/√2 = 0.7071`, `−3.01 dB`, `∠H = −45.00°`).
- **Probe Loading Check:** Keysight DSOX4024G Ch2 passive input (`1 MΩ ∥ 16 pF`) yields DC divider `0.9985` (`−0.013 dB`) and shifts `fc` to `10,609.3 Hz` (`<0.01%`), confirming negligible loading.

---

## 2. Post-Lab Theoretical Values

### Sinusoidal Response (`15 Vpp` = `7.50 Vpk`, `14.49 dBVrms`, `0°` phase)
| `f` | `ω` (rad/s) | `|H(jω)|` | `|H|` (dB) | `∠H(jω)` | `|Vo|` (`Vpk`) | `|Vo|` (`Vpp`) | `|Vo|` (`dBVrms`) |
|---|---:|---:|---:|---:|---:|---:|---:|
| `1 kHz` | `6,283.19` | `0.9956` | `−0.04` (`−0.0384`) | `−5.38°` | `7.47` | `14.93` | `14.45` |
| `10 kHz` | `62,831.85` | `0.7277` | `−2.76` (`−2.7606`) | `−43.30°` | `5.46` | `10.92` | `11.73` |
| `40 kHz` | `251,327.41` | `0.2564` | `−11.82` (`−11.8219`) | `−75.14°` | `1.92` | `3.85` | `2.67` |

### 8 kHz Periodic Square Wave (`±7.50 V`, `50%` duty cycle, `bn = 30/(nπ)` Vpk for odd `n`, `0` for even `n`)
> **Note on Peak vs. RMS dBV:** Keysight DSOX4024G Math FFT displays magnitudes in **dBVrms** (`20 log10(Vrms / 1 V) = 20 log10(Vpk) − 3.01 dB`). Both conventions yield the identical filter gain `G_dB = Out − In`.

| Harmonic | `f` (kHz) | `bn` (`Vpk`) | Input (`dBVpk` / `dBVrms`) | `|H(jnω0)|` (dB) | `∠H(jnω0)` | Output (`Vpk`) | Output (`dBVpk` / `dBVrms`) |
|---|---:|---:|---:|---:|---:|---:|---:|
| `n = 1` | `8.0` | `9.55` | `19.60 / 16.59` | `0.7985 (−1.95 dB)` | `−37.02°` | `7.62` | `17.64 / 14.63` |
| `n = 3` | `24.0` | `3.18` | `10.06 / 7.05` | `0.4043 (−7.87 dB)` | `−66.15°` | `1.29` | `2.19 / −0.82` |
| `n = 5` | `40.0` | `1.91` | `5.62 / 2.61` | `0.2564 (−11.82 dB)` | `−75.14°` | `0.49` | `−6.20 / −9.21` |

- **Exact Time-Domain Steady-State Capacitor Peak (`T0/2 = 62.5 µs = 4.17τ`):**
  `Vpeak,ss = ±7.5 × (1 − e^(−62.5/15)) / (1 + e^(−62.5/15)) = ±7.27 V` (`14.54 Vpp`).

---

## 3. Verified Experimental Results

### Part 1 — Sinusoidal Time Domain (Normalised by Measured `Vi,pp`)
| `f` | `Vi,pp` (V) | `Vo,pp` (V) | `|H|` Theory | `|H|` Measured (`Vo/Vi`) | Mag. Error | `∠H` Theory | `∠H` Measured |
|---|---:|---:|---:|---:|---:|---:|---:|
| `1 kHz` | `15.60` | `15.20` | `0.9956` | `0.9744` | `−2.13%` | `−5.38°` | `−6.55°` (`−6.65°` sheet) |
| `10 kHz` | `15.90` | `11.50` | `0.7277` | `0.7233` | `−0.61%` | `−43.30°` | `−42.30°` |
| `40 kHz` | `15.60` | `4.22` | `0.2564` | `0.2705` | `+5.51%` | `−75.14°` | `−73.71°` |

### Part 2 — Sinusoidal Frequency Domain (`dBVrms`)
| `f` | Output (`dBVrms`) | Input (`dBVrms`) | Measured Gain (dB) | Theoretical Gain (dB) | `|ΔG|` (dB) |
|---|---:|---:|---:|---:|---:|
| `1 kHz` | `14.61` | `14.83` | `−0.22` | `−0.04` | `0.18` |
| `10 kHz` | `12.18` | `14.99` | `−2.81` | `−2.76` | `0.05` |
| `40 kHz` | `3.47` | `14.83` | `−11.36` | `−11.82` | `0.46` |

### Part 3 — 8 kHz Square Wave Oscilloscope FFT Cursor Measurements (`dBVrms`)
Extracted directly from `10.17.29 AM (1)` – `10.17.33 AM (1)`:
| Harmonic | Scope `f` (In / Out) | Output `FFT(Ch2)` | Input `FFT(Ch1)` | Measured Gain (dB) | Theoretical Gain (dB) | `|ΔG|` (dB) |
|---|---|---:|---:|---:|---:|---:|
| `n = 1` | `8.0 / 8.0 kHz` | `14.53 dBV` | `16.56 dBV` | `−2.03` | `−1.95` | `0.08` |
| `n = 3` | `24.0 / 23.9 kHz` | `−0.63 dBV` | `7.19 dBV` | `−7.81` | `−7.87` | `0.06` |
| `n = 5` | `40.0 / 40.0 kHz` | `−9.06 dBV` | `2.66 dBV` | `−11.72` | `−11.82` | `0.10` |

---

## 4. Known Errors in Raw Student Worksheet Files (`result_sheets/`)
1. **`Lab 2 result sheet-1 (1) ss lab 2.pdf`:** Entered the phase angle `−73.71` in the `40 kHz` dB magnitude column instead of `−11.82 dB`.
2. **`Lab 2 result finalll.pdf` (Post-Lab C & Table C):**
   - Wrote `|H(j·2π·8000)| = 0.7854` (`π/4`) instead of the true RC gain `0.7985` (`−1.95 dB`), giving `7.50 V` (`17.50 dBVpk`) instead of `7.62 V` (`17.64 dBVpk`).
   - Copied the sinusoidal dBV numbers (`14.61/14.83`, `12.18/14.99`, `3.47/14.83` at `1, 10, 40 kHz`) into Table C instead of transcribing the actual `8, 24, 40 kHz` square-wave FFT cursor photos (`14.53/16.56`, `−0.63/7.19`, `−9.06/2.66 dBV`). All figures and tables in `Lab_Report2` use the authentic oscilloscope FFT cursor data.
