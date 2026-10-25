# Lab 1 — Spectral Analysis of Periodic Signals

**File:** `lab1_spectral_analysis/signals and system lab 1 kbb.docx`
**Author:** Anandhu Kaithavalappil Binod (ID 10730544), ENS6160, Edith Cowan University.
(The date on the title page reads "04 October 20026" — a typo for 2026.)

## Aim
Compare the frequency spectra of sinusoidal, square and triangular periodic signals using Fourier-series
analysis and oscilloscope FFT measurements.

## Structure (a complete report)
Aim & objectives → Introduction → Methodology → Results & analysis (A sine, B square, C triangle) →
Conclusion → References (2 papers). Includes 9 figures and 3 theoretical-vs-measured tables.

## Content
| Signal | Setup | Theory | Measured |
|--------|-------|--------|----------|
| **Sine** | 1 MHz, 2 Vpp | Single component, b₁ = 1 V at 1 MHz | 1 MHz, −2.5 dBV ≈ 0.75 V |
| **Square** | 1 MHz, h = 1 V | b_n = 4h/(nπ), n odd: 1.273, 0.424, 0.255, 0.182 V at 1/3/5/7 MHz; even harmonics = 0 | 1.413, 0.439, 0.256, 0.189 V at 1.00/2.98/4.98/6.98 MHz |
| **Triangle** | 200 kHz, A = 1 V | b_n = (8A/n²π²)·sin(nπ/2): 0.8106, −0.0901, 0.0324, −0.0165 V at 200/600/1000/1400 kHz | peaks near 200/596/998/1400 kHz |

**Conclusion of the report:** theory and FFT measurements agree; differences in magnitude are attributed to
practical measurement conditions and FFT limitations.

## Notes
- The Figure 7 caption says "1 MHz triangular wave" while the body uses 200 kHz.
- The sine-wave comparison attributes the 1 V vs 0.75 V gap to "practical conditions"; a 2 Vpp generator
  output into the scope may also be a factor worth discussing.
- Lab 2's post-lab Part C re-uses the square-wave Fourier formula from this lab.
- This report is a useful **model** for the Lab 2 report layout.
