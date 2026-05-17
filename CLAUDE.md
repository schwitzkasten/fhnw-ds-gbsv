# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an FHNW (Fachhochschule Nordwestschweiz) data science course project — **GBSV (Grundlagen der Bild- und Signalverarbeitung / Fundamentals of Image and Signal Processing)**. It contains Jupyter notebooks organized around two mini-challenges (MC1, MC2), each spanning 15 days in a structured 5-day cycle.

## Environment Setup

The project uses Python virtual environments (`.venv`, `.venv-1`). Activate before running notebooks:

```bash
# Activate venv
source .venv/Scripts/activate  # Windows bash
# or
.venv\Scripts\activate.bat     # Windows cmd
```

Launch Jupyter:
```bash
jupyter notebook
# or
jupyter lab
```

Core libraries: `numpy`, `pandas`, `matplotlib`, `scipy.signal`, `PIL`

## Repository Structure

- **`Challenges MC1/`** — Mini-challenge 1: Sampling Theorem, applied to BVP (blood volume pulse) signals from the WESAD dataset
- **`Challenges MC2/`** — Mini-challenge 2: Convolution, Correlation, Segmentation, Pattern Detection, applied to alpine ibex imagery
- **`WESAD/S2/`** — Signal data: `S2_BVP.csv` (64 Hz BVP), `S2_respiban.txt` (respiration)
- **`Challenges MC2/Data/Steinbock.jpg`** — Alpine ibex photograph used for image processing tasks
- **`General/`** — Template notebook and rubric interpretations

## Submission Structure

Each mini-challenge follows a **5-day cycle repeated 3 times** (Days 1–15):

| Day in cycle | Competency |
|---|---|
| 1, 6, 11 | Data & Domain |
| 2, 7, 12 | Methodological Design |
| 3, 8, 13 | Technical Implementation |
| 4, 9, 14 | Evaluation |
| 5, 10, 15 | Analysis & Communication |

Individual day notebooks (e.g., `Day2.ipynb`, `day-11-lg.ipynb`) are consolidated into submission notebooks (e.g., `gbsv-mc1.1.ipynb`, `gbsv-mc2.2-clean.ipynb`).

## Assessment Rubric

Five competencies evaluated per submission (see `General/rubric_gbsv_interpretations.txt` and `Challenges MC2/Documents/gbsv-rubric-mc2.xlsx`):

1. **Data & Domain** — WESAD dataset characteristics, Swiss Alpine Rescue / National Park use case justification
2. **Methodological Design** — Nyquist analysis, filter selection, convolution/correlation design rationale
3. **Technical Implementation** — Working Python/scipy code, signal processing pipeline
4. **Evaluation** — Metric extraction (IBI, systolic slope, respiratory modulation depth), quantitative comparison
5. **Analytical & Communication** — Interpretation, regional relevance, Swiss-specific context

## Domain Context

- **MC1 signals:** WESAD BVP at 64 Hz; decimation experiments at 8/12/16/24/32 Hz; key metrics: inter-beat interval (IBI), systolic slope, respiratory modulation depth
- **MC2 images:** Alpine ibex (`Steinbock.jpg`); tasks include ROI extraction, augmentation (rotation, lighting variation), fur/rock/sky boundary segmentation for wildlife detection robustness
- All use cases anchor to Switzerland (Alpine Rescue telemetry, Swiss National Park conservation)
