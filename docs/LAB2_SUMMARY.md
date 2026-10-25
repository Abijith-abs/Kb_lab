# Lab 2 Summary — Square-Wave Section & Partner Alignment

Reference summary of the square-wave theoretical calculations, oscilloscope observations, and predicted Table C values incorporated into `lab2_frequency_response/report/Lab_Report2.docx` and `Lab_Report2.pdf` (aligned with `La.pdf` for the 2-member group split: Partner 1 = Sine-Wave Section; Partner 2 = Square-Wave Section).

---

## 1. RC Circuit & Transfer Function
- **Topology:** Series RC low-pass filter (`R = 1.5 kΩ`, `C = 0.01 µF = 10 nF`), output `vo(t) = vC(t)` across the capacitor.
- **Frequency Response:** `H(jω) = 1 / (1 + jωRC)`, time constant `τ = RC = 15 µs`, −3 dB cut-off `fc = 1 / (2πRC) = 10.61 kHz` (`|H| = 0.7071`, `−3.01 dB`, `∠H = −45.00°`).

---

## 2. Strict Separation of Theoretical, Predicted, and Measured Values

### A. Theoretical Calculations — Specified `15 Vpp` (`±7.50 V`), `8 kHz`, `50%` Duty-Cycle Square Wave (Post-Lab Section C)
Uses the **peak-amplitude `dBV` convention** (`LdBV = 20 log10(Vpeak / 1 V)`), matching `La.pdf`:
- Odd Fourier sine coefficients: `bn = 4A / (nπ) = 30 / (nπ)` V (`bn = 0` for even `n`).

| Harmonic | `f` (Hz) | `ω` (rad/s) | `|H(jω)|` | Gain (dB) | `∠H(jω)` | Input `bn` (V) | Input (dBV) | Output `|Vo,n|` (V) | Output (dBV) |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| `n = 1` | `8,000` | `50,265.48` | `0.7985` | `−1.95` | `−37.02°` | `9.55` | `19.60` | `7.63` | `17.65` |
| `n = 3` | `24,000` | `150,796.45` | `0.4041`* | `−7.87` | `−66.15°` | `3.18` | `10.06` | `1.29` | `2.19` |
| `n = 5` | `40,000` | `251,327.41` | `0.2564` | `−11.82` | `−75.14°` | `1.91` | `5.62` | `0.49` | `−6.19` |

*\*Exact `|H(j·2π·24000)| = 0.4043`; `La.pdf` rounded intermediate `ωRC` to `0.4041`, giving the identical `1.29 V` (`2.19 dBV`) output.*
- **Theoretical Steady-State Capacitor Excursion (`15 Vpp` input):** `±7.27 V` (`14.54 Vpp`).

### B. Actual Experimental Measurements — Keysight DSOX4024G Oscilloscope (`10.17.27 AM.jpeg` & FFT Captures)
- **Channel 1 Input (`Pk-Pk(1)`):** **`20.1 Vpp`** (flat plateau `Ampl(1) = 15.1 V` plus fast-edge switching overshoot and 50 Ω high-Z generator termination mismatch).
- **Channel 2 Output (`Pk-Pk(2)`):** **`14.9 Vpp`** (`Ampl(2) = 14.2 V`), smoothed exponential charging/discharging waveform.
- **Measured Frequency:** **`8.0000 kHz`** (CH1) / **`7.9949 kHz`** (CH2).
- **FFT Screenshot Limitation:** The saved FFT photos mainly capture `FFT(CH2)` (`10.17.32 AM (1)`–`10.17.33 AM (1)`) confirming odd-harmonic peaks at `X1 = 8.0, 23.9, 40.0 kHz`, while the manual horizontal cursor `Y1` remained uncoupled (e.g., parked at `−2.50 dBV`) rather than confirming paired input–output peak amplitudes.

### C. Predicted Harmonic Response — Scaled to Observed `20.1 Vpp` (`±10.05 V`) Input (Table C in `La.pdf`)
Explicitly presented as **predicted values** (`bn,pred = 40.2 / (nπ)` V, peak-amplitude `dBV` convention), **not** claimed as measured FFT readings:

| Harmonic | Frequency | Predicted Output (`20.1 Vpp`) | Predicted Input (`20.1 Vpp`) | Predicted Gain (`Out − In`) | Theoretical RC Gain (`15 Vpp`) |
|---|---|---:|---:|---:|---:|
| Fundamental (`n = 1`) | `8 kHz` | `20.19 dBV` (`10.22 V`) | `22.14 dBV` (`12.80 V`) | `−1.95 dB` | `−1.95 dB` (`−1.96 dB` in `La.pdf`) |
| Third (`n = 3`) | `24 kHz` | `4.72 dBV` (`1.72 V`) | `12.60 dBV` (`4.27 V`) | `−7.87 dB` | `−7.87 dB` |
| Fifth (`n = 5`) | `40 kHz` | `−3.65 dBV` (`0.66 V`) | `8.17 dBV` (`2.56 V`) | `−11.82 dB` | `−11.82 dB` |
