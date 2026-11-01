# FluenceFormer Capstone — Research Progress Log

## Project objective

Reproduce the original two-stage FluenceFormer methodology
using the PortPy prostate dataset, then investigate the
approved Stage 2 dose-input perturbation improvement.

The PortPy dataset was recommended by Professor Ma because
the dataset used in the original paper was inaccessible.

## Research methodology

Original FluenceFormer framework:

1. Stage 1: Predict dose from CT and anatomical information.
2. Stage 2: Predict beam fluence maps from predicted dose
   and beam-angle information.

The primary goal is faithful reproduction before
implementing improvements.

## Completed: Dataset investigation

- Investigated the official PortPy prostate dataset.
- Identified ten available patient cases.
- Inspected CT, structures, dose and beam information.
- Investigated beam geometry and beamlet indexing.
- Identified differences between the original paper's
  dataset and PortPy.

## Completed: Provisional Stage 1 experiment

- Prepared CT, dose and anatomical-mask inputs.
- Used ten PortPy patient cases.
- Prepared 397 image slices at 128 x 128 resolution.
- Implemented a 2D SwinUNETR-based provisional baseline.
- Used MSE loss and Adam optimization.
- Completed 50 training epochs.
- Recorded training and validation history.
- Evaluated on held-out patients.

Selected results:

- Best validation MSE: 0.020064 (epoch 41).
- Patient 2 test MSE: 0.017226.
- Patient 9 test MSE: 0.017030.

IMPORTANT:
This is a provisional PortPy adaptation and is NOT yet
a verified faithful reproduction of the original
FluenceFormer Stage 1 methodology.

## Completed: Stage 2 PortPy investigation

- Examined Patient 1 beam geometry.
- Identified nine treatment beams.
- Inspected beamlet dimensions and indexing.
- Investigated the official PortPy implementation.
- Constructed PortPy patient objects.
- Built a PortPy influence matrix using a PTV margin
  of 3 mm.
- Confirmed that the selected beamlet count is 1965,
  matching the saved Patient 1 intensity vector.

## Completed: Patient 1 fluence reconstruction validation

Used PortPy's official fluence_1d_to_2d method to
reconstruct fluence maps from the saved optimized
intensity vector.

Validation result:

- Nine fluence maps reconstructed.
- Nine out of nine maps matched saved maps exactly.
- Maximum absolute difference: 0.0.
- The saved intensity vector contains 1965 elements.

Evidence file:

Stage2_Fluence_Validation/
Patient_1_Fluence_Reconstruction_Validation.json

IMPORTANT:
This confirms spatial fluence reconstruction consistency.
It does not establish the optimization provenance or
constitute full FluenceFormer Stage 2 reproduction.

## Remaining work

1. Complete a methodology audit against the original paper.
2. Resolve paper-versus-implementation discrepancies.
3. Establish reproducible PortPy optimization targets.
4. Build and validate a multi-patient Stage 2 dataset.
5. Reproduce the original two-stage training and evaluation.
6. Evaluate the approved Stage 2 dose-input perturbation.
7. Report limitations and reproducibility evidence.

## Collaboration

Research notebook:
notebooks/FluenceFormer_PortPy_TwoStage_Reproduction.ipynb

The notebook contains experimental code and development
history. Saved outputs are excluded from the GitHub copy.

Large datasets and model checkpoints will be managed
separately in Google Drive.

## Reproducibility status

- Provisional Stage 1 baseline: Completed.
- Patient 1 fluence spatial validation: Completed.
- Faithful full two-stage reproduction: In progress.
- Proposed Stage 2 improvement: Not yet evaluated.
