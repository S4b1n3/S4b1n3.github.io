---
title: "Tracking objects that change in appearance with phase synchrony"
collection: publications
category: ai_conferences
permalink: /publication/tracking
excerpt: 'We introduce a complex-valued recurrent neural network (CV-RNN) that leverages neural synchrony to bind the different features of target objects while they change locations, offering a biologically inspired mechanism for tracking appearance-morphing objects. Using FeatureTracker, a large-scale challenge involving controlled changes in object shape, color, and location, we show that while standard deep networks fail, the CV-RNN closely matches human performance, providing a computational proof-of-concept for synchrony-based object tracking.'
date: 2024-10-02
venue: 'International Conference on Learning Representations (ICLR)'
paperurl: 'https://arxiv.org/pdf/2410.02094'
citation: '<strong>Muzellec, S.*</strong>, Linsley, D.*, Ashok, A. K., Mingolla, E.,  Malik, G., VanRullen, R., Serre, T.  (2024). Tracking objects that change in appearance with phase synchrony. International Conference on Learning Representations (ICLR).'
featured: true
header:
    teaser: "tracking.png"
---

Objects we encounter often change appearance as we interact with them. Changes in illumination (shadows), object pose, or the movement of non-rigid objects can drastically alter available image features. How do biological visual systems track objects as they change? One plausible mechanism involves attentional mechanisms for reasoning about the locations of objects independently of their appearances --- a capability that prominent neuroscience theories have associated with computing through neural synchrony. Here, we describe a novel deep learning circuit that can learn to precisely control attention to features separately from their location in the world through neural synchrony: the complex-valued recurrent neural network (CV-RNN). Next, we compare object tracking in humans, the CV-RNN, and other deep neural networks (DNNs), using FeatureTracker: a large-scale challenge that asks observers to track objects as their locations and appearances change in precisely controlled ways. While humans effortlessly solved FeatureTracker, state-of-the-art DNNs did not. In contrast, our CV-RNN behaved similarly to humans on the challenge, providing a computational proof-of-concept for the role of phase synchronization as a neural substrate for tracking appearance-morphing objects as they move about.

![Phase synchrony enables appearance-invariant tracking](/images/featuretracker.png)

[Full paper link](https://arxiv.org/pdf/2410.02094)
