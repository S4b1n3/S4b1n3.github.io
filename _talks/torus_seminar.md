---
title: "AI Tasting Seminar"
collection: talks
type: "Talk"
permalink: /talks/torus_seminar
venue: "Torus AI"
date: 2023-09-07
location: "Toulouse, France"
---

Attribution methods are essential for understanding how deep networks make decisions, yet prediction-based approaches routinely outperform classic gradient-based ones. We show that the key difference lies in their frequency content: gradient-based attribution maps contain excessive high-frequency noise, while prediction-based maps do not. By analyzing gradients across multiple CNN classifiers, we trace this noise to aliasing introduced during downsampling operations. Applying an optimal low-pass filter removes this high-frequency contamination and dramatically improves the performance of gradient-based methods, reshaping the ranking of state-of-the-art attribution techniques. Our results highlight a simple principle—filtering out high-frequency noise restores the faithfulness of gradients, and point toward a renewed appreciation of efficient, interpretable gradient-based explanations.

<p style="text-align:center; margin-top:0.5rem;">
  <a href="https://blogs.torus.ai/gradient-strikes-back-how-filtering-out-high-frequencies-improves-explanations/"
     target="_blank" rel="noopener"
     style="display:inline-block; padding:0.4rem 0.9rem; border-radius:999px;
            border:1px solid #444; text-decoration:none;">
    ▶ More information →
  </a>
</p>