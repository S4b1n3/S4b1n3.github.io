---
layout: archive
title: "Software & Code"
permalink: /software/
author_profile: true
---

{% include base_path %}

Here is a selection of software, code, and datasets that I maintain or contribute to.
Most of it sits at the intersection of **computational neuroscience**, **deep learning**, and **vision**.

---

## Computational Neuroscience Toolbox

### Reverse Predictivity

#### 🔹 1. Reverse Predictivity (analysis repo)
**Purpose:** fully reproduces the analyses from the paper (model comparisons, time-resolved predictivity, neuron-level regression, reliability estimation, etc.).

- **Code:** <https://github.com/vital-kolab/reverse_pred>  
- **Data (OSF):** <https://osf.io/y3qmk/>  
- **Archive / DOI:** 10.5281/zenodo.17704686  
- **Paper:** Muzellec & Kar (2025).
- **Includes:**
  - Regression pipelines  
  - Reliability & noise-ceiling estimation  
  - Model-to-Monkey, Monkey-to-Model and Monkey-to-Monkey comparisons  
  - Full reproducibility scripts for figures and benchmarks

This repo is designed to **replicate the publication** and provide a transparent scientific workflow.

#### 🔹 2. `reverse-pred` (PyPI Python library)
A lightweight, general-purpose Python package that exposes the core mapping utilities independent of the paper’s full analysis pipeline.

- **Package:** <https://pypi.org/project/reverse-pred/>  
- **Install:**  
  ```bash
  pip install reverse-pred
  ```

- **Features:**
    - Unified API for the four mapping modes
    - Fit/evaluate linear models (ridge by default; PLS & others supported)
    - Clean, modular functions for ANN feature extraction → mapping → evaluation
    - Can be integrated into any model–brain alignment project

- **Example usage**
    ```python
    import numpy as np
    from reverse_predictivity.monkey_to_model import compute_monkey_to_model

    # Model features: one row per image, one column per ANN unit
    model_features = np.load("features/resnet50_itlayer.npy")   # shape: (n_images, n_units)

    # Neural data: images × neurons × repeats
    rates = np.load("data/it_rates.npy")                        # shape: (n_images, n_neurons, n_repeats)

    compute_monkey_to_model(
        model_features=model_features,
        rates=rates,
        out_dir="results/monkey_to_model/resnet50",
        reps=20,   # number of cross-validated fits
    )
    ```

### MAPS — Masked Attribution-based Probing of Strategies

**Purpose:** MAPS is a computational framework for testing whether **visual explanations** from deep neural networks capture **human-like and primate-like visual strategies**.  
It combines attribution methods, explanation-driven perturbations, and behavioral evaluation to compare **models ↔ humans ↔ monkeys**.

- **Code:** <https://github.com/vital-kolab/maps>  
  *(Currently private; will be public soon.)*  
- **Data (OSF):** <https://osf.io/t6kw8/>  
- **Paper:** Muzellec, Alghetaa, Kornblith & Kar (2025)
- **Includes**:
    - Fine-tuning pipelines for object-recognition models  
    - Attribution map generation using Captum (e.g., Saliency, NoiseTunnel, Integrated Gradients)  
    - **Explanation-Masked Inputs (EMIs)**: images maksed based on attribution maps
    - Behavioral metrics (**B.I1**) to compare model strategies to humans, monkeys, and neurons  
    - Similarity analyses (L1, L2, LPIPS)  
    - Full reproducibility scripts for MAPS paper figures

---

## Brain-inspired neural networks

### KomplexNet – Complex-valued networks with Kuramoto synchrony

**Purpose:**  PyTorch(-Lightning) framework for **complex-valued neural networks** with **Kuramoto-style phase synchronization**, designed to test the benefits of binding-by-synchrony in deep networks (generalization to overlap, noise and more or less objects).

- **Code:** <https://github.com/S4b1n3/KomplexNet>  
- **Paper:** Muzellec, Alamia, Serre & VanRullen (TMLR, 2025)  
- **Includes:** 
    - A modular implementation of **complex-valued convolutions** and with phase-based recurrence
    - A differentiable **Kuramoto synchrony module** that enforces phase alignment among units  
    - Training pipelines for MultiMNIST benchmark
    - Tools to analyze **phase dynamics**, **synchrony strength**, and their effect on recognition accuracy  
    - Baseline comparisons against real-valued CNNs and ablated synchrony models  
    - Complete scripts to reproduce all experiments and figures from the paper

---

## Datasets & Benchmarks

### FeatureTracker – Tracking objects that change in appearance with phase synchrony

**Purpose:**  Synthetic video benchmark where objects change **shape**, **color**, and **position** over time, designed to probe **object tracking under appearance changes** and phase-based grouping mechanisms. :contentReference[oaicite:0]{index=0}  

- **Code** <https://github.com/S4b1n3/feature_tracker>  
- **Paper:** Muzellec*, Linsley*, Ashok, Mingolla, Malik, VanRullen & Serre (ICLR, 2024)  
- **Includes:**
  - Stimulus generation scripts (`utils_shapes.py`, `utils_colors.py`, `generate_data.py`)
  - Training scripts for CV-RNN and related models on FeatureTracker
  - Testing scripts on the different variations of FeatureTracker

---



<!-- ### Memorability & feature manipulation pipelines

Utilities for:
- Computing and analyzing **image memorability** scores (MemNet/AMNet/VitMem)
- Generating and evaluating **feature-accentuated** image variants
- Selecting stimulus sets for behavioral experiments (AMT, lab-based)

**Status:** under active development; some parts will be merged into a public repository. -->

## How to cite

If you use any of this code or datasets in your work, please cite the corresponding paper(s) when available.  
If something looks useful but isn’t yet public, feel free to **email me** to discuss early access or collaboration.
