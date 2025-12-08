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

<h3 style="margin-top:1.8rem; margin-bottom:0.4rem;
           font-size:1.1rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  Reverse Predictivity
</h3>

<p style="margin-top:1.0rem; margin-bottom:0.4rem;
          font-weight:600;
          font-size:0.95rem;
          text-transform:uppercase;
          letter-spacing:0.08em;">
  🔹 1. Reverse Predictivity (analysis repo)
</p>

**Purpose:** fully reproduces the analyses from the paper (model comparisons, time-resolved predictivity, neuron-level regression, reliability estimation, etc.).

- **Code:** <https://github.com/vital-kolab/reverse_pred>  
- **Data (OSF):** <https://osf.io/y3qmk/>  
- **Archive / DOI:** 10.5281/zenodo.17704686  
- **Paper:** Muzellec & Kar (2025)  
- **Includes:**
  - Regression pipelines  
  - Reliability & noise-ceiling estimation  
  - ANN → Monkey, Monkey → ANN, Monkey → Monkey, and Model → Model comparisons  
  - Full reproducibility scripts for figures and benchmarks  

This repo is designed to **replicate the publication** and provide a transparent scientific workflow.

<p style="margin-top:1.2rem; margin-bottom:0.4rem;
          font-weight:600;
          font-size:0.95rem;
          text-transform:uppercase;
          letter-spacing:0.08em;">
  🔹 2. <code>reverse-pred</code> (PyPI Python library)
</p>

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

<h3 style="margin-top:2.0rem; margin-bottom:0.4rem;
           font-size:1.1rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  MAPS — Masked Attribution-based Probing of Strategies
</h3>

**Purpose:** MAPS is a computational framework for testing whether **visual explanations** from deep neural networks capture **human-like and primate-like visual strategies**.  
It combines attribution methods, explanation-driven perturbations, and behavioral evaluation to compare **models ↔ humans ↔ monkeys**.

- **Code:** <https://github.com/vital-kolab/maps>  
  *(Currently private; will be public soon.)*  
- **Data (OSF):** <https://osf.io/t6kw8/>  
- **Paper:** Muzellec, Alghetaa, Kornblith & Kar (2025)  
- **Includes**:
  - Fine-tuning pipelines for object-recognition models  
  - Attribution map generation using Captum (e.g., Saliency, NoiseTunnel, Integrated Gradients)  
  - **Explanation-Masked Inputs (EMIs)**: images masked based on attribution maps  
  - Behavioral metrics (**B.I1**) to compare model strategies to humans, monkeys, and neurons  
  - Similarity analyses (L1, L2, LPIPS)  
  - Full reproducibility scripts for MAPS paper figures  

---

## Brain-inspired neural networks

<h3 style="margin-top:1.8rem; margin-bottom:0.4rem;
           font-size:1.1rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  KomplexNet – Complex-valued networks with Kuramoto synchrony
</h3>

**Purpose:**  PyTorch(-Lightning) framework for **complex-valued neural networks** with **Kuramoto-style phase synchronization**, designed to test the benefits of binding-by-synchrony in deep networks (generalization to overlap, noise and more or less objects).

- **Code:** <https://github.com/S4b1n3/KomplexNet>  
- **Paper:** Muzellec, Alamia, Serre & VanRullen (TMLR, 2025)  
- **Includes:** 
  - A modular implementation of **complex-valued convolutions** with phase-based recurrence  
  - A differentiable **Kuramoto synchrony module** that enforces phase alignment among units  
  - Training pipelines for the MultiMNIST benchmark  
  - Tools to analyze **phase dynamics**, **synchrony strength**, and their effect on recognition accuracy  
  - Baseline comparisons against real-valued CNNs and ablated synchrony models  
  - Complete scripts to reproduce all experiments and figures from the paper  

---

## Datasets & Benchmarks

<h3 style="margin-top:1.8rem; margin-bottom:0.4rem;
           font-size:1.1rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  FeatureTracker – Tracking objects that change in appearance with phase synchrony
</h3>

**Purpose:**  Synthetic video benchmark where objects change **shape**, **color**, and **position** over time, designed to probe **object tracking under appearance changes** and phase-based grouping mechanisms.

- **Code:** <https://github.com/S4b1n3/feature_tracker>  
- **Paper:** Muzellec*, Linsley*, Ashok, Mingolla, Malik, VanRullen & Serre (ICLR, 2024)  
- **Includes:**
  - Stimulus generation scripts (`utils_shapes.py`, `utils_colors.py`, `generate_data.py`)  
  - Training scripts for CV-RNN and related models on FeatureTracker  
  - Testing scripts on the different variations of FeatureTracker  

---

## How to cite

If you use any of this code or datasets in your work, please cite the corresponding paper(s) when available.  
If something looks useful but isn’t yet public, feel free to **email me** to discuss early access or collaboration.
