
# SADAN-ADHD

Official implementation of the paper:

**State-Aware Dynamic Spatiotemporal Modeling for Interpretable EEG-Based ADHD Classification and Brain Network Characterization**

This repository provides the implementation of the proposed **State-Aware Dynamic Attention Network (SADAN)** for EEG-based ADHD classification and interpretable brain-network characterization.

## Overview

SADAN is designed to model non-stationary EEG dynamics by integrating:

- Latent neural state decoding inspired by the Gaussian Linear Hidden Markov Model (GLHMM)
- Multi-scale temporal representation learning
- State-driven cross-domain attention
- State-aware spatiotemporal feature modeling

For neurophysiological interpretation, the framework further incorporates the **State-Guided Spatiotemporal Reconstruction-Based Feature (SG-SRBF)** method to analyze:

- Dynamic channel importance
- Cross-state stability
- State-dependent brain-network reconfiguration

## Dataset

### Public EEG dataset

The public ADHD EEG dataset used in this study is available through IEEE DataPort.

The dataset contains EEG recordings from children with ADHD and healthy controls.

Due to data redistribution restrictions, the original EEG data are not included in this repository.

### In-house dataset

The independent in-house EEG dataset was collected at Xi'an Hospital of Traditional Chinese Medicine.

Due to privacy and ethical restrictions, this dataset is not publicly available. Access may be considered upon reasonable request, subject to institutional approval and a signed data access agreement.

## Experimental Protocol

The public dataset was evaluated using **subject-independent five-fold cross-validation**.

Subjects, rather than EEG segments, were divided into five mutually exclusive folds. All EEG segments belonging to the same subject were kept within the same fold to avoid subject-level data leakage.

The independent in-house dataset was used for cross-dataset validation.

## Performance

On the public IEEE ADHD EEG dataset:

- Mean accuracy: **92.43% ± 2.26%**
- Best-performing fold accuracy: **95.66%**
- Best-performing fold AUC: **0.9921**

On the independent in-house dataset:

- Accuracy: **94.27%**
- AUC: **0.9894**

## Requirements

The main dependencies include:

- Python
- PyTorch
- NumPy
- SciPy
- scikit-learn
- MNE-Python
- pandas
- matplotlib

Install dependencies using:

```bash
pip install -r requirements.txt
