# File catalog

Every file in the repository, grouped by folder. (36 MB total, 37 files before this
documentation was added.)

## `course_material/lectures/`
| File | What it is |
|------|-----------|
| `Signal and system Module 5 slides.pdf` | 31-slide lecture deck "ENS3553 Module 5 post-class slides". Frequency response of LTI systems to everlasting exponentials / sinusoids, frequency spectrum and bandwidth, trigonometric and exponential **Fourier series**, convergence (Gibbs), and computing a system's response to a periodic input using its frequency response. |
| `Signals and Systems Module 6 slides.pdf` | 34-slide deck. Extends Fourier series to the **Fourier transform** (aperiodic signals), transform pairs, properties (linearity, duality, scaling, shifting, time convolution), frequency response as H(jω), distortionless transmission, ideal vs. realisable filters, windowing/spectral leakage, energy and bandwidth. Includes the sample MATLAB used for plotting frequency responses (Lab 2 post-lab part A(c)). |

## `course_material/tutorials/`
| File | What it is |
|------|-----------|
| `Tute 5 Q6.pdf` | 2 pages: tutorial question (page 1) and worked solution (page 2). Shows that an LTI system's response to e^{st} is H(s)e^{st}, then derives H(s) for a system described by a first-order differential equation (a RC-type low-pass). This is the method the Lab 2 post-lab asks you to use. |

## `lab1_spectral_analysis/`
| File | What it is |
|------|-----------|
| `signals and system lab 1 kbb.docx` | Finished **Lab Report 1 – Spectral Analysis of Periodic Signals** (ENS6160) by Anandhu Kaithavalappil Binod, ID 10730544. Covers 1 MHz sine, 1 MHz square and 200 kHz triangular waves: Fourier coefficients vs. oscilloscope FFT. See `LAB1_SUMMARY.md`. |

## `lab2_frequency_response/instructions/`
| File | What it is |
|------|-----------|
| `Lab 2 instruction sheet-3.pdf` | 4-page official brief: "Laboratory Experiment 2 – Frequency Response of Systems". Objectives, post-lab exercises A–C, equipment, and the 3-part lab procedure. |

## `lab2_frequency_response/result_sheets/`
All three are the same 2019-v0.9 template ("Lab 2 result sheet"); they differ in how complete they are.
| File | Pages | What it is |
|------|-------|-----------|
| `Lab 2 result sheet-1.pdf` | 8 | The **blank** template as downloaded from Canvas. |
| `Lab 2 result sheet-1 (1) ss lab 2.pdf` | 9 | **Partly filled** copy: post-lab frequency response table (the 40 kHz dB cell still says −73.71, which is a mistake — see `LAB2_SUMMARY.md`). |
| `Lab 2 result finalll.pdf` | 10 | **Most complete** version: post-lab tables, square-wave Fourier coefficients and harmonic gains, plus measured values for Tables A, B and C. Student name/number fields are still blank. |

## `lab2_frequency_response/canvas_screenshots/`
Four screenshots of the Canvas (LMS) page for **ENS6160.4 → Assignments → Laboratory 2**:
the instruction/resources page (links to the lab sheets, slides, Tute Q6 and the mandatory cover sheet),
the assignment details (6 points, group, due Sun 25 Oct 2026 23:59), and the submission area with the
academic-integrity/AI-use declaration. Files: `…10.17.22 AM (1)`, `…10.17.22 AM`, `…10.17.23 AM (1)`, `…10.17.23 AM`.

## `lab2_frequency_response/oscilloscope_photos/`
22 phone photos (named `WhatsApp Image 2026-10-25 at 10.17.25 AM.jpeg` … `10.17.33 AM (1).jpeg`) of a
Keysight InfiniiVision DSOX4024G oscilloscope screen showing the RC-circuit measurements. See
`OSCILLOSCOPE_PHOTOS.md`.

## `lab2_frequency_response/report/`
| File | What it is |
|------|-----------|
| `Lab_Report2.docx` | **Editable Word report (Square-Wave Section & Lab Report)**: contains only the Square-Wave investigation and shared RC circuit foundation for the 2-member group split (Partner 1: Sine Wave; Partner 2: Square Wave), strictly separating `15 Vpp` theoretical Fourier results, `20.1 Vpp` Table C predicted harmonic levels, and `20.1 Vpp / 14.9 Vpp` oscilloscope observations. |
| `Lab_Report2.pdf` | **Matching 15-page PDF counterpart** with the official ECU Groupwork Cover Sheet embedded as Page 1 (unit details pre-filled and all student AcroForm fields preserved as editable/clickable fields). |
| `figures/fig01_circuit_schematic.png` … `fig07_predicted_20v1_comparison.png` | 7 publication-grade 300-DPI square-wave figures (circuit schematic, Bode plot at 8/24/40 kHz, 15 Vpp theoretical spectra & waveforms, oscilloscope waveform & FFT(CH2) captures, and 20.1 Vpp Table C comparison). |

## Root Reference Files Added by Partner / User
| File | What it is |
|------|-----------|
| `La.pdf` | Partner's calculation worksheet containing Post-Lab Section C (`15 Vpp` Fourier & harmonic tables) and Result Sheet Table C (`20.1 Vpp` predicted harmonic values). |
| `signals lab 2 report copy.docx` | Sample past-report formatting/structure reference file. |

## `assessment_admin/`
| File | What it is |
|------|-----------|
| `Labs Marking Scheme-1.pdf` | 3-page marking rubric for the lab report (weights per section, HD/D/C/P/F descriptors). |
| `Groupwork coversheet v23 08 2024_Fillable (4).pdf` | ECU School of Engineering group-work declaration (relative contributions & accountability). **Mandatory** for submission; the form is currently unfilled. |

## `docs/`
These explanatory notes (added later).
