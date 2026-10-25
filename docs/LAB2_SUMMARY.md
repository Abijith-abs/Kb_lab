# Lab 2 — Frequency Response of Systems

## Goal
Derive the frequency response H(jω) of a first-order **RC low-pass filter**, predict what it does to a
sine wave and to a square wave, then **measure** it with a function generator and a Keysight DSO-X
oscilloscope and compare theory with measurement (time domain and FFT/frequency domain).

## The circuit
Series R–C, input = source voltage Vi, output = capacitor voltage Vo.
**R = 1.5 kΩ, C = 0.01 µF** → RC = 15 µs.

LCCDE: RC·dVo/dt + Vo = Vi. Setting the input to e^{jωt} (method of Tute 5 Q6) gives

> **H(jω) = 1 / (1 + jωRC)**, |H| = 1/√(1+(ωRC)²), ∠H = −arctan(ωRC)

Cut-off (−3 dB, |H| = 0.707) at **f_c = 1/(2πRC) ≈ 10.6 kHz**. It is a **low-pass** filter.

## Post-lab (theory) — values checked against the formula
| f | ω (rad/s) | \|H\| | \|H\| dB | ∠H |
|---|-----------|------|---------|-----|
| 1 kHz | 6283.19 | 0.9956 | −0.038 | −5.38° |
| 10 kHz | 62831.85 | 0.7277 | −2.76 | −43.30° |
| 40 kHz | 251327.41 | 0.2564 | −11.82 | −75.14° |

**Part B** — 15 Vpk-pk sine in (7.5 V peak): output peaks ≈ 7.47 V / 5.46 V / 1.92 V
(i.e. 14.93 / 10.92 / 3.85 Vpk-pk) at 1 / 10 / 40 kHz, with the phases above.

**Part C** — 15 Vpk-pk, 8 kHz, 50% square wave: b_n = 4h/(nπ) for odd n with h = 7.5 V →
b₁ = 9.55 V (8 kHz), b₃ = 3.18 V (24 kHz), b₅ = 1.91 V (40 kHz). Filter gain at those harmonics
0.7985 / 0.4041 / 0.2564 → output harmonics 7.63 V / 1.29 V / 0.49 V.
Expected output: a rounded, "charging/discharging" waveform (higher harmonics attenuated).

## Measured data (from `Lab 2 result finalll.pdf`)
**Table A — time domain (sine, 15 Vpk-pk in)**
| f | Mag. theory | Mag. measured | Phase theory | Phase measured |
|---|------|------|------|------|
| 1 kHz | 14.93 | 15.20 | −5.39° | −6.65° |
| 10 kHz | 10.92 | 11.50 | −43.30° | −42.30° |
| 40 kHz | 3.85 | 4.22 | −75.14° | −73.71° |

**Table B — FFT of sine input/output**
| f | Output | Input | Gain measured | Gain theory |
|---|---|---|---|---|
| 1 kHz | 14.61 dBV | 14.83 dBV | −0.23 dB | −0.0384 dB |
| 10 kHz | 12.18 dBV | 14.99 dBV | −2.81 dB | −2.7606 dB |
| 40 kHz | 3.47 dBV | 14.83 dBV | −11.35 dB | −11.821 dB |

**Table C — 8 kHz square wave, harmonic gains**
| Harmonic | Output | Input | Gain measured | Gain theory |
|---|---|---|---|---|
| Fundamental (8 kHz) | 20.19 dBV | 22.14 dBV | −1.95 dB | −1.96 dB |
| 3rd (24 kHz) | 4.72 dBV | 12.60 dBV | −7.87 dB | −7.87 dB |
| 5th (40 kHz) | −3.65 dBV | 8.17 dBV | −11.82 dB | −11.82 dB |

Measured and theoretical values agree closely; the output falls with frequency, confirming low-pass behaviour.

## How the three result-sheet versions differ
1. `Lab 2 result sheet-1.pdf` — blank template.
2. `… (1) ss lab 2.pdf` — post-lab filled in (including the screenshots of the plots).
3. `Lab 2 result finalll.pdf` — adds Part B/C theory and Tables A–C.
Still empty in all versions: student name/number, the written answers (filter type, −3 dB meaning, cut-off,
behaviour in time/frequency domain), sketches and the discussion section.

## Things to fix before submitting (observed while reviewing)
- The 40 kHz dB value is shown as **−73.71** in the earlier sheet (and the final sheet's first post-lab table);
  the correct value is **−11.82 dB** (20·log₁₀ 0.2564). The final sheet's second table has it right.
- In the square-wave table the harmonic frequencies are written "3rd = 2000 Hz" and "5th = 4000 Hz";
  they should be **24 000 Hz** and **40 000 Hz** (3×8 kHz, 5×8 kHz).
- The Table A phase measured at 40 kHz (−73.71°) is the same number as the mistaken dB value — double-check
  against the scope photo.
- The 40 kHz sine *magnitude* in the theory table is 0.2564 in one place and 0.2568 in another.
- Sketches, written answers, name/ID and the group cover sheet are still outstanding; a full IMRaD report
  is required (see `ASSESSMENT_REQUIREMENTS.md`).
