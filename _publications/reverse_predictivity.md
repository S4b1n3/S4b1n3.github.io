---
title: "Reverse Predictivity: Going Beyond One-Way Mapping to Compare Artificial Neural Network Models and Brains"
collection: publications
category: preprints
permalink: /publication/reverse_predictivity
excerpt: 'We introduce reverse predictivity, a new metric that complements traditional forward predictivity by testing bidirectional alignment (how well ANN representations can be predicted by macaque IT activity). While monkey-to-monkey and same-architecture ANN initializations show symmetry, ANNs exhibit a striking asymmetry with IT, and we identify factors (such as adversarial training) that reduce these non-IT-aligned representational dimensions and improve ANN–brain alignment. See the associated talk <a href="/talks/reverse_pred_vss" target="_blank" rel="noopener">here</a>.'
date: 2025-08-11
venue: 'Under Revision at Nature Machine Intelligence'
paperurl: 'https://www.biorxiv.org/content/biorxiv/early/2025/08/11/2025.08.08.669382.full.pdf'
codeurl: "https://github.com/vital-kolab/reverse_pred"
dataurl: "https://osf.io/y3qmk/overview"
citation: '<strong>Muzellec, S.</strong> & Kar, K. (2025). Reverse Predictivity: Going Beyond One-Way Mapping to Compare Artificial Neural Network Models and Brains. bioRxiv, 2025.08. 08.669382'
featured: true
header:
    teaser: "reverse_pred.png"
---

A major goal in systems neuroscience is to build computational models that capture the
primate brain’s internal representations. Standard evaluations of artificial neural networks
(ANNs) emphasize forward predictivity—how well model features predict neural responses—
without testing whether model representations are themselves predictable from
neural activity. Here we develop the reverse predictivity metric, which quantifies how well
macaque inferior temporal (IT) cortex responses predict ANN unit activations. This two-way
framework reveals a striking asymmetry: models with high forward predictivity (~50% variance
explained) often contain units unpredictable from neural activity, reflecting biologically
inaccessible dimensions. In contrast, monkey-to-monkey mappings are symmetric, confirming
that the asymmetry reflects genuine representational mismatch. Reverse predictivity isolates
“common” ANN units—shared with IT, behaviorally relevant, and generalizing across
species—and “unique” units lacking such alignment. Influenced by feature dimensionality,
training objectives, and adversarial robustness, reverse predictivity offers a principled
benchmark for guiding next-generation ANNs toward both high task performance and genuine
biological plausibility.

![Reverse Predictivity](/images/reverse_pred_paper.png)
