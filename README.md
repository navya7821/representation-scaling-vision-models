# Representation Scaling in Vision Models

This repository contains the code and experimental results for an empirical study on **representation scaling behavior in vision models**, focusing on how internal feature representations vary with model depth and dataset size under controlled conditions.


## Overview

While traditional scaling studies focus on task-level metrics such as accuracy or loss, this work investigates **representation-level behavior**, analyzing how feature spaces evolve across architectures.

The study is conducted under controlled settings using frozen backbones and a trained projection head to isolate representation dynamics.


## Methodology

### Architectures
- ResNet (18, 50, 101)
- DenseNet (121, 169, 201)
- Vision Transformers (ViT-Small, Base, Large)

### Experimental Axes
- Model size scaling (depth variation within architecture)
- Dataset size scaling (100, 200, 300 samples)

### Metrics
- ℓ2 norm of feature representations  
- Variance of activations  
- Effective rank (participation ratio)  


## Repository Contents

- `Ablation_Study.ipynb`  
  Experimental pipeline used to generate all results  

- `results/`  
  Contains CSV outputs for:
  - model size scaling  
  - dataset size scaling  


## Research Output

This work has been formalized into a research study and published as a preprint on Zenodo:

**Paper (Zenodo):** https://zenodo.org/records/19427823

The paper extends this repository by:
- consolidating experimental findings  
- analyzing scaling behavior across architectures  
- providing a structured interpretation of results  


## Reproducibility

This code was developed and executed in a Colab environment.  
Paths may need to be adjusted based on local directory structure before running.


## Notes

- All experiments use frozen pretrained backbones  
- Only projection layers are trained to isolate representation behavior  
- Results correspond directly to the published study  
