---
title: "Benefits of synchrony: Improving deep neural networks using complex values and Kuramoto synchronization"
collection: publications
category: neuro_conferences
permalink: /publication/komplexnet_ccn
excerpt: 'Preliminary version of KomplexNet presented at CCN.'
date: 2023-08-12
venue: 'Conference on Cognitive Computational Neuroscience (CCN)'
paperurl: 'https://2023.ccneuro.org/proceedings/0001044.pdf?s=W&pn=1131'
citation: '<strong>Muzellec, S.</strong>, Alamia, A., Serre, T., VanRullen, R. (2023). Benefits of synchrony: Improving deep neural networks using complex values and Kuramoto synchronization. Conference on Cognitive Computational Neuroscience (CCN).'
featured: false
---

Deep neural networks continue to improve at visual tasks but still fall short of human generalization. They also struggle to learn abstract concepts and to represent hierarchical relations between objects. The binding by synchrony theory describes how the brain processes visual scenes by synchronizing the activity of neurons that encode features from the same object. Here, we instantiate this theory in an artificial deep neural network through ”complex-valued” neurons. These neurons’ magnitude can be interpreted as the firing rate and their phase as a degree of synchrony with respect to other neurons in the population. We first initialize the phases by synchronizing them using an adaptation of the ”Kuramoto model” where a coupling kernel is learned to maximize the degree of synchrony/desynchrony between neurons encoding for the same/different objects. We then train a complex-valued neural network on a multi-object classification task, using the Kuramoto-synchronized state as phase initialization. We find that this model outperforms both its real-valued counterpart and a complex model initialized with random phases – exhibiting greater robustness to noise and to occlusions.

![KomplexNet](/images/komplexnet_ccn.png)

[Full paper link](https://2023.ccneuro.org/proceedings/0001044.pdf?s=W&pn=1131)


