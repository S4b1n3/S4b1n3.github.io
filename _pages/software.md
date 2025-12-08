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
           font-size:1.15rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  Reverse Predictivity
</h3>

<p style="margin-top:1.0rem; margin-bottom:0.4rem;
          font-weight:600;
          font-size:0.95rem;">
  🔹 1. Reverse Predictivity (analysis repo)
</p>

**Purpose:** fully reproduces the analyses from the paper (model comparisons, time-resolved predictivity, neuron-level regression, reliability estimation, etc.).

- **Code:** <https://github.com/vital-kolab/reverse_pred>  
- **Data (OSF):** <https://osf.io/y3qmk/>  
- **Archive / DOI:** 10.5281/zenodo.17704686  
- **Paper:** Muzellec & Kar (2025)

**Includes:**
<div style="font-size:0.90rem; margin-left:1rem;">
<ul>
  <li>Regression pipelines</li>
  <li>Reliability & noise-ceiling estimation</li>
  <li>ANN → Monkey, Monkey → ANN, Monkey → Monkey, and Model → Model comparisons</li>
  <li>Full reproducibility scripts for figures and benchmarks</li>
</ul>
</div>

This repo is designed to **replicate the publication** and provide a transparent scientific workflow.

<p style="margin-top:1.2rem; margin-bottom:0.4rem;
          font-weight:600;
          font-size:0.95rem;">
  🔹 2. <code>reverse-pred</code> (PyPI Python library)
</p>

A lightweight, general-purpose Python package that exposes the core mapping utilities independent of the paper’s full analysis pipeline.

- **Package:** <https://pypi.org/project/reverse-pred/>  
- **Install:**  
  ```bash
  pip install reverse-pred
  ```

**Features:**
<div style="font-size:0.90rem; margin-left:1rem;">
<ul>
  <li>Unified API for the four mapping modes</li>
  <li>Fit/evaluate linear models (ridge by default; PLS & others supported)</li>
  <li>Clean, modular functions for ANN feature extraction → mapping → evaluation</li>
  <li>Integrates easily into any model–brain alignment project</li>
</ul>
</div>

**Example usage**
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
    reps=20,
)
```

---

## Brain-inspired neural networks

<h3 style="margin-top:1.8rem; margin-bottom:0.4rem;
           font-size:1.15rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  MAPS — Masked Attribution-based Probing of Strategies
</h3>

**Purpose:** MAPS is a computational framework for testing whether **visual explanations** from deep neural networks capture **human-like and primate-like visual strategies**.

It combines attribution methods, explanation-driven perturbations, and behavioral evaluation to compare **models ↔ humans ↔ monkeys**.

- **Code:** <https://github.com/vital-kolab/maps> *(private, public soon)*  
- **Data (OSF):** <https://osf.io/t6kw8/>  
- **Paper:** Muzellec, Alghetaa, Kornblith & Kar (2025)

**Includes:**
<div style="font-size:0.90rem; margin-left:1rem;">
<ul>
  <li>Fine-tuning pipelines for object-recognition models</li>
  <li>Attribution generation using Captum (Saliency, NoiseTunnel, IG, etc.)</li>
  <li><b>Explanation-Masked Inputs (EMIs)</b> based on attribution maps</li>
  <li>Behavioral metrics (B.I1) comparing models, humans, and monkeys</li>
  <li>Similarity analyses (L1, L2, LPIPS)</li>
  <li>Full reproducibility scripts for MAPS paper figures</li>
</ul>
</div>

---

<h3 style="margin-top:1.8rem; margin-bottom:0.4rem;
           font-size:1.15rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  KomplexNet – Complex-valued networks with Kuramoto synchrony
</h3>

**Purpose:** PyTorch(-Lightning) framework for **complex-valued neural networks** with **Kuramoto-style phase synchronization**, designed to test the benefits of binding-by-synchrony in deep networks.

- **Code:** <https://github.com/S4b1n3/KomplexNet>  
- **Paper:** Muzellec, Alamia, Serre & VanRullen (TMLR, 2025)

**Includes:**
<div style="font-size:0.90rem; margin-left:1rem;">
<ul>
  <li>Complex-valued convolutions with phase-based recurrence</li>
  <li>Differentiable <b>Kuramoto synchrony module</b></li>
  <li>Training pipelines for MultiMNIST</li>
  <li>Tools to analyze phase dynamics, synchrony strength, and recognition accuracy</li>
  <li>Comparisons with real-valued CNNs and ablated models</li>
  <li>Full experiment + figure reproduction scripts</li>
</ul>
</div>

---

## Datasets & Benchmarks

<h3 style="margin-top:1.8rem; margin-bottom:0.4rem;
           font-size:1.15rem;
           font-weight:700;
           border-bottom:1px solid currentColor;
           padding-bottom:0.25rem;">
  FeatureTracker – Tracking objects that change in appearance
</h3>

**Purpose:** Synthetic video benchmark where objects change **shape**, **color**, and **position** over time, designed to probe **object tracking under appearance changes** and phase-based grouping mechanisms.

- **Code:** <https://github.com/S4b1n3/feature_tracker>  
- **Paper:** Muzellec*, Linsley*, Ashok, Mingolla, Malik, VanRullen & Serre (ICLR, 2024)

**Includes:**
<div style="font-size:0.90rem; margin-left:1rem;">
<ul>
  <li>Stimulus generation scripts (shapes, colors, dynamics)</li>
  <li>Training scripts for CV-RNN and related models</li>
  <li>Testing scripts for all FeatureTracker variations</li>
</ul>
</div>

---

## How to cite

If you use any of this code or datasets in your work, please cite the corresponding paper(s).  
If something looks useful but isn’t yet public, feel free to **email me** for early access or collaboration.
