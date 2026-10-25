# Oscilloscope Photos Catalog (`lab2_frequency_response/oscilloscope_photos/`)

All 22 photographs (`2048 × 1536` JPEG, named `WhatsApp Image 2026-10-25 at 10.17.XX AM*.jpeg`) capture a **Keysight InfiniiVision DSOX4024G** digital storage oscilloscope testing the series RC low-pass filter (`R = 1.5 kΩ`, `C = 0.01 µF`, `fc = 10.61 kHz`):
- **Channel 1 (Yellow):** Input voltage `vi(t)` directly from the Agilent 33220A function generator.
- **Channel 2 (Green):** Capacitor output voltage `vo(t) = vC(t)`.
- **Math 1 (White/Purple):** Built-in hardware FFT (`Span = 50.0 kHz`, `Center = 25.0 kHz`, `Scale = 5.00 dB/div`, `Offset = 0.0 dBV`, `Bin Size = 954 Hz`, vertical units in **dBVrms**).

---

## Complete Verified Photo Map (22 Captures)

### 1. Part 1 — Sinusoidal Time-Domain Captures (4 Photos)

| Filename (`WhatsApp Image 2026-10-25 at …`) | Test Signal | Scale Settings | On-Screen Automated Measurements | Report Usage |
|---|---|---|---|---|
| `10.17.25 AM.jpeg` | **1 kHz Sine** | Ch1: `5.00 V/div`, Ch2: `5.00 V/div`, Time: `500.0 µs/div` | `Freq(1) = 1.0001 kHz`, `Pk-Pk(1) = 15.6 V`, `Ampl(1) = 15.6 V`, `Pk-Pk(2) = 15.2 V`, `Ampl(2) = 15.2 V`, `Phase(1→2) = 6.55°` (`−6.55°` lag) | **Figure 6(a)** |
| `10.17.25 AM (1).jpeg` | **1 kHz Sine** (duplicate angle) | Same as above | Same readings (`Pk-Pk(1) = 15.6 V`, `Pk-Pk(2) = 15.2 V`, `Phase(1→2) = 6.55°`) | Duplicate backup |
| `10.17.26 AM.jpeg` | **10 kHz Sine** | Ch1: `5.00 V/div`, Ch2: `5.00 V/div`, Time: `20.00 µs/div` | `Freq(1) = 9.9962 kHz`, `Pk-Pk(1) = 15.9 V`, `Ampl(1) = 15.9 V`, `Pk-Pk(2) = 11.5 V`, `Ampl(2) = 11.5 V`, `Phase(1→2) = 42.30°` (`−42.30°` lag) | **Figure 6(b)** |
| `10.17.26 AM (1).jpeg` | **10 kHz Sine** (duplicate angle) | Same as above | Same readings (`Pk-Pk(1) = 15.9 V`, `Pk-Pk(2) = 11.5 V`, `Phase(1→2) = 42.30°`) | Duplicate backup |

> **Note on 40 kHz Sinusoid:** No separate photograph was saved for the 40 kHz sinusoidal capture; its measured values (`Vi,pp = 15.6 V`, `Vo,pp = 4.22 V`, `Phase = −73.71°`) were recorded directly in `Lab 2 result finalll.pdf`.

---

### 2. Part 3 — 8 kHz Square Wave Time-Domain + FFT Setup (6 Photos)

| Filename (`WhatsApp Image 2026-10-25 at …`) | Display Mode | Key Readings & Notes | Report Usage |
|---|---|---|---|
| `10.17.27 AM.jpeg` | **8 kHz Square** Time + `FFT(Ch1)` | Ch1: `10.0 V/div`, Ch2: `5.00 V/div`, `50.00 µs/div`. `Freq(1) = 8.0000 kHz`, `Ampl(1) = 15.1 V` (true plateau), `Pk-Pk(1) = 20.1 V` (edge ringing), `Pk-Pk(2) = 14.9 V`, `Ampl(2) = 14.2 V`, `Phase(1→2) = 28.25°` | **Figure 9** |
| `10.17.27 AM (1).jpeg` | `FFT(Ch1)` menu setup | Initial FFT display before manual cursor placement (`X1 = 0.0 Hz`) | Setup frame |
| `10.17.28 AM.jpeg` | `FFT(Ch1)` cursor setup | Manual cursor selected on Math 1 (`X1 = 0.0 Hz`) | Setup frame |
| `10.17.28 AM (1).jpeg` | `FFT(Ch1)` cursor setup | Duplicate of cursor setup (`X1 = 0.0 Hz`) | Setup frame |
| `10.17.28 AM (2).jpeg` | `FFT(Ch1)` off-peak | Cursor at `X1 = 7.9 kHz`, `Y1 = 15.0 dBV` (adjacent bin before centring on 8.0 kHz peak) | Setup frame |
| `10.17.29 AM.jpeg` | `FFT(Ch1)` off-peak | Duplicate of `X1 = 7.9 kHz`, `Y1 = 15.0 dBV` | Setup frame |

---

### 3. Part 3 — 8 kHz Square Wave Input Spectrum `FFT(Ch1)` Harmonic Peaks (6 Photos)

| Filename (`WhatsApp Image 2026-10-25 at …`) | Harmonic | Cursor `X1` (Frequency) | Cursor `Y1(M1)` (Magnitude) | Theory (`15 Vpp`, dBVrms) | Report Usage |
|---|---|---|---|---|---|
| `10.17.29 AM (1).jpeg` | **Fundamental (`n = 1`)** | `8.0 kHz` | **`16.5625 dBV`** (`16.56 dBV`) | `16.59 dBV` | **Figure 10(a)** |
| `10.17.29 AM (2).jpeg` | Fundamental (`n = 1`, dup.) | `8.0 kHz` | `16.5625 dBV` | `16.59 dBV` | Duplicate backup |
| `10.17.30 AM.jpeg` | **3rd Harmonic (`n = 3`)** | `24.0 kHz` | **`7.1875 dBV`** (`7.19 dBV`) | `7.05 dBV` | Duplicate backup |
| `10.17.30 AM (1).jpeg` | 3rd Harmonic (`n = 3`, clearer) | `24.0 kHz` | **`7.1875 dBV`** (`7.19 dBV`) | `7.05 dBV` | **Figure 10(b)** |
| `10.17.30 AM (2).jpeg` | **5th Harmonic (`n = 5`)** | `40.0 kHz` | **`2.65625 dBV`** (`2.66 dBV`) | `2.61 dBV` | Duplicate backup |
| `10.17.31 AM.jpeg` | 5th Harmonic (`n = 5`, clearer) | `40.0 kHz` | **`2.65625 dBV`** (`2.66 dBV`) | `2.61 dBV` | **Figure 10(c)** |

---

### 4. Part 3 — 8 kHz Square Wave Output Spectrum `FFT(Ch2)` Harmonic Peaks (6 Photos)

| Filename (`WhatsApp Image 2026-10-25 at …`) | Harmonic | Cursor `X1` (Frequency) | Cursor `Y1(M1)` (Magnitude) | Theory (`15 Vpp`, dBVrms) | Measured Gain (`Out − In`) | Report Usage |
|---|---|---|---|---|---|---|
| `10.17.31 AM (1).jpeg` | **Fundamental (`n = 1`)** | `8.0 kHz` | **`14.5313 dBV`** (`14.53 dBV`) | `14.63 dBV` | **`−2.03 dB`** (th: `−1.95 dB`) | **Figure 10(d)** |
| `10.17.32 AM.jpeg` | Fundamental (`n = 1`, dup.) | `8.0 kHz` | `14.5313 dBV` | `14.63 dBV` | `−2.03 dB` | Duplicate backup |
| `10.17.32 AM (1).jpeg` | **3rd Harmonic (`n = 3`)** | `23.9 kHz`* | **`−625.00 mdBV`** (`−0.63 dBV`) | `−0.82 dBV` | **`−7.81 dB`** (th: `−7.87 dB`) | **Figure 10(e)** |
| `10.17.32 AM (2).jpeg` | 3rd Harmonic (`n = 3`, dup.) | `23.9 kHz`* | `−625.00 mdBV` (`−0.63 dBV`) | `−0.82 dBV` | `−7.81 dB` | Duplicate backup |
| `10.17.33 AM.jpeg` | **5th Harmonic (`n = 5`)** | `40.0 kHz` | **`−9.0625 dBV`** (`−9.06 dBV`) | `−9.21 dBV` | **`−11.72 dB`** (th: `−11.82 dB`) | **Figure 10(f)** |
| `10.17.33 AM (1).jpeg` | 5th Harmonic (`n = 5`, dup.) | `40.0 kHz` | `−9.0625 dBV` | `−9.21 dBV` | `−11.72 dB` | Duplicate backup |

*\*At a 50.0 kHz span (`954 Hz` FFT bin spacing), `23.9 kHz` is the closest discrete FFT bin to `24.0 kHz`.*
