---
layout: post
title: Transformer-based models for fMRI analysis
subtitle: An interpretable model for Autism Spectrum disorder prediction
thumbnail-img: /assets/img/ohbm.jpg
tags: [transformers, fMRI, PyTorch, wandB]
---

<b>TransMod</b> - a transformer-based architecture with modularity maximization pooling layer, to obtain high-quality brain network communities for ASD prediction. This work has been selected for poster presentation in the 2023 [OHBM](https://www.humanbrainmapping.org/i4a/pages/index.cfm?pageid=4114) Annual Meeting.

{: .box-warning}
**Note:** We extended this work and developed a more accurate and interpretable model for prediction of Autism Spectrum Disorder and submitted to the MICCAI 2023 conference (Impact factor: 13.828). Project details with the code will be shared after the conference decision.

**Abstract**: Autism Spectrum Disorder (ASD) is a neurodevelopmental disorder that affects communication, social interaction, and behavior. Transformers are powerful Artificial Intelligence tools and have been used in the
analysis of functional connectivity (FC) on brain regions of interest (ROIs) recently. However, the
previous method did not consider graph topology and modularity, which can greatly help in understanding
the structure and function of brain networks and therefore aid in the diagnosis of clinical disorders,
including ASD. Given the significance of identifying ROI communities and their relevance in ASD
diagnosis, we propose a novel Transformer-based architecture with modularity maximization pooling layer:
TransMod, to obtain high-quality brain network communities for ASD prediction.

### Architecture

We used the Autism Brain Imaging Data Exchange (ABIDE) dataset, a collection of resting-state functional
MRI data from 17 international sites with Configurable Pipeline for the Analysis of Connectomes (CPAC),
parcellated by Craddock 200 atlas. It includes data from 1009 individuals, 51.14% of whom were
diagnosed with ASD. Correlation matrix computed using the mean time series of ROIs (nodes in the graph)
and Pearson correlation coefficient is used as input to the model. Stratified sampling strategy is used for
1 2 3
1 2
3train-validation-test data split.
Model Architecture: There are two components in TransMod (Fig. 1 (b)), (i) The Transformer Encoder Layer
and (ii) DMon Pooling Layer. Inspired by BrainNetTF, we chose Transformer Multi-Head Self Attention
module to learn the underlying FC of nodes and update node embeddings using attention mechanism.
Studies suggest that ASD is associated with abnormal FC; therefore, detecting brain communities
(clusters) is crucial for ASD prediction. An extensively used graph-theory based approach to detect clusters
is 'modularity maximization', which divides ROIs into clusters by maximizing a global objective function, the
modularity metric. Previous works on Brain Network Analysis do not fully leverage these insights.
Therefore, we adapt a Graph Convolutional Network (GCN)-based DMoN pool layer that maximizes the
spectral 'modularity' metric, thus enabling the soft assignment of nodes to different clusters and aggregate
(pool) cluster-wise ROI embedding. This pooled feature matrix is then flattened and passed through a linear
layer to get binary class prediction (Healthy Control (HC) vs ASD).
Objective function and Optimization: The objective function incorporates both Cross-Entropy loss and DMoN
Pool Loss. The DMoN Pool Loss function optimizes cluster assignments through a combination of three
terms: the 'spectral modularity' term to be maximized, the 'orthogonality loss' term that encourages the
cluster assignments to be orthogonal, and the 'collapse regularization' term that discourages the formation
of trivial clusters and prevents getting stuck in local minima.

![arch](/assets/img/ohbm-arch.PNG){: .mx-auto.d-block :}

### Results

TransMod achieves comparable performance with the state-of-the-art (SOTA) methods with a better
accuracy of 71.2% and AUROC 80.7% on average (Fig 2.a). The attention matrices learned by the first
transformer layer (Fig 2.b) shows that the learned attention scores match the divisions of 7 functional
networks consistently identified in prior studies. ROIs in default mode and limbic networks, cerebellum,
and subcortical structures display large weights, consistent with the aberrant FC findings reported in autism
studies.

![Results](/assets/img/ohbm-results.png){: .mx-auto.d-block :}