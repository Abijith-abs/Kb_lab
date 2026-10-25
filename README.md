# Kb_lab — Signals and Systems lab workspace

A personal study/assignment repository for **ENS3553 / ENS6160 Signals and Systems**
(School of Engineering, Edith Cowan University). It holds everything needed for the
**laboratory assessments**: lecture slides, the lab instruction and result sheets,
a finished Lab 1 report, photos taken in the lab, screenshots of the Canvas
assignment page, and the marking/cover-sheet paperwork.

## The big picture

| Lab | Topic | What this repo contains |
|-----|-------|-------------------------|
| **Lab 1** | Spectral analysis of periodic signals (sine, square, triangle; Fourier series vs. oscilloscope FFT) | A completed report (`.docx`) |
| **Lab 2** | Frequency response of an RC low-pass filter (R = 1.5 kΩ, C = 0.01 µF) | Instruction sheet, three versions of the result sheet, 22 oscilloscope photos, 4 Canvas screenshots |

Lab 2 (6% of the unit grade, group work, due **Sun 25 Oct 2026, 23:59** on Canvas) is the
assignment currently being prepared. The work is: do the post-lab theory, build the
RC circuit, measure it with a function generator and oscilloscope, then write an
IMRaD-style report using the marking scheme and the mandatory group cover sheet.

## Folder structure

```
Kb_lab/
├── README.md                      ← you are here
├── docs/                          ← explanatory notes (start here)
│   ├── FILE_CATALOG.md            ← what every single file is
│   ├── LAB1_SUMMARY.md            ← Lab 1 report explained
│   ├── LAB2_SUMMARY.md            ← Lab 2 theory, data and results explained
│   ├── COURSE_NOTES.md            ← Module 5 / Module 6 slides + tutorial summary
│   ├── OSCILLOSCOPE_PHOTOS.md     ← the 22 lab photos, grouped
│   └── ASSESSMENT_REQUIREMENTS.md ← report structure, marking scheme, cover sheet
├── course_material/
│   ├── lectures/                  ← Module 5 and Module 6 slide PDFs
│   └── tutorials/                 ← Tute 5 Q6
├── lab1_spectral_analysis/        ← Lab 1 report (.docx)
├── lab2_frequency_response/
│   ├── instructions/              ← Lab 2 instruction sheet
│   ├── result_sheets/             ← blank, partly filled and final result sheets
│   ├── canvas_screenshots/        ← screenshots of the Canvas assignment page
│   └── oscilloscope_photos/       ← phone photos of the oscilloscope screen
└── assessment_admin/              ← marking scheme + group-work cover sheet
```

## Suggested reading order

1. `docs/FILE_CATALOG.md` — quick inventory.
2. `docs/LAB2_SUMMARY.md` — the live assignment.
3. `docs/ASSESSMENT_REQUIREMENTS.md` — what the report must contain.
4. `docs/COURSE_NOTES.md` — the theory behind it.

> Note: the repository's original files were reorganised into the folders above; nothing
> was renamed or edited, only moved (original filenames, including the WhatsApp image
> names, are unchanged).
