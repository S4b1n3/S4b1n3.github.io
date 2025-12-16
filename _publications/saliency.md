---
title: "Saliency strikes back: How filtering out high frequencies improves white-box explanations"
collection: publications
category: ai_conferences
permalink: /publication/saliency
excerpt: 'We identify a major limitation of gradient-based white-box attribution methods (their susceptibility to high-frequency artifacts) and introduce FORGrad, a simple filtering approach that removes these distortions using architecture-specific optimal cut-off frequencies. Across models, FORGrad reliably boosts the performance of existing white-box methods, allowing them to rival more accurate but computationally expensive black-box approaches and enabling more faithful and efficient explainability.'
date: 2023-07-18
venue: 'International Conference on Machine Learning (ICML)'
paperurl: 'https://arxiv.org/pdf/2307.09591'
citation: '<strong>Muzellec, S.</strong>, Fel, T., Boutin, V., Andeol, L., VanRullen, R., Serre, T. (2023). Saliency strikes back: How filtering out high frequencies improves white-box explanations. International Conference on Machine Learning (ICML).'
featured: false
---

Attribution methods correspond to a class of explainability methods (XAI) that aim to assess how individual inputs contribute to a model’s decision-making process. We have identified a significant limitation in one type of attribution methods, known as “white-box" methods. Although highly efficient, as we will show, these methods rely on a gradient signal that is often contaminated by high-frequency artifacts. To overcome this limitation, we introduce a new approach called "FORGrad". This simple method effectively filters out these high-frequency artifacts using optimal cut-off frequencies tailored to the unique characteristics of each model architecture. Our findings show that FORGrad consistently enhances the performance of already existing white-box methods, enabling them to compete effectively with more accurate yet computationally demanding "black-box" methods. We anticipate that our research will foster broader adoption of simpler and more efficient white-box methods for explainability, offering a better balance between faithfulness and computational efficiency.

![Saliency](/images/saliency.png)
