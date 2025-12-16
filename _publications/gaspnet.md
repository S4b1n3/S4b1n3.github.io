---
title: "GASPnet: Global Agreement to Synchronize Phases"
collection: publications
category: preprints
permalink: /publication/gaspnet
excerpt: 'We introduce a new, neuroscience-inspired binding mechanism that integrates Transformer-style attention with phase-based synchrony, enabling neural networks to selectively enhance interactions between neurons with aligned temporal phases while suppressing mismatched signals. By incorporating Kuramoto-driven phase alignment into all layers of a convolutional network, our model achieves higher accuracy, stronger noise robustness, and better generalization than standard CNNs on multi-object datasets, offering a principled solution to the visual binding problem in artificial networks.'
date: 2025-07-22
venue: 'Under Revision at Neurocomputing'
paperurl: 'https://arxiv.org/pdf/2507.16674'
citation: 'Alamia, A.*, <strong>Muzellec, S.*</strong>, Serre, T., VanRullen, R. (2025). GASPnet: Global Agreement to Synchronize Phases. arXiv preprint arXiv:2507.16674'
featured: false
---

In recent years, Transformer architectures have revolutionized most fields of artificial intelligence, relying on an attentional mechanism based on the agreement between keys and queries to select and route information in the network. In previous work, we introduced a novel, brain-inspired architecture that leverages a similar implementation to achieve a global 'routing by agreement' mechanism. Such a system modulates the network's activity by matching each neuron's key with a single global query, pooled across the entire network. Acting as a global attentional system, this mechanism improves noise robustness over baseline levels but is insufficient for multi-classification tasks. Here, we improve on this work by proposing a novel mechanism that combines aspects of the Transformer attentional operations with a compelling neuroscience theory, namely, binding by synchrony. This theory proposes that the brain binds together features by synchronizing the temporal activity of neurons encoding those features. This allows the binding of features from the same object while efficiently disentangling those from distinct objects. We drew inspiration from this theory and incorporated angular phases into all layers of a convolutional network. After achieving phase alignment via Kuramoto dynamics, we use this approach to enhance operations between neurons with similar phases and suppresses those with opposite phases. We test the benefits of this mechanism on two datasets: one composed of pairs of digits and one composed of a combination of an MNIST item superimposed on a CIFAR-10 image. Our results reveal better accuracy than CNN networks, proving more robust to noise and with better generalization abilities. Overall, we propose a novel mechanism that addresses the visual binding problem in neural networks by leveraging the synergy between neuroscience and machine learning.

![GASPNet](/images/gaspnet.png)

[Full paper link](https://arxiv.org/pdf/2507.16674)
