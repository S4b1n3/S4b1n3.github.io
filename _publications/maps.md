---
title: "MAPS: Masked Attribution-based Probing of Strategies — A computational framework to align human and model explanations"
collection: publications
category: preprints
permalink: /publication/maps
excerpt: "MAPS is a validated tool that identifies which ANN explanations best match human vision. By converting attribution maps into explanation-masked images (EMIs), it links model explanations with human and macaque behavior and enables principled comparison of interpretability methods using far fewer trials."
date: 2025-10-14
venue: "Under revision at Communications Psychology"
paperurl: "https://arxiv.org/pdf/2510.12141"
codeurl: "https://github.com/vital-kolab/maps"
dataurl: "https://osf.io/t6kw8/overview?view_only=c9d2b96a8c7f43bda3acefc07fc25bc8"
citation: "<strong>Muzellec, S.</strong>, Alghetaa, Y. K., Kornblith, S., & Kar, K. (2025). MAPS: Masked Attribution-based Probing of Strategies — A computational framework to align human and model explanations. arXiv preprint arXiv:2510.12141"
featured: true
header:
    teaser: "maps.jpeg"
---

Human core object recognition depends on the selective use of visual information, but the strategies guiding these choices are difficult to measure directly. We present MAPS (Masked Attribution-based Probing of Strategies), a behaviorally validated computational tool that tests whether explanations derived from artificial neural networks (ANNs) can also explain human vision. MAPS converts attribution maps into explanation-masked images (EMIs) and compares image-by-image human accuracies on these minimal images with limited pixel budgets with accuracies on the full stimuli. MAPS provides a principled way to evaluate and choose among competing ANN interpretability methods. In silico, EMI-based behavioral similarity between models reliably recovers the ground-truth similarity computed from their attribution maps, establishing which explanation methods best capture the model's strategy. When applied to humans and macaques, MAPS identifies ANN-explanation combinations whose explanations align most closely with biological vision, achieving the behavioral validity of Bubble masks while requiring far fewer behavioral trials. Because it needs only access to model attributions and a modest set of behavioral data on the original images, MAPS avoids exhaustive psychophysics while offering a scalable tool for adjudicating explanations and linking human behavior, neural activity, and model decisions under a common standard.

![MAPS](/images/maps_paper.png)

