# Lab photos and screenshots

Folder: `lab2_frequency_response/`

## Canvas screenshots (`canvas_screenshots/`, 4 files)
| File | Shows |
|------|-------|
| `WhatsApp Image 2026-10-25 at 10.17.22 AM (1).jpeg` | Lab 2 instructions page: links to the instruction sheet, result sheet, marking scheme, support slides, Tute Q6, and the red note that the cover sheet is mandatory. |
| `…10.17.22 AM.jpeg` | Assignment page: *Laboratory 2: Frequency Response of Systems*, 6 points, group, due Sun 25 Oct 2026 23:59. |
| `…10.17.23 AM (1).jpeg` | Submission box with the academic-integrity / AI-use declaration. |
| `…10.17.23 AM.jpeg` | Upload / Webcam / Canvas Files submission options. |

## Oscilloscope photos (`oscilloscope_photos/`, 22 files, 10.17.25 → 10.17.33)
Keysight InfiniiVision DSOX4024G (200 MHz, 5 GSa/s). Yellow trace = channel 1 (generator input),
green = channel 2 (capacitor output), white/purple = FFT (MATH1). Grouped by what is on screen
(grouping is by visual inspection; identical-looking photos are separate cursor readings):

| Group | Files (time stamp) | What they show |
|-------|--------------------|----------------|
| Sine, 1 kHz | `10.17.25 AM` | In/out sine waves; frequency ≈ 1.0001 kHz, phase ≈ 6.65°, Pk-Pk readings of 16.2 V in / 15.6 V out. Source of the 1 kHz row in Table A. |
| Sine, 10 kHz | `10.17.26 AM` | In/out sines ≈ 9.996 kHz, phase ≈ 42.9°, output Pk-Pk ≈ 11.5 V. |
| Square wave 8 kHz + FFT | `10.17.26 AM (1)`, `10.17.27 AM`, `10.17.27 AM (1)`, `10.17.27 AM (2)`, `10.17.28 AM`, `10.17.28 AM (1)`, `10.17.28 AM (2)` | Input square, RC-filtered output and the FFT trace together; automatic measurements (≈8 kHz, phase ≈ 28°) and cursors placed on the waveform. |
| FFT only (spectrum of output) | `10.17.29 AM (1)`, `10.17.29 AM (2)`, `10.17.29 AM`, `10.17.30 AM (1)`, `10.17.30 AM (2)`, `10.17.30 AM` | FFT magnitude peaks at the odd harmonics with cursors reading dBV (e.g. cursors at 8 kHz and 24 kHz). Source of Table C. |
| Sine, 40 kHz + FFT | `10.17.31 AM (1)`, `10.17.31 AM (2)`, `10.17.31 AM`, `10.17.32 AM (1)`, `10.17.32 AM` | Waveform with FFT, cursor X1 = 40 kHz, readings such as 14.53 dBV (input) and ≈ −2.6 to −9 dBV values. Source of Table B / 40 kHz row. |
| Final cursor readings | `10.17.33 AM (1)`, `10.17.33 AM` | Cursors at 8 kHz / 23.9 kHz with ≈ −2.5 dBV, ΔY ≈ 22.5 dB. |

These are raw evidence for the Results section; label and crop the useful ones as figures in the report.
