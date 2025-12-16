---
title: "Latent Representation Matters: Human-like Sketches in One-shot Drawing Tasks"
collection: publications
category: ai_conferences
permalink: /publication/latents
excerpt: 'We systematically investigate how different inductive biases shape the latent space of Latent Diffusion Models (LDMs) in one-shot drawing tasks, comparing standard LDM regularizers with supervised and contrastive objectives. We find that redundancy-reduction and prototype-based regularizations enable LDMs to generate near-human-like drawings (highly recognizable and original), bringing machine one-shot generation remarkably close to human performance.'
date: 2024-12-16
venue: 'Advances in Neural Information Processing Systems (NeurIPS)'
paperurl: 'https://neurips.cc/virtual/2024/poster/93325'
citation: 'Boutin, V., Mukherji, R., Agrawal, A., <strong>Muzellec, S.</strong>, Fel, T., Serre, T., VanRullen, R. (2024). Latent Representation Matters: Human-like Sketches in One-shot Drawing Tasks. Advances in Neural Information Processing Systems (NeurIPS) 37, 96282-96324'
featured: false
---

Humans can effortlessly draw new categories from a single exemplar, a feat that has long posed a challenge for generative models. However, this gap has started to close with recent advances in diffusion models. This one-shot drawing task requires powerful inductive biases that have not been systematically investigated. Here, we study how different inductive biases shape the latent space of Latent Diffusion Models (LDMs). Along with standard LDM regularizers (KL and vector quantization), we explore supervised regularizations (including classification and prototype-based representation) and contrastive inductive biases (using SimCLR and redundancy reduction objectives). We demonstrate that LDMs with redundancy reduction and prototype-based regularizations produce near-human-like drawings (regarding both samples' recognizability and originality) -- better mimicking human perception (as evaluated psychophysically). Overall, our results suggest that the gap between humans and machines in one-shot drawings is almost closed.

![Latent diffusion models](/images/latent_dif.png)



