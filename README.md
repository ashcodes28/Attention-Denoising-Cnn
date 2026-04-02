# Attention-Enhanced Denoising CNN

## Overview
This project integrates a Denoising Autoencoder (DAE) with a CNN classifier to improve robustness under noisy image conditions.

## Features
- Denoising Autoencoder for preprocessing
- Attention mechanism for feature focus
- Ablation study (Baseline vs Hybrid)

## Dataset
- CIFAR-10 with synthetic noise (Gaussian + Salt & Pepper)

## Results
| Model | Accuracy |
|------|--------|
| Baseline | 55.9% |
| Hybrid | 48.5% |
| Hybrid + Attention | 50.9% |

## Run
```bash
pip install -r requirements.txt
python model.py
