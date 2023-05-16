---
layout: post
title: V-DMGNN-GAN
subtitle: Spatial inpainting for Human Motion Prediction
thumbnail-img: /assets/img/dmgnn.jpg
tags: [VAE, GAN, PyTorch]
---

Variational seq2seq DMGNN-based GAN (V-DMGNN-GAN) model for human skeletal motion prediction.

**Abstract:** For the task of modelling and predicting human motion trajectories, existing
generative models suffer from occlusions and mislabeling that are commonplace
in human motion datasets. We tackle this problem by building a network that
can accurately infer trajectories of skeletal joints missing from input, by building
upon previous work on deterministic multi-scale motion prediction. We build a
GAN-based architecture consisting of a variational auto-encoder (VAE) as our
generator network to learn the distribution of human motion and a recurrent neural
network-based discriminator for explicitly penalizing the unrealistic motion that
is generated from our generator.


[GitHub](https://github.com/AnushreeBannadabhavi/V-DMGNN-GAN/tree/master) | [Report](https://github.com/AnushreeBannadabhavi/V-DMGNN-GAN/blob/master/report/EECE_571F_Final_Project_Report.pdf)