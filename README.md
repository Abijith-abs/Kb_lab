# ENS3553 / ENS6160.4 — Signals and Systems (ECU) — Lab Workspace

Organized coursework, experimental oscilloscope captures, and the **Square-Wave Section & Lab Report (`Lab_Report2.docx` / `Lab_Report2.pdf`)** for **Laboratory 2: Frequency Response of Systems** (`ENS3553` / `ENS6160.4`, Semester 2, 2026, Edith Cowan University).

---

## Repository Structure

```
Kb_lab/
├── README.md                              ← Overview & group workflow guide
├── La.pdf                                 ← Partner's calculation worksheet (Post-Lab C & Table C)
├── signals lab 2 report copy.docx         ← Sample layout reference file
├── docs/                                  ← Verified technical & administrative notes
│   ├── FILE_CATALOG.md                    ← Guide to every file in the repository
│   ├── ASSESSMENT_REQUIREMENTS.md         ← Rubric weights, Canvas rules & cover-sheet policy
│   ├── COURSE_NOTES.md                    ← Summary of Module 5 & 6 slides + Tutorial 5 Q6
│   ├── LAB1_SUMMARY.md                    ← Reference notes on Lab 1 (Spectral Analysis)
│   ├── LAB2_SUMMARY.md                    ← Verified square-wave theory, Table C predictions & measurements
│   └── OSCILLOSCOPE_PHOTOS.md             ← Verified catalog of all 22 Keysight DSOX4024G captures
│
├── course_material/
│   ├── lectures/
│   │   ├── Signal and system Module 5 slides.pdf
│   │   └── Signals and Systems Module 6 slides.pdf
│   └── tutorials/
│       └── Tute 5 Q6.pdf
│
├── lab1_spectral_analysis/
│   └── signals and system lab 1 kbb.docx  ← Completed Lab 1 report (formatting/style reference)
│
├── lab2_frequency_response/
│   ├── instructions/
│   │   └── Lab 2 instruction sheet-3.pdf  ← Official Lab 2 brief
│   ├── result_sheets/
│   │   ├── Lab 2 result sheet-1.pdf               ← Blank template
│   │   ├── Lab 2 result sheet-1 (1) ss lab 2.pdf  ← Partially filled worksheet
│   │   └── Lab 2 result finalll.pdf               ← Earlier worksheet
│   ├── canvas_screenshots/                ← 4 screenshots of the Canvas assignment page
│   ├── oscilloscope_photos/               ← 22 Keysight DSOX4024G time & FFT photos
│   └── report/                            ← Square-wave lab report deliverables (2-person split)
│       ├── Lab_Report2.docx               ← Editable Word (.docx) — Square-Wave Lab Report & Sections
│       ├── Lab_Report2.pdf                ← Matching 15-page PDF (with fillable Page 1 ECU cover sheet)
│       └── figures/                       ← 7 publication-grade 300-DPI square-wave figures (fig01–fig07)
│
└── assessment_admin/
    ├── Labs Marking Scheme-1.pdf          ← Official marking rubric
    └── Groupwork coversheet v23 08 2024_Fillable (4).pdf
```

---

## Final Deliverables (`lab2_frequency_response/report/`)

Structured for the **2-member group split** (Partner 1: Sine-Wave Section; Partner 2: Square-Wave Section):

- **`Lab_Report2.docx`** — Full editable Microsoft Word report containing **only the Square-Wave investigation and shared RC circuit foundation**, ready either to review standalone or combine directly with the partner's Sine-Wave sections:
  - **Theoretical Calculations (`15 Vpp` manual specification):** Keeps the instructed `15 Vpp` (`±7.50 V`, `8 kHz`, `50%` duty cycle) for Post-Lab Section C(a)–(c), yielding odd Fourier coefficients `9.55, 3.18, 1.91 V` (`19.60, 10.06, 5.62 dBV`) and filtered outputs `7.63, 1.29, 0.49 V` (`17.65, 2.19, −6.19 dBV`) under the peak-amplitude `dBV` convention.
  - **Actual Oscilloscope Measurements (`20.1 Vpp` input, `14.9 Vpp` output):** Documents the observed Channel 1 (`20.1 Vpp`) and smoothed Channel 2 (`14.9 Vpp`) waveforms at `8.00 kHz`, embeds the actual Keysight DSOX4024G screenshots (`Figures 5 & 6`), and discusses why `20.1 Vpp` exceeded the instructed `15 Vpp`.
  - **Predicted Table C Values (`20.1 Vpp` basis — explicitly not claimed as measured):** Presents the partner's exact Table C predictions (`22.14, 12.60, 8.17 dBV` input; `20.19, 4.72, −3.65 dBV` output; `−1.95, −7.87, −11.82 dB` gain) and explains why reliable paired experimental FFT peak amplitudes could not be extracted from the saved screenshots.
- **`Lab_Report2.pdf`** *(15 pages)* — Matching PDF counterpart with the official **ECU Groupwork Cover Sheet** embedded as Page 1 (unit details pre-filled and student AcroForm fields preserved as interactive fillable fields), **Abstract** (`313 words`), populated **Table of Contents**, **Conclusion** (`202 words`), **APA 7th References**, and **Acknowledgement of AI Use**.
