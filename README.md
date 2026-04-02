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

## Analysis

The baseline model achieves the highest accuracy as it directly learns from input images without reconstruction loss.  
The hybrid model introduces a denoising autoencoder, which slightly reduces classification accuracy due to imperfect reconstruction.  

However, adding attention improves performance by helping the model focus on important regions, demonstrating its effectiveness in recovering useful features from noisy inputs.

## Key Insight

This experiment highlights a trade-off between denoising and feature preservation.  
While denoising improves robustness to noise, it can degrade classification performance.  
Attention mechanisms help mitigate this issue by preserving important features.

## Visualization

- Reconstruction results (Original vs Noisy vs Denoised)
- Accuracy comparison graph (Ablation study)

All visual outputs are included in the notebook.

## Future Work

- Use advanced attention mechanisms (CBAM / Transformers)
- Improve reconstruction quality using deeper autoencoders
  
## Run

```bash
pip install -r requirements.txt
jupyter notebook

