---
layout: post
title: Community-Aware Transformer for Autism Prediction in fMRI Connectome
subtitle: Selected for the MICCAI 2023 conference
thumbnail-img: /assets/img/ohbm.jpg
tags: [transformers, fMRI, PyTorch, wandB]
---

<b>Com-BrainTF</b> - A novel local-global hierarchical transformer architecture to efficiently learn and integrate community-aware ROI embeddings for fMRI connectome analysis by utilizing both ROI-level and community-level information. Our paper got accepted in the prestigious [MICCAI](https://conferences.miccai.org/2023/en/) (The Medical Image Computing and Computer Assisted Intervention Society) 2023 conference.

<b>TransMod</b> - a transformer-based architecture with modularity maximization pooling layer, to obtain high-quality brain network communities for ASD prediction. This work has been selected for poster presentation in the 2023 [OHBM](https://www.humanbrainmapping.org/i4a/pages/index.cfm?pageid=4114) Annual Meeting.

**Abstract**: Autism spectrum disorder(ASD) is a lifelong neurodevelopmental condition that affects social communication and behavior. Investigating functional magnetic resonance imaging (fMRI)-based  brain functional connectome can aid in the understanding and diagnosis of ASD, leading to more effective treatments. The brain is modeled as a network of brain Regions of Interest (ROIs), and ROIs form communities and knowledge of these communities is crucial for ASD diagnosis. On one hand, Transformer-based models have proven to be highly effective across several tasks, including fMRI connectome analysis to learn useful representations of ROIs. On the other hand, existing transformer-based models treat all ROIs equally and overlook the impact of community-specific associations when learning node embeddings. To fill this gap, we propose a novel method, Com-BrainTF, a hierarchical local-global transformer architecture that learns intra and inter-community aware node embeddings for ASD prediction task. Furthermore, we avoid over-parameterization by sharing the local transformer parameters for different communities but optimize unique learnable prompt tokens for each community. Our model outperforms state-of-the-art (SOTA) architecture on ABIDE dataset and has high interpretability, evident from the attention module.

[GitHub](https://github.com/AnushreeBannadabhavi/Com-BrainTF)