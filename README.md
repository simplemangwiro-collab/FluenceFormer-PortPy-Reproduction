# FluenceFormer — PortPy Two-Stage Reproduction

## COM6000 Capstone Project

Team:
- Geoff Mangwiro
- Simbarashe Mukanganwa
- Ngonidzashe Tsimba

Supervisor: Professor Ma

## Project objective

Reproduce the original two-stage FluenceFormer methodology
using the PortPy prostate dataset.

The original study dataset was inaccessible, and Professor Ma
recommended PortPy as the replacement dataset.

The approved research sequence is:

1. Faithfully reproduce the original FluenceFormer method.
2. Evaluate controlled Stage 2 dose-input perturbation.

Current status: Full reproduction in progress.

## Original references

FluenceFormer paper:
https://arxiv.org/pdf/2512.22425

Original implementation:
https://github.com/UJUNWAMGBOH/FluenceFormer

PortPy source:
https://github.com/PortPy-Project/PortPy

PortPy dataset:
https://huggingface.co/datasets/PortPy-Project/PortPy_Dataset

## Project files

- notebooks/: Original experimental code with saved outputs cleared
- results/stage1/: Training history, patient split, test results
- results/stage2/: Patient 1 fluence reconstruction evidence
- PROGRESS_LOG.md: Research milestones and outstanding work

## Stage 1 — Provisional experiment

A 2D SwinUNETR baseline was trained using data prepared
from ten PortPy prostate patients.

Selected results:

- Best validation MSE: 0.020064 at epoch 41
- Patient 2 test MSE: 0.017226
- Patient 9 test MSE: 0.017030

This experiment is provisional and is not yet a
verified faithful reproduction of the original paper.

## Stage 2 — Patient 1 validation

Using PortPy's influence-matrix workflow:

- Selected beamlets: 1965
- Fluence maps reconstructed: 9
- Exact matches with saved fluence maps: 9/9
- Maximum absolute difference: 0.0

This verifies spatial fluence reconstruction consistency.

It does not establish optimization provenance or
constitute complete Stage 2 neural-network reproduction.

## How colleagues can review the project

1. Read this README.
2. Read PROGRESS_LOG.md for the research history.
3. Open the notebook in Google Colab.
4. Review the Stage 1 and Stage 2 evidence files.
5. Consult the original paper before changing methodology.

## Reproducibility limitations

The notebook contains experimental research code,
not a fully automated reproduction pipeline.

It uses Colab-specific paths, intermediate diagnostics,
and external dependencies.

Large patient datasets and trained checkpoints are
stored separately and are not included in GitHub.

Do not assume every notebook cell can be executed
sequentially without additional setup.

## Remaining work

1. Audit the original paper and reference implementation.
2. Resolve methodology and dataset adaptations.
3. Establish reproducible PortPy optimization targets.
4. Prepare multi-patient Stage 2 training data.
5. Complete faithful two-stage reproduction.
6. Evaluate the approved Stage 2 improvement.

## Research progress

See PROGRESS_LOG.md for detailed progress.

## Important distinction

Completed provisional experiments and fluence reconstruction
validation are not equivalent to a complete reproduction
of the original FluenceFormer paper.
