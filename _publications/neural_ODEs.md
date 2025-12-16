---
title: "Accurate implementation of computational neuroscience models through neural ODEs"
collection: publications
category: neuro_conferences
permalink: /publication/neural_ODEs
excerpt: "Master's internship on the use of neural ODEs to accurately implement computational neuroscience models, leading to better performance and computational effiency."
date: 2022-08-15
venue: 'Conference on Cognitive Computational Neuroscience (CCN) as a <strong>Talk</strong>'
paperurl: 'https://2022.ccneuro.org/proceedings/0000090.pdf'
citation: '<strong>Muzellec, S.</strong>, Chalvidal, M., Serre, T., VanRullen, R. (2022). Accurate implementation of computational neuroscience models through neural ODEs. Conference on Cognitive Computational Neuroscience (CCN).'
featured: false
---

Computational neuroscience models are usually defined by differential equations representing their dynamics. One recently popular solution to implement such models on a large-scale has been to use deep learning tools and associated optimization methods. However, to train models with these approaches, the differential equations need to be discretized and sometimes adapted, which can affect their performance and decrease their dynamical precision. Here, we show that neural Ordinary Differential Equations (neural ODEs), a framework recently introduced in the machine learning community to allow end-to-end training of ODEs, is more suitable for large-scale implementation of computational neuroscience models. Neural ODEs are compatible with a large choice of strategies to solve the differential equations. For instance, the prevailing deep learning approach essentially amounts to using a solver based on Euler discretization, combined with back-propagation training; but more precise solvers and training approaches can be employed. We compare the performance of different neural ODE implementations of two computational neuroscience models on vision tasks : (i) the original (Rao-Ballard) predictive coding model characterizing cortico-cortical feedback in the visual system, and (ii) hGRU (horizontal Gating Recurrent Unit), a model of classical and extra-classical receptive fields of the visual cortex. In both cases, our results show that the standard deep learning method is sub-optimal, and that neural ODEs with higher-order adaptive solvers can help improve the performance and stability of the models.

![Neural ODEs](/images/neural_ode.png)

