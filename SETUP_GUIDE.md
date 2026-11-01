# FluenceFormer — Team Setup Guide

## 1. Project purpose

This repository preserves the team's experimental
FluenceFormer reproduction work using PortPy.

The full faithful two-stage reproduction is in progress.

## 2. Open the research notebook

Open the file in the notebooks directory using
Google Colab.

The notebook contains historical experiments,
debugging steps and intermediate investigations.

It is not yet an end-to-end execution pipeline.

Do not run all cells sequentially without reviewing
their dependencies and required input files.

## 3. Configure Google Drive

In Colab, mount your own Google Drive.

The research notebook currently contains paths
originally used by the project author.

Those paths must be adapted to your own Drive
organization before rerunning experiments.

Do not modify the archived research notebook merely
to change paths.

## 4. Software dependencies

See requirements.txt for a snapshot of the software
versions observed in the current Colab environment.

These versions have not yet been verified as the exact
environment used for all earlier experiments.

PyTorch and CUDA versions must be compatible with
the selected runtime.

PortPy is also required for the official influence
matrix and fluence reconstruction workflows.

Official PortPy source:
https://github.com/PortPy-Project/PortPy

## 5. Dataset

Official PortPy dataset:
https://huggingface.co/datasets/PortPy-Project/PortPy_Dataset

The original FluenceFormer paper used a different
dataset that was unavailable to the team.

Professor Ma recommended PortPy as the replacement.

Large datasets are not included in the GitHub package.

The team must arrange access to the shared Google
Drive data or retrieve permitted files from the
official dataset source.

Do not redistribute patient data without checking
the dataset's applicable terms.

## 6. Experimental results

Stage 1 evidence:
results/stage1/

Stage 2 evidence:
results/stage2/

Research progress:
PROGRESS_LOG.md

These files support review of recorded experiments,
but do not replace full experimental reproduction.

## 7. Model checkpoints

Trained checkpoints are stored separately in the
Google Drive research project.

They are not included in the GitHub package.

The team will document their shared Drive locations
before attempting checkpoint-based evaluation.

## 8. Reproducibility status

Provisional Stage 1 baseline: Completed.

Patient 1 fluence reconstruction validation: Completed.

Faithful full two-stage reproduction: In progress.

Controlled Stage 2 dose-input perturbation:
Not yet evaluated.

## 9. Collaboration

Before modifying the research method, compare the
proposed changes with the original FluenceFormer paper.

Document any deviations required by PortPy or
hardware constraints.

Keep experimental improvements separate from the
faithful reproduction baseline.
