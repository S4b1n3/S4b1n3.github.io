---
title: "Enhancing deep neural networks through complex-valued representations and Kuramoto synchronization dynamics"
collection: publications
category: manuscripts
permalink: /publication/komplexnet
excerpt: 'We investigate whether neural-inspired synchrony can improve object binding in deep learning models, testing whether complex-valued representations and Kuramoto dynamics can align phases and group features belonging to the same object. Across multi-object and noisy visual categorization tasks, including overlapping digits and out-of-distribution inputs, both feedforward and recurrent synchrony-based models outperform real-valued and unsynchronized complex networks, demonstrating that phase-based mechanisms can substantially enhance performance, robustness, and generalization.'
date: 2025-02-28
venue: 'Transactions on Machine Learning Research (TMLR)'
paperurl: 'https://arxiv.org/pdf/2502.21077?'
citation: '<strong>Muzellec, S.</strong>, Alamia, A., Serre, T., VanRullen, R. (2025). Enhancing deep neural networks through complex-valued representations and Kuramoto synchronization dynamics. Transactions on Machine Learning Research (TMLR).'
featured: true
header:
    teaser: "komplexnet.png"
---

Neural synchrony is hypothesized to play a crucial role in how the brain organizes visual scenes into structured representations, enabling the robust encoding of multiple objects within a scene. However, current deep learning models often struggle with object binding, limiting their ability to represent multiple objects effectively. Inspired by neuroscience, we investigate whether synchrony-based mechanisms can enhance object encoding in artificial models trained for visual categorization. Specifically, we combine complex-valued representations with Kuramoto dynamics to promote phase alignment, facilitating the grouping of features belonging to the same object. We evaluate two architectures employing synchrony: a feedforward model and a recurrent model with feedback connections to refine phase synchronization using top-down information. Both models outperform a real-valued baseline and complex-valued models without Kuramoto synchronization on tasks involving multi-object images, such as overlapping handwritten digits, noisy inputs, and out-of-distribution transformations. Our findings highlight the potential of synchrony-driven mechanisms to enhance deep learning models, improving their performance, robustness, and generalization in complex visual categorization tasks.

![KomplexNet](/images/komplexnet_tmlr.png)

